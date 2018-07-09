drupal.develop
--

This is a Composer-based installer for the [Lightning](https://www.drupal.org/project/lightning) Drupal distribution. Welcome to the future!

## Project setup
```
# Clone repository
git clone git@github.com:weknowinc/drupal.develop.git

# Copy .env file
cp .env.dist .env

# Add hostname entry in your /etc/hosts file
127.0.0.1    drupal.develop

# Start containers
ahoy up
```

## Sync Project
```
# Switch develop branch
git checkout master

# Fetch latest changes
git fetch upstream

# Merge changes locally
git merge upstream/master

# Sync forked repo 
git push origin/master

# Download new dependencies
ahoy composer install

# Build Drupal site
ahoy drupal build:develop

# Create branch
git checkout -b BRANCH_NAME 

# Add file changes
git add -p

# Commit changes
git commit -m MESSAGE_SUBJECT

# Push code to repository
git push origin BRANCH_NAME
```

## Using Composer 
```
ahoy composer install

ahoy composer require drupal/MODULE_NAME

ahoy composer remove drupal/MODULE_NAME
```

## Export Configuration
```
# Using default drupal config system  
ahoy drupal config:export --no-interaction

# Using config_split
ahoy drupal config_split:export --no-interaction
```
