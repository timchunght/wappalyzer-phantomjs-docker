Wappalyzer Phantomjs Docker Image
---

This is the base image for a pre-built environment that will enable you to run the Wappalyzer extension in a headless browser powered by Phantomjs. To get the docker file running, you need to have ``boot2docker`` installed on Mac. Under that assumption, let's move on.

#Boot2Docker basics

Start boot2docker:

	boot2docker start # default password is tcuser, try as many time as necessary until you see "started"

#Build the Docker image

	docker build -t wappa-phantomjs .

The above command will create a container based on the Dockerfile and name it ``wappa-phantomjs``, you can change the name to a name you prefer.

#Run the container and enter the bash/shell

	docker run -it wappa-phantomjs /bin/bash

Now, you are in the bash; play with your container. Yeah!

So, to run the phantomjs script, use the following command:

	/usr/local/phantomjs/bin/phantomjs --load-images=false --ignore-ssl-errors=yes --ssl-protocol=any driver.js http://dropbox.com

Note: replace ``http://dropbox.com`` with a URL you want to analyse.

Enjoy!

--Tim
timchunght
