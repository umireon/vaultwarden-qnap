# Vaultwarden deployment definition for QNAP Container Station

You can install this definition into QNAP Container Station as an application.

Both ARM and x86 should be supported, although I tested this only on ARM.

This definition will publish the vaultwarden as an HTTPS service with the non-standard port (8443) and the myQNAPCloud domain.

# Prerequisites

- Configure the myQNAPCloud domain and install Container Station.
- Remember the email address you used in the Let's Encrypt configuration of myQNAPCloud.
- Enable NAS Web and expose 80 to the internet and ensure that redirection to HTTPS is disabled.

# Installation

1. Create a shared folder named `vaultwarden.`
2. Click the Create Application button in Container Station.
3. Name a new application and paste docker-compose.yml into the text box.
4. Edit the definition to meet your environment.
5. Validate YAML and create the application.
6. Expose 8443 to the internet.
7. Enjoy your vaultwarden!

# About ACME

The webroot of [acme-companion](https://github.com/nginx-proxy/acme-companion) should usually be [nginx-proxy's](https://github.com/nginx-proxy/nginx-proxy) one, but in this definition sets to be NAS Web's one.
Acme-companion will create an ACME challenge file in the Web share, and it will be exposed by NAS Web so that the ACME challenge for myQNAPCloud domain will succeed.
