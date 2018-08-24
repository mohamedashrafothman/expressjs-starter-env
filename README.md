# Express Starter Env
Inspired by [Hackathon Starter](https://github.com/sahat/hackathon-starter) & [Aqua](https://jedireza.github.io/aqua/), this project is a more simplified boilerplate application with some basic examples of user authentication with [Passport](https://github.com/jaredhanson/passport), [OAuth2](https://oauth.net/2/) using Passportjs OAuth Strategies, and simple permission system via an [Permission](https://www.npmjs.com/package/permission).

## Services
This application has been designed to use the free tiers of these services to get a live development environment up and running with minimal effort as a starter env. In order to deploy this application as-is, you will need accounts from these services:

* [Heroku](https://signup.heroku.com/) - hosts the application.
* [Mailtrap](https://mailtrap.io) - Mailtrap is a solution that allows testing email notifications without sending them to the real users of your application. It also lets you view all your emails online, forward them to your regular mailbox, share with the team and more!
* [Facebook Developer account](https://developers.facebook.com/) - For OAuth purpose.
* [Github Developer account](https://developer.github.com/) - For OAuth purpose.
* [Google Developer account](https://console.developers.google.com) - For OAuth purpose.


## Heroku Setup

* Fork this project to your own GitHub account.
* Sign up for or log into a Heroku account and create a new app.
* On your app, change the Deployment Method on the Deploy tab to "GitHub."
* Search for your forked project and connect your repository.
* On the Resources tab, search for "mLab" under Add-ons.  Add the mLab add-on, choosing the free sandbox plan. This will automatically add the environment variable for `MONGODB_URI`.
* On the Settings tab, add [the necessary environment variables](#environment-variables).
* On the Deploy tab, perform a manual deployment of the master branch.  Once the deployment is complete, you should be able to open your app.


## Environment Variables
The below environment variables are needed to get the application up and running.

* `GOOGLE_CLIENT_ID` - google developer account id.
* `GOOGLE_CLIENT_SECRET` - google developer account secret.
* `GOOGLE_CALLBACK_URL` - OAuth redirect after success login using Google.
* `FACEBOOK_CLIENT_ID` - Facebook developer account id.
* `FACEBOOK_CLIENT_SECRET` - Facebook developer account secret.
* `FACEBOOK_CALLBACK_URL` - OAuth redirect after success login using Facebook.
* `GITHUB_CLIENT_ID` - Github developer account id.
* `GITHUB_CLIENT_SECRET` - Github developer account secret.
* `GITHUB_CALLBACK_URL` - OAuth redirect after success login using Github.
* `MONGODB_URI` - this only needs to be added manually if you are A) working locally or B) using your own mLab instance that you didn't provision through Heroku.
* `PORT` - Port for starting your application on.
* `SESSION_SECRET` - Sessions secret.
* `NODE_ENV` - Node enviroment mode, it can be development or deploy, errorhandler package depend on development env.
* `MAIL_HOST` - Nodemailer mailer Host.
* `MAIL_PORT` - Nodemailer mailer port.
* `MAIL_USER` - Nodemailer email address from which you will send notification emails.
* `MAIL_PASS` - Nodemailer password for mailer user.
* `AVATAR_FIELD` - avatar field name.
* `AVATAR_BASE_URL` - Multer avatar base url, the base url for storing avatar images.
* `AVATAR_STORAGE` - Multer avatar Storage Url to store avatar images. 
* `ADMIN_SECRET` - Admin registeration sectret, this can be passed to any one for register as an admin, the server will check if his input equal to this secreet, then he will be an admin.
* `MINIMUM_PASSWORD_LENGTH` - the minimum length of user passwords.
* `PASSWORD_HASH_ROUNDS` - the number of rounds for bcrypt to apply its hashing algorithm.  The higher the rounds, the more secure the password is, but the more computing power is needed to hash passwords.  [Choose a number that best balances security and performance](http://security.stackexchange.com/questions/3959/recommended-of-iterations-when-using-pkbdf2-sha256/3993#3993).
* `PASSWORD_RESET_TIME_LIMIT_IN_HOURS` - the amount of time a user has to reset their password if they go through the "Forgot Password" process.


## License
(The MIT License)

Copyright (c) Mohamed Ashraf

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.