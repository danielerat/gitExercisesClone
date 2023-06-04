# Git Bundles.

## Bundle 1.

### Exercise 1

```bash
# Initialize git.
git init

# Create our Readme File.
echo "# Git Bundles." > README.md

# Staging everything
git add .

# Commiting our changes
git commit -m "Adding The Readme.md File"

# Renaming our branch
git branch -M main

# Adding our remote branch
git remote add origin https://github.com/danielerat/gitExercises.git

#pushing our changes.
git push -u origin main

# Creating and switching to the dev branch
git switch -C dev
    # git branch
        # Output
            # * dev
            #   main
# Doing the same for test
git switch -C test

# switching to the dev branch
git switch dev

# Deleting our test branch
git branch -d test
    # Output: Deleted branch test (was d80a34a).
```

### Exercise 2

```bash
# Creating our home page
echo "" > home.html

# Stashing our home page
git stash push -am "Home Page"


# Creating our about page
echo "" > about.html

# Stashing our home About
git stash push -am "About Page"

# Creating our Team Page
echo "" > team.html

git stash push -am "Team Page"
	# git stash list
		# Output
		# stash@{0}: On dev: Team Page
		# stash@{1}: On dev: About Page
		# stash@{2}: On dev: Home Page

#stash pop the about page
git stash pop 1
# Stash pop the home page
git stash pop 1

# pushing the dev branch.
git push -u origin dev

# Poping the team page.
git stash pop 0

#removing the team page.
git reset --hard

```

## Bundle 2.

### Exercise 1

```bash
# create new branch
git switch -C ft/bundle-2

echo "" > services.html

git push -u origin ft/bundle-2
```

### Exercise 2

```bash
git switch -C ft/service-redesign

git add services.html

git commit -m "Redesigning the service page"

git switch main

git add service.html

git commit -m "Additional changes to the service page"

git push
```
