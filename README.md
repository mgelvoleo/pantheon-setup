# Drupal Website Deployment Pantheon
# Step 1
terminus site:list
# Step 2
terminus site:create aquaeden-dev "My Aquaeden official Site"
# Step 3
terminus site:create aquaeden-dev "My Aquascape site" "drupal-composer-managed"

# Step 4
terminus dashboard:view aquaeden-dev
# Step 5
terminus drush aquaeden-dev -- site-install -y
# Step 6
terminus drush aquaeden-dev.dev -- site-install -y
# Step 7
terminus env:deploy aquaeden-dev.test
# Step 8
terminus env:deploy aquaeden-dev.live

