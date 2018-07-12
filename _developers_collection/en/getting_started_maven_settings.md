---
layout: default
title: Set up your maven settings file
tags: developers_getting_started
sequence: 20
summary: maven `settings.xml`file for eclipse and cmdline
lang: en
ref: developers_getting_started_mvn_settings
---

Here is a simple `settings.xml` file that you might want to place in your maven `.m2` folder.
It makes sure that maven knows about our maven repo

```xml
<?xml version="1.0" encoding="UTF-8"?>

<!-- Licensed under http://www.apache.org/licenses/LICENSE-2.0 -->
<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0 http://maven.apache.org/xsd/settings-1.0.0.xsd">
  <!-- localRepository
   The path to the local repository maven will use to store artifacts.
	 Default: ~/.m2/repository
	 If you have more than one local (eclipse-)workspace, it might make sense to have one local repo per-workspace, to avoid inconsistencies.
	<localRepository>${user.home}\.m2\mvn-eclipse-ws-1</localRepository>
  -->
	<profiles>
		<profile>
			<id>env-dev</id>
			<properties>
				<!--
				Go with 10.0.0.0 if you have all metasfresh projects in your workspace anyways
				The maven repo does not contain any metasfresh artifact with this version, so m2e will just download various maven-metadata.xml files,
				but not the binary artifacts
				-->
				<metasfresh.version>10.0.0</metasfresh.version>
				<!--
				Use this version range if you have only a few metasfresh projects in your workspace
				*or* if from time to time you need to build individual modules from command line
				m2e will download the ones that are missing from the repository, but prefer the ones that are in your workspace
        Warning: those ranges can give the m2e plugin even more problems than the fixed version
				<metasfresh.version>[1,10.0.0]</metasfresh.version>
				-->
			</properties>

			<repositories>
				<repository>
					<id>metasfresh-repo</id>
					<releases>
						<enabled>true</enabled>
						<updatePolicy>always</updatePolicy>
						<checksumPolicy>warn</checksumPolicy>
					</releases>
					<url>https://repo.metasfresh.com/content/groups/mvn-master/</url>
				</repository>
			</repositories>
		</profile>

	</profiles>

	<activeProfiles>
		<activeProfile>env-dev</activeProfile>
	</activeProfiles>
</settings>
```
