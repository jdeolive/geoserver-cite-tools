GeoServer CITE Tools
====================

Requirements
------------

* git
* maven
* ant

Building the Tools
------------------

1. Clone the ``geoserver-cite-tools`` repository:

       % git clone git://github.com/jdeolive/geoserver-cite-tools.git 

1. Build the tools with maven:

       % mvn install

Testing from Command Line
-------------------------

The ``build.xml`` file is used to perform test runs. Run ant with no arguments
to show information about available targets:

    % ant 
    usage:
     [echo] 
     [echo] Targets:
     [echo] 
     [echo]  wfs-1.0        --> Run WFS 1.0 tests
     [echo]  wfs-1.0-log    --> View WFS 1.0 test log
     [echo]  wfs-1.1        --> Run WFS 1.1 tests
     [echo]  wfs-1.1-log    --> View WFS 1.1 test log
     [echo]  wms-1.1        --> Run WMS 1.1 tests
     [echo]  wms-1.1-log    --> View WMS 1.1 test log
     [echo]  wms-1.3        --> Run WMS 1.3 tests
     [echo]  wms-1.3-log    --> View WMS 1.3 test log
     [echo]  wcs-1.0        --> Run WCS 1.0 tests
     [echo]  wcs-1.0-log    --> View WCS 1.0 test log
     [echo]  wcs-1.1        --> Run WCS 1.1 tests
     [echo]  wcs-1.1-log    --> View WCS 1.1 test log
     [echo]  clean          --> Cleans results from previous test runs
     [echo]  webapp         --> Runs teamengine web application

To perform a test run execute the ant command passing it the service to test.
For example to test the WFS 1.0 service:

    ant wfs-1.0

To view the log of a test run execute the ant command passing it the service 
name suffixed with "-log". For example, to view the WFS 1.0 logs:

    ant wfs-1.0-log

To clean results from previous test runs run the command:

    ant clean

Testing from the Web Application
--------------------------------

TEAMEngine comes with a web application that can be used to execute tests and 
view test results. To run the teamengine web application:

    ant webapp

By default the engine is available at http://localhost:9090/teamengine. To 
change the webapp port edit the file ``engine/pom.xml``.
