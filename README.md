# Linux Server Configuration
========================

This project involves configuring a Linux web server (LAPP stack) to host a restaurant website using a relational database. The Restaurant app also utilizes CSS style sheets, JSON returns and utilizes the Google+ API and Facebook API for OAuth login as well as demonstrates CRUD operators for all items. Please view my commits for latest updates.

###Server Address
----------
* IP: 52.35.181.210
* URL: http://ec2-52-35-181-210.us-west-2.compute.amazonaws.com/

###SSH Port
----------
* SSH Port: 2200

###Summary of Software Installed and Steps to Configure
----------
* Create user ```Grader``` with sudo permission.
* Add SSH public key to ```Grader``` ssh directory.
* Remove ssh access from ```root```.
* Configure UFW to only allow ports 2222/tcp, 80/tcpm, 2200, 123, 8080.
* Install the ***LAPP*** stack. Includes the following (some of which were perviously installed):
    * ***L***inux distribution: Ubuntu 14.0
    * ***A***pache2
    * ***P***ostgreSQL
    * ***P***ython
* Install the ***mod_wsgi*** and enabled it.
    * libapache2-mod-wsgi python-dev
* Install ***Git*** and clone my repository from [here][4] in the ```/var/www/``` directory
    * git
* Install the dependencies for the app to run
    * Flask (0.10.1)
    * Flask-SQLAlchemy (2.1)
    * Flask-WTF (0.12)
    * oauth (1.0.1)
    * oauth2client (2.0.1)
    * oauthlib (1.0.3)
    * requests (2.2.1)
    * requests-oauthlib (0.6.1)
    * SQLAlchemy (1.0.12)
    * virtualenv (15.0.1)
    * WTForms (2.1)

* Activate the restaurant virtual environment
* Create ```Restaurant.conf``` file in ```/etc/apache2/sites-available/``` directory
* Deactivate the default host and activate the Restaurant host
* Create ```restaurant.wsgi``` file in ```/var/www/Restaurant/``` directory

###Third Party Resources
----------
* Python 2.7.10
* Bootstrap
* SQLAlchemy
* PostgreSQL
* Flask  
* Special modules:
    * SQLAlchemy
    * BaseHTTPServer
    * FLask
    * WTForms
* Google+ OAuth2 API
* Facebook OAuth2 API

###Support/Contact
----------
If you are having issues, please let me know. Contributions, tips and comments are welcome!
* Email: robertkohl125@gmail.com
* [Github Profile][5]
* [StackOverflow Profile][6]
* [LinkedIn Profile][7]

###License
----------
The MIT License (MIT)

Copyright (c) [2015] [Robert Kohl]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.


[4]: https://github.com/robertkohl125/Restaurant.git "Github repository"
[5]: https://github.com/robertkohl125 "Github Profile"
[6]: http://stackoverflow.com/users/2180707/robertkohl125?tab=profile "Stack Overflow Profile"
[7]: https://www.linkedin.com/in/robertkohl125 "LinkedIn"