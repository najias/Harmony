# Harmony
## What is this?
`Harmony` is a Page Object Model Test Framework, using Java, TestNG,Selenium WebDriver and Maven.

How To Create Page Object Model Test Framework?


	
	
    Step 0: Create a Maven Project
	`Steps:
	- Click file
	- New
	- Click Other
	- Expand Maven
	- Select Maven Project
	- Click Next
	- Click Next
	- Select maven-archetype-quickstart
	- Click Next
	- Enter Grour Id: yourCompanyName.yourProjectName
	- Enter artifactId: yourProjectName
	- Click Finish`
	
Step 1: CleanupStep
	
	- Delete Autogenerated Package from both
		- `src/main/java` and
		- `src/test/java`
	- Delete `JUnit` dependency from `pom.xml`
Step 2: Add new source folder

	- Right Click on `ProjectName`
	- Hover over `New`
	- Click on `Source Folder`
	- Enter Source folder name as `src/main/resources`
	- Click on `Finish`
Step 3: Push Project to GitHub

	Create Repo:
		- First Create a Git repo with exact same name as your project.
		- Copy that Git repo URL
	Export Project To Git:
		- Open Command line
		- cd to your project
		- execute `ls -al` and make sure there is no `.git` file
		- execute `git init` command to convert this project as git project
		- execute `ls -al` and make sure there you can see `.git` file
		- add `.gitignore` file to skipp gurbage data in `git add`, make sure there is no space before any of the file or folder name.
	Push Project:
		- `git add --all`
		- `git commit -m "initial commit"`
		- `git push --set-upstream gitRepoUrl master`
		- `git remote add origin gitRepoUrl` Note: Sets the new remote
		- `git remote -v` Note: Verifies the new remote URL
		- `git push -u origin master`
		- Make sure your project is in GitHub
	Create `develop` branch:
		- `git checkout -b develop`
		- `git push --set-upstream origin develop`
	Change Default branch to `develop`:
		- Visit git repo
		- Click on `Settings`
		- Click on `Branches` in left menubar
		- Click dropdown list of `Default branch`
		- Select `develop` branch
		- Click `Update`
		- Click on confirmation
	Create a `feature` branch:
		- `git checkout -b feature/feature-name`
		- `git push --set-upstream origin feature/feature-name`
Step 4: Create required packages

	- Within `src/main/java` create following packages
		- base
		- pages
		- listener
		- utils
	- Within `src/test/java` create following package
		- tests
	- Within `src/main/resources` create following packages
		- properties
		- suites
Step 5: Create required parent level classes

	- Within `base` package create following clases
		- Driver
		- PageBase
		- TestBase
		- SauceLabs
	- Within `utils` package create following clases
		- ReadProperties
	- Within `listener` package create following clases
		- EliteListener
Step 6: Create required properties/config files

	- Within `properties` package create following properties files
		- qa.properties
		- stg.properties
		- prod.properties
		- testRun.properties
		- saucelabs.properties
Step 7: Create a README file

	- Right Click of `ProjectName`
	- Hover over `New`
	- Click on `File`
	- Insert file name as `README.md`
	- Click `Finish`

