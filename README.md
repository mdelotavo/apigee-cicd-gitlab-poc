# apigee_apis
Apigee Edge CI/CD consumer proof of concept

## deployproxy
This is set in `.gitlab-ci.yml` as a manual job and will run like so:
```console
$ apigeetool deployproxy --verbose --organization $APIGEE_ORG --username $APIGEE_USER --password $APIGEE_PASSWORD --environments test --api helloworld --directory api-proxies/helloworld/
Going to create revision 7 of API helloworld
Using api-proxies/helloworld/apiproxy/helloworld.xml as the root file
Creating revision 7 of API helloworld
No resources found
Uploading policy add-cors.xml
Uploading policy check-quota.xml
Uploading target default
Uploading proxy default
Deploying revision 7 of helloworld to test
Delaying deployment for 0 seconds
Deployment on test successful
"helloworld" Revision 7
  deployed
  environment = test
  base path = /
  URI = http://matthew-eval-test.apigee.net/v0/hello
  URI = https://matthew-eval-test.apigee.net/v0/hello

Job succeeded
```
