<pre lang="markdown">
# Gradle Private Package Test

This repository tests a Gradle setup that uses a private package from JFrog Artifactory.

## Package Location

The package used is located at:

```
https://endorlabs1.jfrog.io/artifactory/testpackage-nuget/com/endor/endor-utils/1.0.0/endor-utils-1.0.0.pom
```

## Setup Instructions

To test the setup, you need to configure the credentials using `endorctl`:

### Set Artifactory Username

```bash
endorctl api create -n -r PackageManager -d '{
  "meta": {
    "name": "gradle properties"
  },
  "spec": {
    "gradle": {
      "property_key_name": "artifactoryUsername",
      "property_key_value": ""
    }
  }
}'
```

### Set Artifactory Password

```bash
endorctl api create -n -r PackageManager -d '{
  "meta": {
    "name": "gradle properties"
  },
  "spec": {
    "gradle": {
      "property_key_name": "artifactoryPassword",
      "property_key_value": ""
    }
  }
}'
```

> ⚠️ Be sure to replace the empty `property_key_value` fields with your actual Artifactory credentials.
</pre>
