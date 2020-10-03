# This repository contains postman collections for the REST APIs made for TIA.

## Structure
For each differnt postman collection, there will be a separate folder.
Each folder will contain one `collection.json` file and one Example `env` file.
`collection.json` file will have all the APIs defined in a Postman recognizable format. This file is 
exported from the Postman UI. Similarly `example.env.json` file has all the environment variables 
which are used in the REST APIs defined in `collections.json`.

## How to sync and export
General rule to follow to use this repository is to at a time work on the json configuration in the repoistory or work in the UI directly.
When you want to change something in the file, do those changes directly in the file and then export the collection in Postman UI. You can rename the old collection as a backup collection and work on this newly imported one.
When you want to make changes in the postman collection from the UI, make sure those changes are then imported in the `collection.json` file manually without changing the file name. This applies for example env file too.
Always double check for secrets/password/confidential information being imported in the repository. Try to redact it wherever possible and keep the confidential information in the environment variable. You'll have to manually download the updated json file for environment, redact sensitive info and replace it with the `example.env.json` file.

## Managing enviornmnet
Use `example.env.json` file as the blueprint for all your environments. Import it in the Postman UI and modify the values.
Typical example environments could be:
 - TIA Dev Mod User
 - TIA Prod Non Mod User
 - TIA Local Mod User

For production environment and mod user, find the environment json on the slack: 
https://ti-app.slack.com/archives/CE68JUXPC/p1601740894000500
