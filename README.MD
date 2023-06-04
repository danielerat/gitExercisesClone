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
