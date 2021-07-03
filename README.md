# Vaultwarden deployment definition for QNAP Container Station

You can install this definition into QNAP Container Station as an application.

Both ARM and x86 are supported.

This definition requires another domain whose CNAME is set to be myQNAPCloud's one.

# Prerequisites

- Install Container Station.
- Disable HTTPS NAS Web (443).

# Installation

1. Create a shared folder named `vaultwarden` and `letsencrypt`.
2. Click the Create Application button in Container Station.
3. Name a new application and paste docker-compose.yml into the text box.
4. Edit the definition to meet your environment.
5. Validate YAML and create the application.
6. Expose 443 to the internet.
7. Enjoy your vaultwarden!
