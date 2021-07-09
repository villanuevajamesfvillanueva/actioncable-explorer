## redis:
    installation:
        switch to superuser
        sudo apt update && apt upgrade
        sudo apt install redis-server


    in config/cable.yml, edit development:
        development:
            adapter: redis
            url: redis://localhost:6379/1

    run:
        sudo service redis-server start

    in Gemfile, add:
        gem 'redis'
    
    run:
        bundle install