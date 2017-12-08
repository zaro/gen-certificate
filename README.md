# cerbot gen certificates

Simple ansible playbook to run certbot on a server and copy the generated certificates back to your machine

# how to use

1. edit inventory/hosts and add the ip/domain of the server where cerbot will be run, and make sure the domains are pointed to this ip

2. edit inventory/group_vars/default.yml and add email and domains for let's encrypt

3. run

    ansible-playbook -i inventory/hosts gen_cerificates.yml

4. the resulting cerbot directory is copied in under certbot-generated/certbot/, you can find your certificates in certbot-generated/certbot/live/

5. if you wish you can make a zip with all certificates like so :

    zip -r certificates.zip certbot-generated/certbot/live/


# license

WHATEVER License

All files in this distribution shall be considered under this license agreement( or disagreement if you don't agree with it :) unless stated different  in the file itself.

This program is free, you can copy, redistribute it and generally do WHATEVER you want with it.
In the case you are using the code for commercial purpose without providing access to the source code itself I guess you are very sad and lonely person anyway and nobody wants to really have something to do with you.

Whatever 2017, Zaro <zarrro [AT] gmail [DOT] com>
