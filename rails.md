# Rails

- The rails new command created a new Rails app named <the Site you want>. 
  
  **It creates lot of files and folders**

## The rails new command is the starting point of every Rails project.
  
- The bundle install command installed all the software packages needed by the new Rails app. 
  
  **These software packages are called gems and they are listed in the file Gemfile.**
  
## The rails server command 
  - started the Rails development server so that we could preview the app in the browser by visitinglocal host 
  
    **This development server is called WEBrick**
  
 # Controller 
  
  ## Request-Response Cycle 
  
  - The browser makes a request for the URL http://localhost:port
  
   - The request hits the Rails router in config/routes.rb. The router recognizes the URL and sends the request to the controller.
  
- The controller receives the request and processes it.
  
- The controller passes the request to the view.
  
- The view renders the page as HTML.
  
- The controller sends the HTML back to the browser for you to see.
  
- This is called the request/response cycle. 
  
  
 ## we need three parts to build a Rails app: a controller, a route, and a view. 
  
  - Let’s start here by creating a controller.
```
      In the terminal, type:

      rails generate controller Pages 
  
  ```
  
  
