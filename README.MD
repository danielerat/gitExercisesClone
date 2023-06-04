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

## Bundle 3

### Exercise 1

```bash
git switch -C ft/team-page

echo "" > team.html

git add .

git push -u origin ft/team-page

git switch main

git switch -C ft/contact-page

git switch ft/team-page

git log --oneline --all --graph
	#output
	  #* cd56139 (HEAD -> ft/team-page, origin/ft/team-page) Addi..

git switch ft/contact-page

git add .

git commit -m "Changes after picking cherries" #😂

git push -u origin ft/contact-page

# Faq Branch
git switch -C ft/faq-page
git add .
git commit -m "Adding the faq page"
git push -u origin ft/faq-page

git revert cd56139

git commit .
git commit -m "Reverting from the ft/team commit"
git push

```

### Exercise 2

```bash
git switch -C ft/home-page-redesign
git add .
git commit -m "Redesign the home page"
git push

git switch ft/home-page-redesign
git rebase main
git add .
git commit -m "Commit after rebasing from the main branch"
git push
```

## Bundle 4

### Exercise 1

```bash

git remote add git-copy https://github.com/danielerat/gitExercisesClone.git
	# git remote
		# git-copy
		# origin
git add home.html
git commit -m "Changes on the home page"

git push origin
git push git-copy
```
