[![Python 3.7](https://img.shields.io/badge/python-3.7-blue.svg)](https://www.python.org/downloads/release/python-360/)

# Cavalcade
A python utility for automating video uploads to youtube using the YouTube Data API.


## Setup
You will need to register your application with Google in order to create Oauth2 credentials that will allow you to programmatically access the YouTube Data API. 

Documentation:

* [Getting Started with YouTube Data API](https://developers.google.com/youtube/v3/getting-started)

* [Register an application with Google](https://developers.google.com/youtube/registering_an_application)

* [Create Oauth2 Credentials](https://developers.google.com/identity/protocols/OAuth2InstalledApp)

Create a file in the same directory as `cavalcade.py` named `client_secrets.json`. The structure of the file should be:

```json
{
  "web": {
    "client_id": "some-unique-id.apps.googleusercontent.com",
    "client_secret": "some-secret-issued-by-google",
    "redirect_uris": [],
    "auth_uri": "https://accounts.google.com/o/oauth2/auth",
    "token_uri": "https://accounts.google.com/o/oauth2/token"
  }
}
```

 Now paste the `client_id` and `client_secret` from your OAuth2 credentials into the file and save it.

## Installation

Clone this repository with `git`:

```
$ git clone https://github.com/terciero/cavalcade.git
```

## Usage
Cavalcade currently exists as a standalone Python script. Future releases will include migration to a first class CLI architecture and releases in binary form for both Windows and Linux.


Windows command line:
```
python upload_video.py --file="\path\to\video\test-vid.wmv" ^
                       --title="Sample Video" ^
                       --description="Awesome example video" ^
                       --keywords="streaming,Destiny" ^
                       --category="24" ^
                       --privacyStatus="public"
```

Powershell:
```
python upload_video.py --file="\path\to\video\test-vid.wmv" `
                       --title="Sample Video" `
                       --description="Awesome example video" `
                       --keywords="streaming,Destiny" `
                       --category="24" `
                       --privacyStatus="public"

```

Bash:
```
python upload_video.py --file="\path\to\video\test-vid.wmv" \
                       --title="Sample Video" \
                       --description="Awesome example video" \
                       --keywords="streaming,Destiny" \
                       --category="24" \
                       --privacyStatus="public"
```

## Development

For working on `cavalcade`, you'll need Python >= 3.7.

Create a virtualenv:

```
python -m virtualenv env
```

Activate the virtualenv:

Windows:

```
.\env\Scripts\activate
```

Linux:

```
source env/bin/activate
```
