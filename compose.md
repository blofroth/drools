# JBPM workbench and KIE server with Docker Compose

## Prerequisites

* Docker (tested with 17.06.0-ce)
* docker-compose (tested with 1.14.0)
* Checked projects with the same parent directory:
    * `git@github.com:blofroth/drools.git`
    * `git@github.com:blofroth/jbpm.git`

# Instructions

1. Build the base images:

        docker-compose -f docker-compose.base.yml build

2. Bring up the containers:

        docker-compose up

  * or daemonized:

        docker-compose up -d

# Exposed endpoints

Assuming your Docker host has hostname `${DOCKER_HOST}`, you should be
able to access:

* JBPM web console (admin/admin):

    * http://${DOCKER_HOST}:8080/jbpm-console

* KIE server rest interface (kieserver/kieserver1!):

    * http://${DOCKER_HOST}:8081/kie-server/services/rest/server

# Usage

1. Open the JBPM web console

2. Log in (admin/admin)

3. Create an example project by choosing _Project Authoring_ and selecting 
one (e.g. _itorders_)