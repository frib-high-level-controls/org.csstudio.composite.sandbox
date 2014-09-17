org.csstudio.composite.sandbox
==============================

P2 composite repo for sharing sandbox features

To share your features with the CS-Studio Community, you can edit the the compositeArtifacts.xml and compositeContent.xml to include your p2 site.  The IUs will be available on http://downloads.controlsystemstudio.org/sandbox/4.0 as a P2 update site on commit to this repo.

P2 repos can be served from your personal webspace or even github as in the example, just add your child location:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<?compositeArtifactRepository version='1.0.0'?>
<repository name="CS Studio Sandbox Composite Repository" type="org.eclipse.equinox.internal.p2.artifact.repository.CompositeArtifactRepository" version="1.0.0">
  <properties size="3">
	  <property name="p2.compressed" value="true"/>
	  <property name='p2.atomic.composite.loading' value='false'/>
    <!-- get new time w/ `date +%s000` -->
    <property name="p2.timestamp" value="1395756034000"/>
  </properties>
  <children size="1">
	  <child location="https://github.com/berryma4/p2/raw/master/rocs/4.0"/>
	  <!-- add your repo here -->
  </children>
</repository>
```
