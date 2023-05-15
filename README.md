The Recipes project is the application that powers my personal recipe blog at https://www.brunnerfamily.org.

---
# Description

The goal of the project was to create a simple blog that I could host for free and update fairly easily.

History of past attempts shows that I become disengaged with the application when the workflow becomes too complicated.  I want to be able to focus on the content and spend as little time as possible struggling with the process.

# Tooling

To achieve a minimal process, I used standard formats and familiar tools:
* Git for version management
* Markdown for content formatting
* Github for CI/CD

Additional tooling I found useful were:
* Jekyll for static site generation
* Netlify for automated deployments
* Obsidian for Markdown editing
* msys2 to make windows nicer


# Posting Content

The project itself is stored in Github.
1. To begin work, clone the github repository locally.
	1. `git clone https://github.com/jjbrunne/recipes.git`
	2. NOTE: Install git clients, generate and add ssh keys as appropriate
2. Create a branch to store your changes.
	1. `git checkout -b <branchname>`
3. Open the project folder as a new Vault in Obsidian
4. Add posts in the `_posts` directory
	1. All posts must have the `.md` file extension
	2. Posts must be named like `YYYY-MM-DD-<name>.md`
	3. NOTE: Obsidian will hide the `.md` extension
5. Build locally
	1. `jekyll build`
	2. 
6. Test locally 
	1. `jekyll serve`
	2. Browse to: http://localhost:4000
7. Deploy
	1. Commit your code
		1. `git add .`
		2. `git commit`
	2. Submit a PR
		1. `git push origin`
		2. Browse to Github (there will be a link in the previous command outputs)
		3. Create a PR
	3. Watch the tests to verify that Netlify built it successfully
		1. This will generate a preview deployment that you can review
	4. Browse to netlify and finalize the deployment
8. Verify the deployment by browsing to the site!
