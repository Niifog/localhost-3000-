# localhost-3000-
How I resolved Localhost:3000 issue on rails

This was how i resolved the issue of the localhost not opening on localhost:3000

**C:\rubytester>rails s
=> Booting Puma
=> Rails 5.1.7 application starting in development
=> Run `rails server -h` for more startup options
*** SIGUSR2 not implemented, signal based restart unavailable!
*** SIGUSR1 not implemented, signal based restart unavailable!
*** SIGHUP not implemented, signal based logs reopening unavailable!
Puma starting in single mode...
* Version 3.12.1 (ruby 2.3.3-p222), codename: Llamas in Pajamas
* Min threads: 5, max threads: 5
* Environment: development
* Listening on tcp://localhost:3000**

This could be because the localhost:3000 is already in use, so i have to change it to

bundle exec puma -C config/puma.rb -b tcp://127.0.0.1:3001

Niifog
