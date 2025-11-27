## WSL Setup

- Open your WSL (we use Ubuntu as the distro)
    `wsl -d Ubuntu`
    - You’ll see that you’re in an mnt directory:
        > !
- Go to your home directory
    - `cd ~`
- Create a directory for your Laravel development
    - `mkdir laradev`
- Navigate to that directory
    - `cd laradev`

> !

## Setting up a Laravel Project

- Create a new project (type or copy):
    - `curl -s https://laravel.build/m7prog-laravel | bash`

    > HINT: You can change m7prog-laravel when starting other projects
- You should have a password for your Android user (if not, see `wsl change pw.md`)
    - Enter it when prompted for [sudo] password...
    > !

## Sail Up

- Go to your project directory:
    > !
    > It’s now m7prog-laravel

- Type now `vendor/bin/sail up`

- You’ll see:
    > !

## Check

- Your Docker should now be running; verify that you see this:
    > !

## Breeze, NPM, etc.

- Open the exec terminal of your Laravel Docker container:
    > !
    
- Install Breeze:
    - `composer require laravel/breeze --dev`
    - `php artisan breeze:install`
    - `php artisan migrate`

- Install NPM:
    - `npm install`
- Test:
    - `npm run dev`
    - You’ll see:
    > !
    
- Open your browser; you should now see Laravel with Breeze
    > !

## Files in Visual Studio Code

- All our files are now in the Linux file system of WSL. How do we access them?
    - Open Windows Explorer
        - In the address bar, type:
            - `\\wsl.localhost\Ubuntu\home\android`

        - There you’ll find our directory
            > !
- Open that directory in Visual Studio Code
- Now you can start coding!