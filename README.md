# GitHubActionsLab-rutva

## Workflow 1 - Dependent Jobs
Runs when code is pushed to master.
Jobs run in this order: build → test → deploy
Each job waits for the previous one to finish using `needs`.

## Workflow 2 - Multi Platform Testing
Runs when a pull request is made to master.
Three jobs run at the same time on different operating systems:
Ubuntu, Windows, and macOS.

## Key Concepts
- `needs` = makes jobs run in order
- `runs-on` = chooses the operating system
- `uses` = runs a pre-built action like checkout

## Challenges
- YAML needs exact spacing (2 spaces per level)
- Windows uses different commands than Linux/Mac
