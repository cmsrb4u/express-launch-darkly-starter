## Creating customized user experiences with Express JS and LaunchDarkly segment targeting

Example [Express](https://expressjs.com/) app that can be integrated with [LaunchDarkly's Node.js server side SDK](https://docs.launchdarkly.com/sdk/server-side/node-js).

### How to get started:

Log in to your [LaunchDarkly](https://launchdarkly.com/) account (or [sign up for a free one here](https://launchdarkly.com/).) Copy your SDK key. Paste the key into the `.env` file.

With this setup, the LaunchDarkly SDK can access the credentials locally but you won’t accidentally commit them to source control and compromise your security.

Install dependencies using the following command:

`npm install`

Run the server:

`npm start`

The code defines a route for the root URL ("/") that:
Creates a LaunchDarkly context object with user information (kind, key, email).

Uses the ldClient.variation() method to evaluate a feature flag ("show-student-version") for the given context.

Based on the feature flag value, redirects the user to either student.html or enterprise.html.

If you load http://127.0.0.1:3000/ in the browser, you should see a web page accordingly.

