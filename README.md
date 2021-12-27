# nginx-ssl-template
An nginx + SSL scaffold based on Docker Compose for quick deployment of small sites

## How to use
1. Create a repo from this template.
2. Edit *nginx/mydomain.com.conf*, replace all the `mydomain.com` with your domain name.
3. Rename *nginx/mydomain.com.conf* to your domain with `.conf` extension for easier maintenance. (optional)
4. If you've changed the file name of the nginx site config, remember to update the service's volume config in &*docker-compose.yml* accordingly.
5. Edit *init-letsencrypt.sh*. Update the variables of `domains` and `email` to the actual values.
6. Set `staging=1` in *init-letsencrypt.sh* for test flight. (optional)
7. **For the first-timer deployment**, run `./init-letsencrypt.sh` to generate the SSL certificate.
8. Update the compose file and nginx site config to integrate with your app server.
9. `docker-compose up` your server and you are good to go!
