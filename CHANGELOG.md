Changelog
=========

v0.13.0
-------

* Working process-based containers with development mode
* new [development workflow](https://github.com/nearform/nscale-workshop/blob/master/development-workflow.md)
  tutorial.
* Do not allow '-' in the system names [#48](https://github.com/nearform/nscale/issues/48).
* Support custom branch in `repositoryUrl`.

v0.12.0
-------

* Handle HTTP git urls inside service definitions
* Protect against missing systems in the Kernel API
* Better output on the client for missing systems

v0.11.0
-------

* Integrated
  [docker-registry-server](http://npm.im/docker-registry-server),
  so that builds and pulls requires less time as it deduplicates
* Analysis refactoring to complete faster

v0.10.1
-------

* fixed .gitignore not created together with new systems
  https://github.com/nearform/nscale/issues/32
* fixed prompt partially invisible on solarized dark
  https://github.com/nearform/nscale/issues/33
* fixed compiling system with non-js fle in defitions
  https://github.com/nearform/nscale/issues/34
* new AWS tutorial, see
  [ex8](https://github.com/nearform/nscale-workshop/blob/master/ex8.md)


v0.10.0
------

* full AWS cold boot support
* AWS configuration cleaned up
* support for deployment on bare metal
* preliminary supporto for DigitalOcean
* improved kernel debug logging
* corrected default configuration in web and api
* removd unused code from nscale-util

v0.9.0
------

* Check javascript validity with JsHint before compilation
* Improved error reporting for the compiler
* Check on the logical validity of a system.js configuration
* Support multiple root elements in the system.js
* Added a direct environment for bare metal/ssh-only vms
* Reduced disk space for image exports with gzip
* Added a '-v' flag that display nscale version
* Removed docker-registry-container and merged it with docker-container
* Added Google Analytics opt-in usage tracking
* Improved support for AWS

v0.8.0
------

* Improved support for AWS
* AWS plugins now compatible with compilation process
* Compiler support for addtitional attirbutes in topology section

v0.7.1
------

* Support for docker over TLS
* Support for boot2docker 1.3.0

v0.7.0
------

* Improved dockerBuilder
* Added docker-registry-container to use stock images from Docker Hub
* Updated the workshop to avoid the 'missing libssl-dev' issue
  https://github.com/nearform/nscale-workshop/issues/16
* Moved the documentation from the wiki to the repository

v0.6.0
------

* Fixed `nsd cont buildall`
* Refactoring and added tests of nscale-kernel

v0.5.0
------

* nscale no longer deletes docker containers and images during build
* introduced the new system compiler to avoid messing with system.json
* added process containers
* refactored of the analyzers to generalize the docker parts
* improved the client output during build and deploy
* added `nsd sys link <path>` command
* added `nsd cont buildall` command
* moved the checkout folders for containers repositories from `.nscale`
  to `<system>/workspace`
* moved the build folders for containers repositories from `.nscale`
  to `<system>/builds`
* improved system create, now using a better project generator

v0.4.0
------

* sudo arguments removed, now relies on membership of docker group
* fixed git clone issue on hypenated urls
* fixed hardcoded localhost in webapp
* client code cleanup


v0.3.0
------

* filters added to local docker analyzer
* nscale-system tag filter for AWS analyzer
* system name tag added on AWS instance boot
* improved error reporting for system commands
* Refactor for common nscale docker analyzer


v0.2.0
------

* Remove virtualbox-container and use blank-container instead.
* Merged boot2docker-container and docker-container,
  Linux and Mac OS X can now run the same examples.
* Customizable kernel logging.
* Correctly quoting paths with spaces.
* Automatic system detection for nscale-client
* SSH pre-connect to fix known\_hosts problems
* Error handling for missing github keys
* Improved crash reports.
* Added release policy.

v0.1.38
------

* Initial public release for nodeconf.eu 2014.

