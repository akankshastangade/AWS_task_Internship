
# Launching  2 WordPress web applications on EC2 instance and attach load balancer to that instance. Then storing the database of these 2 WordPress instances on MySQL instance.

Let’s see the setup and configurations for this-
# Step1: Launch 2 EC2 instances

![image](https://user-images.githubusercontent.com/72142324/182029165-64601cee-4379-44bd-bd6e-742b3a7e7d12.png)

# Step2: Install httpd webserver and start the services
Use command yum install httpd to install httpd webserver
And systemctl start httpd to start the services

# Step3: Install MySQL database in both the instances
This can be done by using command yum install php-mysqlnd mysql

# Step4: Install PHP
To install PHP, use amazon-linux-extras php7.3[version]

# Step5: Install WordPress software
Now, to install WordPress, use the following-
wget https://wordpress.org/latest.tar.gz
tar -xzf latest.tar.gz
Then copy the wordpress pages into /var/www/html directory
Step6: Create MySQL instance

![image](https://user-images.githubusercontent.com/72142324/182029200-ac7e6b15-bcce-4594-922b-c5ff49c309f9.png)

After providing these database credentials to the WordPress login, we can access the site.

![image](https://user-images.githubusercontent.com/72142324/182029218-57f3208c-faa1-45dd-b6a6-6cca8faae852.png)

Then will be able to see some content on the next page, copy that and create a file named as wp-config.php
Now run the installation …Our WordPress site is here,

![image](https://user-images.githubusercontent.com/72142324/182029229-c134abe6-4bf7-4f05-8ac4-ed90c87c1b7a.png)

Step7: Create Load Balancer and attach to both the created instances

![image](https://user-images.githubusercontent.com/72142324/182029241-89b7a427-59ea-4077-a303-3c7bce28208d.png)

Now, copy the DNS name and will be able to see our webpages as below

![image](https://user-images.githubusercontent.com/72142324/182029302-22c9db72-cf98-4108-bf5e-f137c9c64cd2.png)


We can see the output!!
Thank You For Reading!...


