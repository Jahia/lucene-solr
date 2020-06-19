# Prepare : 

Install ant ..

then execute : 

```ant ivy-bootstrap```

# Build :

Build / deploy snapshots :

```ant -Dm2.repository.id=thirdparty-snapshots -Dm2.repository.url=https://devtools.jahia.com/nexus/content/repositories/thirdparty-snapshots/ generate-maven-artifacts```

(check that thirdparty-snapshots credentials are set up in your settings.xml)

# Make a release :

- switch the version in build.xml (do not touch pom.xml)
- commit and tag
- push artifacts : 

```ant -Dm2.repository.id=thirdparty-releases -Dm2.repository.url=https://devtools.jahia.com/nexus/content/repositories/thirdparty-releases/ generate-maven-artifacts```

(check that thirdparty-releases credentials are set up in your settings.xml)

- switch the version in build.xml for next development version
