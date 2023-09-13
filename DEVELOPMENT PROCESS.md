# Development Process Conventions
This guide is about coding conventions and development process we use for every project. Its mandatory to abide by all the following instruction exactly as defined to get your milestones, pull requests and tasks get approved.

## Development Process
### Environments
For each project we usually have 3 environments `Production`, `Staging` and `Development` environment associated with branches default branch `main` or `master`, `staging` and `develop` respectively.
1. Development - This environment will have the latest features under development. And can be used between the development team and SQA persons for collaboration. For each new feature, issue create a new branch from `develop` branch. And create a pull request for `develop` branch of your newly created branch once your task is completed. The developers cannot push directly to this environment. They can create a Pull Request. Or just add a comment stating the branch name and deliverables that they completed.
2. Staging - For a set of features finalized by development team on develop branch. The project owner will create a Pull Request for Staging Envrionment. Staging environment is for Project Owner and Client to share thoughts, taking signoffs from client regarding features and getting feadback from client. The code in development environment must be tested from QA and developers throughly before merging it into staging.
3. Production - Once the features on staging are approved from client. The project owner will create a pull request for the default branch. And will merge it to make the release available for consumers.
### Branch Naming
There can two types of tickets on Zoho Projects. Feature or Issue. Each ticket created on Zoho Projects will have a reference number.
1. Issue - the naming will be as `issue/<ticket_reference_number>-<small_3_to_words_description>`. Example: `issue/T1-04-project_setup_backend`
2. Feature - the naming will be as `feature/<ticket_reference_number>-<small_3_to_words_description>`. Example: `feature/T1-04-project_setup_backend`
## Ticket Deliverables
The developer can create a Pull Request or incase he has limited access he/she can just add comments under the ticket (Mention branch name associated with the tickets in comments). The PR or ticket comments must have the following format
### Pull Request Format
1. Title - Add the ticket title and its reference number
2. Description - Must address following points
   - The detailed list of features or functioanalities or bugs that are resolved
   - How the other team members can test those features
   - Mention any feature or deliverable of the ticket that is not completed. (if any)
### Deliverable Essentials
For each ticket deliverable the following points must be addressed.
- Update the Readme file (Follow proper .md file format) If there are any changes related to Tech Stack, Versions, How to Setup Project on Local, How to run Unit Tests, Any Management Commands.
- For APIs create a folder named `docs` in the root directory. Add the updated postman collection there.
- Ticket must be tested aggressively by the developers before they submit or create a PR for it.

