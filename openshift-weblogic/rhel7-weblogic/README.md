WebLogic base Image
===================

This Dockerfile will build a base image with WebLogic. It extends the
rhel7-java-180-oracle image, which is a basic RHEL 7 image with Red Hat
distributed oracle java packages installed.

This is an adaptation of the Dockerfile provided by Oracle here:
https://github.com/oracle/docker-images/tree/master/OracleWebLogic/dockerfiles/


Required Files
==============

This build requires that you host a local copy of the WebLogic installer in
a fileserver within your environment. You can use either the quick or generic
installers.

For example, the generic installer: fmw_12.2.1.3.0_wls_Disk1_1of1.zip 

Or for quick installer: fmw_12.2.1.3.0_wls_quick_Disk1_1of1.zip 

These may be downloaded from:
http://www.oracle.com/technetwork/middleware/weblogic/downloads/wls-for-dev-1703574.html 

Image Build Configuration
=========================

You _must_ specify a few environment variables for the OpenShift build to obtain
the WebLogic Fusion Middleware software. These are as follows:

