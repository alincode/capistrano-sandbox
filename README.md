# Capistrano Sandbox

**create new capistrano sandbox step**

```
rails new .
bundle install
gem install mysql2
```

**Install Capistrano, cap install STAGES=staging,production**

`cap install`

**set up config**

```
cp config/deploy/staging.rb.example config/deploy/staging.rb
vi /home/ubuntu/cap/shared/config/database.yml
vi /home/ubuntu/cap/shared/config/secrets.yml
```

**list all available tasks**

`bundle exec cap -T`

**Check commands**

```
cap staging deploy:check                   # Check required files and directories exist
cap staging deploy:check:directories       # Check shared and release directories exist
cap staging deploy:check:linked_dirs       # Check directories to be linked exist in shared
cap staging deploy:check:linked_files      # Check files to be linked exist in shared
cap staging deploy:check:make_linked_dirs  # Check directories of files to be linked exist in shared
```

## commands
```
cap deploy                         # Deploy a new release
cap deploy:check                   # Check required files and directories exist
cap deploy:check:directories       # Check shared and release directories exist
cap deploy:check:linked_dirs       # Check directories to be linked exist in shared
cap deploy:check:linked_files      # Check files to be linked exist in shared
cap deploy:check:make_linked_dirs  # Check directories of files to be linked exist in shared
cap deploy:cleanup                 # Clean up old releases
cap deploy:cleanup_rollback        # Remove and archive rolled-back release
cap deploy:finished                # Finished
cap deploy:finishing               # Finish the deployment, clean up server(s)
cap deploy:finishing_rollback      # Finish the rollback, clean up server(s)
cap deploy:log_revision            # Log details of the deploy
cap deploy:published               # Published
cap deploy:publishing              # Publish the release
cap deploy:revert_release          # Revert to previous release timestamp
cap deploy:reverted                # Reverted
cap deploy:reverting               # Revert server(s) to previous release
cap deploy:rollback                # Rollback to previous release
cap deploy:set_current_revision    # Place a REVISION file with the current revision SHA in the current release path
cap deploy:started                 # Started
cap deploy:starting                # Start a deployment, make sure server(s) ready
cap deploy:symlink:linked_dirs     # Symlink linked directories
cap deploy:symlink:linked_files    # Symlink linked files
cap deploy:symlink:release         # Symlink release to current
cap deploy:symlink:shared          # Symlink files and directories from shared to release
cap deploy:updated                 # Updated
cap deploy:updating                # Update server(s) by setting up a new release
cap doctor                         # Display a Capistrano troubleshooting report (all doctor: tasks)
cap doctor:environment             # Display Ruby environment details
cap doctor:gems                    # Display Capistrano gem versions
cap doctor:servers                 # Display the effective servers configuration
cap doctor:variables               # Display the values of all Capistrano variables
cap install                        # Install Capistrano, cap install STAGES=staging,production
```

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
