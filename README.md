# opensheet

A free API for getting Google Sheets as JSON.

**Documentation blog post:** [benborgers.com/posts/google-sheets-json](https://benborgers.com/posts/google-sheets-json)

**If you have questions:** [benborgers.com/contact](https://benborgers.com/contact)

## Self-hosting

_This section is only necessary if you want to fork opensheet or host your own instance of it on [Vercel](https://vercel.com). If you don’t want to deal with that, you’re welcome to use my hosted instance at `opensheet.vercel.app`._

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fbenborgers%2Fopensheet&env=GOOGLE_SERVICE_ACCOUNT&envDescription=You%20can%20find%20instructions%20for%20populating%20the%20environment%20variables%20in%20opensheet%E2%80%99s%20readme.%20&envLink=https%3A%2F%2Fgithub.com%2Fbenborgers%2Fopensheet)

If you host opensheet in your own Vercel account or make a fork, you’ll need to get your own Google Sheets API credentials:

1. Go to the [Google Cloud Console](https://console.cloud.google.com) and create a new project from the top navigation bar.
2. Search for “Google Sheets API” and enable it.
3. On the left bar, go to Credentials and click “Create Credentials” → “Service account”. _Service accounts_ are Google’s concept for a Google account that you can control programmatically.
4. Fill in any reasonable name, and skip the next two optional steps. Click “Done” to create the set of credentials, which will allow you to access Google Sheets using the API.
5. Click on this newly created service account, and then go to the “Keys” tab. Create a key of type JSON.
6. A JSON file containing the service account’s credentials will be downloaded. Open up that file, and copy its entire contents. **You should paste this whole thing into the `GOOGLE_SERVICE_ACCOUNT` environment variable on the Vercel dashboard for your own deployment of opensheet.**

## Local development

Install the [Vercel CLI](https://vercel.com/cli), and then run:

```sh
vercel dev
```
