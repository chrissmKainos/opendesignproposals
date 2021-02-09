## 0001 - Local Authority Nuget
###### Author(s) - Chris Smith
## Introduction
Detailed below is the suggested approach to be taken to replace the current Local Authority Service built into the He.Htb.Apply solution with a standalone nuget package which can be shared and consumed by many.

## Detail
This full breakout of the service, nuget creation/publish and finally nuget consumption will be done as two individual sub tasks. In doing this we will reduce any impact on the current develop branch of the He.Htb.Apply pipeline.

#### Sub task 1: New service project & Nuget
A new project will be created within the existing He.Htb.Apply solution, this will contain an exact copy of the code in use by the existing He.Htb.Apply.Application project. The new project structure will be:
* __Repo name__: he-htb-apply
* __Solution name__: He.Htb.Apply
* __Project name__: He.Htb.Apply.Services.LocalAuthority

The above code will be merged into the  develop branch of the he-htb-apply repo with a new nuget package published to:
* __Package feed__: homesengland/Help to Buy Apply Beta/Artifacts/Packages
* __Nuget name__: He.Htb.Apply.Services.LocalAuthority

__Note:__ Sub task 2 will only beging once the above update has succesfully passed through the CI pipelines and a nuget package is available on the proposed feed.

#### Sub task 2: Replace existing service with Nuget
Given we now have a published nuget package for the local authority service, we can remove the original service and replace it with the nuget.

* Remove LocalAuthorityService classes from project He.Htb.Apply.Application
* Replace any references to the removed LocalAuthorityService with the new nuget package.

## Questions to consider

* Is ths proposed repo/solution/project structure suitable?
* Is the propsed nuget feed suitable?
* How do we build & publish the nuget package as part of the CI pipeline?