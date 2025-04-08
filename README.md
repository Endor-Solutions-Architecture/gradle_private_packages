This repo test a gradle setup with a private package from jfrog:

It get package located at: https://endorlabs1.jfrog.io/artifactory/testpackage-nuget/com/endor/endor-utils/1.0.0/endor-utils-1.0.0.pom

to test it you need to set: 

endorctl api create -n <tenant> -r PackageManager -d '{
    "meta": {
        "name": "gradle properties"
    },
    "spec": {
        "gradle": {
            "property_key_name": "artifactoryUsername",
            "property_key_value": "<username>"
        }
    }
}'

also:

endorctl api create -n <tenant> -r PackageManager -d '{
    "meta": {
        "name": "gradle properties"
    },
    "spec": {
        "gradle": {
            "property_key_name": "artifactoryPassword",
            "property_key_value": "<password>"
        }
    }
}'


