# Nginx example configuration files

These are Nginx example configuration files to use in your deployed applications on server. Customize them to fit your needs.

The default location for these files in a Ubuntu Server machine is ´/etc/nginx/sites-available´.

By default in this repo all domain references are ´mysite.org´ and ´www.mysite.org´, you need to change them to your own domain and subdomains. For HTTPS support on these scripts, a SSL certificate from Let's Encrypt is generated, be sure to generate a certificate with ´certbot´ after customizing the Nginx configuration files

For example, a config file called ´mysite.conf´ should be in ´/etc/nginx/sites-available/mysite.conf´. After this, symlink the configuration file to ´/etc/nginx/sites-enabled´:

´´´
sudo ln -s /etc/nginx/sites-available/mysite.conf /etc/nginx/sites-enabled/mysite.conf
´´´

Then test the changes to Nginx:
´´´
sudo nginx -t
´´´

Then restart the Nginx service to make changes effective:
´´´
sudo service nginx restart
´´´

## License

MIT