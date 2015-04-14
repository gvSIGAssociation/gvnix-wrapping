======================================================================
GVNIX WRAPPING REPOSITORY
======================================================================

This Git repository contains various script files that enable easy
production of OSGi-compliant bundles using a technique known as
"wrapping". These are generally used by gvNIX and its add-ons.

You can read more about gvNIX at the following location:

   http://www.gvnix.org

======================================================================
GIT POLICIES
======================================================================

The same Git policies apply to this repository as the normal gvNIX
repository.

======================================================================
RELEASING
======================================================================

The wrapping repository is separated from the normal gvNIX repository so
that each project in the wrapping repository can be released as part
of its own release cycle. The wrapping projects are NOT released
during the normal gvNIX release cycle and the gvNIX CI server does NOT
perform any wrapping module releases.

As such, it is expected that developers wishing to make wrapped JAR
available will manually produce/edit the relevant subdirectory of the
wrapping JAR and then use:

   mvn clean deploy

IMPORTANT: Ensure you increment the final three-digit prefix for the
version number displayed in the pom.xml. Also ensure you edit the
main Roo pom.xml <dependencyManagement> section to refer to the new
version once you have completed the deployment. This ensures everyone
is on the latest release you have made.

======================================================================
HELP
======================================================================

If you have general questions on gvNIX's wrapping approach, please use
StackOverflow. Thanks for your interest in gvNIX!

