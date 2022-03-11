#Heroku Hosting

https://devcenter.heroku.com/articles/getting-started-with-nodejs?singlepage=true

##### my-notes

Add a file called Procfile to the backend project's root to tell Heroku how to start the application.
```
web: npm start
```

**Heroku configures application port based on the environment variable.**

### Node.js app deployment
Install heroku CLI from official site or npm package (npm install -g heroku)

1. Login to heroku `heroku login` 
2. Create heroku application using `heroku create`
3. Commit our code to our own repository
4. Move the code to heroku server using 
    - `git push heroku main` //'main' is our branch name
    - or `git push heroku HEAD:master` //as in our case code is at head of master branch 


### Frontend deployment (create-react-app)

1. create production build of the application `npm run build` 
2. copy the production build (the build directory) to the root of the backend repository and configure the backend to show the frontend's main page (the file build/index.html) as its main page.
![cmd](https://fullstackopen.com/static/3c4c5437683d0ea2e206c80b39766136/5a190/27ea.png)
3. config express.js middle to static middleware for display of static content `app.use(express.static('build'))`

