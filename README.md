# .NET Core 3.1 MVC Web App Quickstart
## Sample Code for Integrating with Okta using the Redirect Model

This repository contains a sample of integrating with [Okta](https://www.okta.com/) for authentication using the [Okta-Hosted authentication flow](https://developer.okta.com/docs/concepts/redirect-vs-embedded/) for a [.NET Core 3.1 Web App](https://developer.okta.com/docs/guides/aspnetcore3/main/).

Read more about getting started with Okta and authentication best practices on the [Okta Developer Portal](https://developer.okta.com).

This code sample demonstrates
* Configuring Okta
* Sign-in and sign-out
* Protecting routes
* Displaying user profile information from the ID Token

## Prerequisites

Before running this sample, you will need the following:

* [The Okta CLI Tool](https://github.com/okta/okta-cli#installation)
* An Okta Developer Account (create one using `okta register`, or configure an existing one with `okta login`) - take note of your Okta domain URL
* The [.NET Core 3.1 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/3.1).

To run this example, run the following commands:

```shell
git clone https://github.com/okta-samples/okta-dotnetcore3-webapp-quickstart.git
cd okta-dotnetcore3-webapp-quickstart
```

Restore the Nuget packages.

## Create an OIDC application in Okta

Grab and configure this project using `okta start dotnetcore3-webapp-quickstart`

Follow the instructions printed to the console.

## Run the example

Update `appsettings.json` with your Okta settings adding `Okta` as a top level property.

```json
"Okta": {
    "OktaDomain": "${CLI_OKTA_ORG_URL}",
    "ClientId": "${CLI_OKTA_CLIENT_ID}",
    "ClientSecret": "${CLI_OKTA_CLIENT_SECRET}"
  }
```

Start the app by running Visual Studio with IIS locally. Navigate to http://localhost:8080 (or whatever your localhost default settings are in your IDE) in your browser.

You should see a home page that prompts you to login. Clicking the **Log in** button will redirect you to the Okta hosted sign-in page (aka the redirect flow).

You can sign in with the same account that you created when signing up for your Developer Org, or you can use a known username and password from your Okta Directory - which can be created directly in the admin console.

> **Note:** If you are currently using your Developer Console, you already have a Single Sign-On (SSO) session for your Org.  You will be automatically logged into your application as the same user that is using the Developer Console.  You may want to use an incognito tab to test the flow from a blank slate.

## Helpful resources

* [Learn about Authentication, OAuth 2.0, and OpenID Connect](https://developer.okta.com/docs/concepts/)
* [Get started with NET Core](https://docs.microsoft.com/en-us/dotnet/core/get-started)
* [Authorization Code Flow](https://developer.okta.com/authentication-guide/implementing-authentication/auth-code)

## Help

Please visit our [Okta Developer Forums](https://devforum.okta.com/).
