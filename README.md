Name
====

Openshift Deployment Prep

Automation Summary
------------------

Meant to download resources required for deploying/updating Openshift on vSphere:
- oc
- openshift-install
- RHCOS ova
- container images

Variables
--------

    ocp_release

Specify your intended Openshift release (e.g. 4.6.19).

    ocp_resources_path

Change if desired - specify full path.  Defaulted to "/home/{{ ansible_env.USER }}/ocp-tools".

    local_registry

Specify the registry domain name, and optionally the port, that your mirror registry uses to serve content (e.g. rhel82:5000).

    local_repository

Do not change this unless you really know what you're doing.

    pullsecret_email

Specify the email associated with your pull secret.

    internet_connected

Do not change.

    product_repo: openshift-release-dev

Defaulted to openshift-release-dev.  This is the repository that the images would be mirrored to in your registry.  Do not change unless you really know what you're doing.

    release_name: ocp-release

Defaulted to ocp-release.  This is the repository that the images would be mirrored to in your registry.  Do not change unless you really know what you're doing.

    repo_url: https://mirror.openshift.com/pub/openshift-v4

Repo url is the location to download oc, openshift-install, and ova from.  Should not be changed unless url is changed.

    mirror_registry_user: ''

Username for the internal registry where images will be hosted and pulled from by the Openshift cluster.

    mirror_registry_passwd: ''

Password for the internal registry where images will be hosted and pulled from by the Openshift cluster.

    pullsecret: '{"auths":{"cloud.openshift.com":...'

Copy the pull secret from https://cloud.redhat.com/openshift/install/vsphere/user-provisioned.

    pullsecret_email: ''

Email address associated with pull secret.
