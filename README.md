# The Vision Therapy Online App

Description
--

We had a dream of providing high-quality, cost-effective vision therapy that any patient could access at home. A group of web developers with a background in vision founded Vision Therapy Online like last week. More than 3 days later, we offer world-class products and services that connect patients with their eyecare professionals, as well as extend access to quality healthcare.

Technologies Used
--
<img src="http://www.myintervals.com/blog/wp-content/uploads/2011/12/postgresql-logo1.png" alt="postgressql" width="100" height="100">
<img src="http://blog.tryolabs.com/wp-content/uploads/2015/04/logo-578x270.png" alt="react" height="100">
<img src="https://encrypted-tbn2.gstatic.com/images?q=tbn:ANd9GcT29KTHfYpV97Xy0KfOjc83PerxvTXQ4KtbnDFuddt0I4xkji-9QDZG4w" alt="js" width="100" height="100">
<img src="https://winio.herokuapp.com/images/jquery.png" alt="jquery" width="100" height="100">
<img src="https://avatars0.githubusercontent.com/u/9338635?v=3&s=400" alt="jade" width="100" height="100">
<img src="https://cdn2.iconfinder.com/data/icons/nodejs-1/128/nodejs-128.png" alt="nodejs" width="100" height="100">
<img src="https://winio.herokuapp.com/images/passport.png" alt="passport" width="100" height="100">
<img src="https://winio.herokuapp.com/images/knex.png" alt="knex" height="100">
<img src="https://winio.herokuapp.com/images/mocha.png" alt="mocha" width="100" height="100">

Available Test Accounts on Heroku site
https://vision-therapy-app.herokuapp.com/
--
1. Doctor
  username: gunther, password: secret
2. Patient
  username: katie, password: password

Application Setup
--

To run the app:

  1. Install `npm` dependencies and create the `psql` database:

  ```sh
  npm install
  createdb project2_app
  ```

  2. Create a `.env` file with a random cookie secret:

  ```sh
  echo SECRET=$(node -e "require('crypto').randomBytes(48, function(ex, buf) { console.log(buf.toString('hex')) });") >> .env
  ```

  3. Run the `knex` migrations and seeds

  ```sh
  knex migrate:latest
  knex seed:run
  ```

  4. Start the app:

  ```sh
  nodemon
  ```

To run the tests:

  1. create test db:

  ```sh
  createdb project2_app_test
  npm test
  ```

The app is hosted on port 3000: [http://localhost:3000/](http://localhost:3000/)

