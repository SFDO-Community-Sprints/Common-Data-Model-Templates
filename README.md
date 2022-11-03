# Common-Data-Model-Templates
Template org for the Common Data Model template


## Use Case
## Entity Relationship Diagram
## Data Dictionary 
## Installation
## Customization
## Contributing to the Data Model
### Through CummulusCI
#### Pre Requisites 
1. Github Accoount
2. Contributor Access to the Data Model Repository
3. Git cli intalled on local machine
4. [Set up CumulusCI](https://cumulusci.readthedocs.io/en/latest/get-started.html)


Connect CumulusCI to the GitHub account used to access this repository.
`cci service connect github`

Connect CCI to DevHub
`cci org connect {org-alias}` Authenticate to the devhub org for the project 
`cci service connect devhub --project` Tell CCI the alias of the devhub org to use for this project (org that was connected in previous step)

Verify DevHub and GitHub service
`cci service list`

#### Feature Development

1. Pull *main* branch to get latest updates `git pull origin main`
1. Create feature branch off of *main* branch `git checkout -b feature/issue-key-descriptiveBranchName`
1. Run `cci flow run dev_org --org dev` to create a new scratch org and deploy this project.
1. Run `cci org browser dev` to open the org in your browser.
1. Either develop locally and push to scratch org, or develop in scratch org and pull changes
1. If developing feature in scratch org run `cci task run list_changes --org dev` to see changes that will sync
1. If developing feature in scratch org run `cci task run retrieve_changes --org dev` to retrieve the changes locally.
1. If developing locally, run `cci task run dx_push --org dev` to push local changes to scratch org
1. Add and commit changes to feature branch `git add .` and `git commit -m "issue-KEY: descriptive commit message"`
1. Push feature branch to GitHub and create a pull request to *develop* branch for review `git push origin feature/issue-key-descriptiveBranchName`
1. Delete the scratch org `cci org scratch_delete dev`
### Through Metecho
### Process and Governance 

Common Data Models are Open-Source standardized extensible data schemas that include entities, attributes, semantic metadata, and relationships. While Open-Source, these models try to maximize accessibility by making it an Unlocked Package. When contributing to Common Data Models, the project follow a governance process to ensure it meets all standards.

#### Design-Driven Development
1. Any new Data Model or changes to an existing Data Model will have to go through a review process before being approved for development. 
2. All requests for new features or changes should be first shared in the Trailblazer Community. This is to capture some commmunity feedback on interest as well as some initial requirements.
3. An individual on the Common Data Models Team creates Feature Request Issue in Github following the template, capturing some initial requirements while articulating some expectations.
4. The Feature Request is reviewed by the Common Data Models Team and technical specs are created, adding to the Issue created.
5. The Feature Request Issue is assigned to an individual or a request is made to the community for support on development of the Feature Request.
6. The assigned Developer will document and articulate their solution as part of their process (Create/Update ERD, Data Dictionary).
 #### Development Process
1. Start by creating a new branch from the master branch. Salesforce CLI users will need to do this in Github or Github Desktop.
Make the appropriate edits and changes in your scratch org
2. Commit your changes to your branch.
3. Have your changes reviewed by a peer, utilizing the same tool you used to create the scratch org.
4. Once the peer review is complete, create a pull request.
5. Give as much detail as possible and link any issues you may have completed.
6. The pull request will be reviewed by the Project Leadership team. They will ask questions about the update and may bring the update/enhancement/changes to the monthly team meetings for discussion.





