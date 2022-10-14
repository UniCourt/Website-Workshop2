# Introduction to HTML and CSS - Workshop 2

Build your own website with our one-day workshop on understanding HTML and CSS. Learn how to,
   - Structure HTML elements. 
   - Use CSS to apply style to HTML elements. 
   - Create layouts using CSS flexbox.
   - Build your first website.

## Prerequisites
 - Machine/VM with linux
 - Docker  ( https://docs.docker.com/engine/install/ubuntu/#install-using-the-convenience-script )
 - Git     ( https://www.atlassian.com/git/tutorials/install-git#linux )
   - Create github account (https://github.com/signup)
   - Setting up SSH key with GitHub for Ubuntu
 (https://medium.com/featurepreneur/setting-up-ssh-key-with-github-for-ubuntu-cd8f2fabf25b)
 - VS code IDE ( https://linuxize.com/post/how-to-install-visual-studio-code-on-ubuntu-20-04/ )
 - Internet Connection and Chrome browser.

## Workshop environment setup 
 - Check if Git, Docker, and Docker Compose are installed in on the system. Open the terminal and run the following command
   ```
   mis@mispl-lap-31:~$ git --version
   git version 2.25.1

   mis@mispl-lap-31:~$ docker --version
   Docker version 20.10.17, build 100c701

   mis@mispl-lap-31:~$ docker compose version
   Docker Compose version v2.6.0

   ```
 - Open terminal and run following command to create a folder called workshop
    ```
    mkdir workshop
    ```
 - Navigate to the folder workshop and clone the from your personal repo using git
    ```
    cd workshop
    ```
 - First fork the repo and clone Website-Workshop2 repo & go inside Webiste-Workshop2 folder
    ``` 
    git clone git@github.com:{yourName}/Website-Workshop2.git
    cd Website-Workshop2
    ```
 - To open folder in VS code editor
    ```
    cd ~/workshop/Website-Workshop2
    code .
    ```
 - Bring up the Simple Blog Container
   ```
   sudo docker-compose -f simple-blog/docker-compose.yaml up

                           or
   
   sudo docker compose -f simple-blog/docker-compose.yaml up

   ```

 - open up http://localhost:8080/ in your browse

## What will you learn by the end of this workshop?
- By the end of this workshop, you will learn what is HTML and CSS.
- You will learn how to build website using HTML & CSS.
- You will learn how to use HTML Elements to structure the website.
- You will learn how to use CSS and apply presentation layer to the website.

## Schedule

| Time          | Topics
|---------------|-------
| 09:30 - 10:30 |  [`Revisit Docker Commands`](docker_commands.md)
| 10:30 - 10:45 |  [`Introduction to HTML`](html_intro.md)
| 10:45 - 11:00 |  [`Break`]
| 11:00 - 11:30 |  [`Introduction to HTML Contd.`](html_intro.md)
| 11:30 - 01:00 |  [`Introduction to CSS`](css_intro.md)
| 01:00 - 02:00 |  [`Break`]
| 02:00 - 05:00 |  [`Building Blog Website`](blog_html_css.md)
| 05:00 - 05:15 |  [`Q & A`]
| 05:15 - 05:30 |  [`Wrapping Up`]