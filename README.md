# Drupal Website Deployment Pantheon
# Step 1
terminus site:list
# Step 2
terminus site:create aquaeden-dev "My Aquascape site" "drupal-composer-managed"

# Step 3
terminus dashboard:view aquaeden-dev
# Step 4
terminus drush aquaeden-dev.dev -- site-install -y
# Step 5
terminus env:deploy aquaeden-dev.test
# Step 6
terminus env:deploy aquaeden-dev.live

