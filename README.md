# Community-Az-Devops-Pipeline-Templates
I try to use template files for my Azure Devops pipelines, and this is my attempt to put all of them in a single place.

I am going to attempt to structure these in a way that pipelines that are dependent on these are resilient to change as I can make them. If you use them please be aware that I may cause breaking changes. 

# How to use
You will add a resources attrbiute to your pipeline that will use them. Add triggers on `main` and `test` so that your pipeline will get triggered when we change the templates. 

```
resourcese
  repositories:
      - repository: templates
        type: github
        name: brandonmcclure/Community-Az-Devops-Pipeline-Templates
        endpoint: githubServiceConnection
        trigger:
          - main
          - test
      - repository: self
```
# Service Connections
Create the following service connections. Make sure the names match 

## Docker Registry
Name `Docker Hub`

## github
Name: `githubServiceConnection`