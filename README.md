# Octopus Deploy Integration Pack

This integration pack allows you to integrate with
[Octopus Deploy](http://octopusdeploy.com/),
deployment automation system for .NET applications.

## Actions

The following actions are supported:

### Projects

* Get Projects - `list_projects`
* Get Deployments - `list_deployments`

### Releases

* Create a new release - `create_release`
* Deploy a release to an environment - `deploy_release`
* Get a list of releases for a project - `list_releases`

### Machines (tentacles)

* Add a new machine to an environment(s) - `add_machine`

## Sensors

* Detect a new release being created - `new_release_sensor`
* Detect a new deployment being created - `new_deployment_sensor`

## Configuration

Copy the example configuration in [octopus.yaml.example](./octopus.yaml.example)
to `/opt/stackstorm/configs/octopus.yaml` and edit as required. It must contain:

* `api_key` - an API key generated in Octopus for your user http://docs.octopusdeploy.com/display/OD/How+to+create+an+API+key 
* `host` - the host name of your Octopus server e.g. octopus.mydomain.com
* `port` - the port your API service is running on, 443 by default

Read this pack tutorial for more information: https://stackstorm.com/2015/10/01/octopusdeploy-integration-with-stackstorm/
