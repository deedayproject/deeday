# Setup the project

## Install Docker

You must install Docker in order to make the project working.  
To install it, run `brew cask install docker` on your terminal (ZSH, bash...), then launch it

## Setup files

Once Docker has been installed, you must pull the Docker files from GitHub  
You can find it here:  
deeday: `git clone git@github.com:deedayproject/deeday deeday`

Then, once it has been pulled, go inside with `cd` then, download the project API and client inside  
You can find these here:  
deeday-client: `git clone git@github.com:deedayproject/deeday-front client`  
deeday-api: `git clone git@github.com:deedayproject/deeday-api api`

## Mac Only warning

You have to install docker-sync. Run this:  
`sudo gem install docker-sync`

## Setup the containers

Once everything has been done, run `make up` to complete the installation, and let the magic happens ✨

Once every container has been setupped, you may install the packages of the client and the API  
To make this, run this in your favorite terminal:

`docker-compose run client npm i && docker-compose run php composer install`

To follow up the installation, follow the step on the sub repositories, links under this ❤️  
[API](https://github.com/deedayproject/deeday-api/blob/master/README.md)
