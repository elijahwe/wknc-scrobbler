# wknc-scrobbler
This is a program that uses the Spinitron and Last.fm APIs to take live songs from a radio station on Spinitron and "scrobble" it to a Last.fm account. I wrote this primarily to scrobble songs played on WKNC to [the station's Last.fm account](https://www.last.fm/user/wknc881). However, by using your own .env variables, the script can be used for other Spinitron stations and Last.fm accounts.
## Before you begin
You will need a Last.fm account and API application. If you have an account, you can create an API app [here](https://www.last.fm/api/account/create). For more information on authentication with the Last.fm API, look [here](https://www.last.fm/api/authentication).
You will also need admin access to the Spinitron web app for your station. If you do not have admin access yourself, you will need to contact an admin for your station and get their permission to use the API key for your app.
## Requirements
Python >=3.11: https://www.python.org/
.env file with the following values:
1. LASTFM_API_KEY: Found on your [Last.fm API accounts page](https://www.last.fm/api/accounts) under "API Key"
2. LASTFM_API_SECRET: Found on your [Last.fm API accounts page](https://www.last.fm/api/accounts) under "Shared Secret"
3. SPINITRON_API_KEY: Found on the [Spinitron automation and API page](https://spinitron.com/station/automation/panel) under "API Key"
## Installation
1. Clone the project from the repository
2. Navigate to cloned folder in a terminal
3. Execute 'pip install -r requirements.txt' to install packages
4. Execute 'python scrobbler.py --setup'
5. When prompted, authorize the application while logged into your Last.fm account, using the link provided
## Usage 
These steps are for after you have gone through the installation process and established a session key (using the --setup flag)
Any time you are listening to the radio station associated with your Spinitron account and want to scrobble what you are listening to, simply:
1. Navigate to the project folder in a terminal
2. Execute 'python scrobbler.py'
3. Once you have finished listening, terminate the program