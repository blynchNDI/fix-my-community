<div align="center">
    <div>
      <a href="https://fixmystreet.org/"><img src="https://www.mysociety.org/files/2014/11/fixmystreet-logo.jpg" alt ="FixMystreet Logo" width="200"></a>
        &nbsp;&nbsp;
      <a href="https://www.ndi.org/"><img src="https://www.ndi.org/sites/all/themes/ndi/images/NDI_logo_svg.svg" alt="NDI Logo" width="200"></a>
        &nbsp;&nbsp;
      <a href="https://www.mysociety.org/"><img src="https://www.mysociety.org/files/2014/11/mysociety-logo.jpg" alt ="MySociety Logo" width="200"></a>
    </div>
</div>

<h1 align="center">
  Fix My Community
</h1>



  ### Table of Contents
  1. [Overview](#overview)
  1. [Installation](#installation)
  1. [Additional Configuration](#additional-configuration)

### Overview

The Fix My Community (FMC) DemTool is created from the [FixMyStreet tool](https://fixmystreet.org/) developed by [mySociety](https://www.mysociety.org/). This tool empowers citizens to flag problems in their communities and to bring them to the attention of those who can fix them - or to rally the public around unaddressed issues. Crowdsourcing can put many eyes to work spotting critical problems citizens face. The tool routes citizen-submitted reports together with photos to the key government institutions who can solve them. By making complaints and government updates visible to the public, the tool helps officials demonstrate that they are taking action on the issues that concern citizens. Systems like Fix My Community have been used for reporting everything from potholes to bribes and are a useful bridge between citizens and their representatives.

This repository contains themeing and configuration files for Fix My Community, NDI’s adapted version of FixMyStreet. The instructions below explain how to install FixMyStreet and apply the customized themeing.

### Installation

The latest version of MySociety's code for FixMyStreet can be found at: https://github.com/mysociety/fixmystreet

The only dependency needed to run FixMyStreet is Docker and Docker-compose. Instructions for installing Docker can be found here (for ubuntu): https://docs.docker.com/install/linux/docker-ce/ubuntu/ . Instructions for installing docker-compose can be found here: https://docs.docker.com/compose/install/


Begin by installing both this repository along with the latest version of fixmystreet with the commands below. 
```
git clone https://github.com/mysociety/fixmystreet.git
git clone https://github.com/nditech/fix-my-community.git
```

Then, move the docker overide file into the fixmystreet folder with the command below. This file tells fixmystreet where to find the custom theme and config file.
```
cp fix-my-community/docker-compose.override.yml fixmystreet/docker-compose.override.yml
```

Now, start up FixMyStreet 
```
cd fixmystreet
sudo docker-compose up
```

This commands will start the application and launch four containers: nginx, memcached, postgres, and the FixMyStreet application itself.

By default, the site should then be available at localhost:8000 when installed locally, or at port 8000 if deployed on a server (*server-ip*:8000). The site should be spun up using the custom theme.

### Additional Configuration

For more detailed information on installation and themeing of FixMyStreet, go to https://fixmystreet.org/overview/

