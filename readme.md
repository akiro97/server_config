``` 


# Create Your VPS from providers
- ssh root@your_server_ip 

# Config Key-gen
- ssh-keygen

# update & upgrade  os packages
- sudo apt update & sudo apt upgrade


# Create New user
- adduser -username && password && confirm password

# Add user group as Admin
- usermod -aG sudo username

# Login User
- su - username

# 


# Create github action
- 

# github action runner

# Install node management package 
- nvm / github

# install nodejs

# config database / cloud database

# config cach memory

# config database backup / restore

# Install package server SSL
- sudo apt install nginx certbot python3-certbot-nginx

# Install Run project environment packages / PM2
- npm install pm2 -g

# Create directory For @ /var/www/

# Make dir to new user mode
- sudo chown -R username:username dir_name/ 
	. ls -1a (check role user on dir)
	

# Create nginx site available site_config_file_name
- nano /etc/nginx/sites-available/file_name 
	Add these config to the file
	
	server {
		listen 80;
		server_name www.example.com example.com;
		
		gzip on;
		gzip_proxied any;
		gzip_types application/javascript application/x-javascript text/css text/javascript;
		gzip_comp_level 6;
		gzip_buffers 16 8k;
		gzip_min_length 256;
		
		location /_next/static/ {
			alias /var/www/dir_project_name/.next/static/;
			expires 365d;
			access_log off;
		}
		
		# Add multiple location
		location  / {
			proxy_pass http:127.0.0.1:3000 # APP_PORT
			proxy_http_version 1.1;
			proxy_set_header Upgrade $http_upgrade;
			proxy_set_header Connection 'upgrade';
			proxy_set_header Host $host;
			proxy_cache_bypass $http_upgrade;
		}
		
		location 2 / {
			proxy_pass http:127.0.0.1:3000 # APP_PORT
			proxy_http_version 1.1;
			proxy_set_header Upgrade $http_upgrade;
			proxy_set_header Connection 'upgrade';
			proxy_set_header Host $host;
			proxy_cache_bypass $http_upgrade;
		}
		
		location n / {
			proxy_pass http:127.0.0.1:3000 # APP_PORT
			proxy_http_version 1.1;
			proxy_set_header Upgrade $http_upgrade;
			proxy_set_header Connection 'upgrade';
			proxy_set_header Host $host;
			proxy_cache_bypass $http_upgrade;
		}
	}
	
# Remove nginx default file
- sudo rm /etc/nginx/sites-available/default


# Link Config file from site-available to sites-enable
- sudo ln -s /etc/nginx/sites-available/site_config_file_name /etc/nginx/sites-enabled/site_config_file_name 

# Restart nginx
- sudo systemctl restart nginx

# Clone projection from Github
- git clone repo_url

# Make dir to new user own mode again
- sudo chown -R username:username dir_name/ 
	. ls -1a (check role user on dir)
	
# Make firewall to allow use ssh
- sudo ufw allow "Nginx full"

# Check firewall status
- sudo ufw status

# Build nextjs project
- yarn build

# Run Nextjs project static site
- pm2 start yarn --name app_name -- start

# Check PM2 ready run app By:
- 

# Make SSL run to https req
- sudo certbot --nginx -d www.example.com -d exampl.com

# Make SSL auto check
- 	


 ```