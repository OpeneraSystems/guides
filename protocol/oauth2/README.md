OAuth 2.0 Protocol
==================

A guide for setting up OAuth 2.0 credentials.

Google
------

Visit the [Google Dev Console](https://console.developers.google.com) and
create an API project.

For testing, set up the URLs as shown here
![Google OAuth2 Shot](https://github.com/OpeneraSystems/guides/blob/master/protocol/oauth2/GoogleOAuth2.png)

Ensure that the following APIs are enabled
![Google OAuth2 API Shot](https://github.com/OpeneraSystems/guides/blob/master/protocol/oauth2/GoogleOAuth2APIs.png)

Copy the example env file (.env.example) as env file (.env) and set the client id and secret to
the values in the Google console.
