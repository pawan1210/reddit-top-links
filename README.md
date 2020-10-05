# Vouch Assignement
This is a submission for the assignment by Vouch Insurtech for the Position of Software Engineer. 

The app provides insights abouts links shared in the Subreddits that you follow.
It allows you to see the top contributors who shared different links, along with the top domains whose links were shared and also lists the posts with the said links.


## Pre-requisites (to run App locally)
- Python 3.6 and pip should be preinstalled
- Twitter developer Credentials

## How to Run Locally
- Clone Repository
- Install the requirements using ```pip install -r requirements.txt```, in the repository folder
- Create a .env file inside the reddittoplinks folder, the .env file should contain the following
```
CLIENT_ID=<Your Reddit Client ID>
CLIENT_SECRET=<Your Reddit Client Secret>
```
- Run ```python manage.py makemigrations```
- Run ```python manage.py migrate```
- Finally, Run ```python manage.py runserver```, in the repository Folder
- The Server should start at ```localhost:8000/```.

## How to Use?
- Go to Homepage and Press Login
- Approve the App to see data from your account
- You will be redirected to the dashboard which will show all the required information.

## Database Schema
```
class Posts(models.Model):
    username = models.CharField(max_length=100, blank=False)
    author = models.CharField(max_length=100, blank=False)
    text = models.TextField(blank=False)
    title = models.TextField(blank=False)
    link = models.URLField(max_length=400, blank=False)
    subreddit = models.URLField(max_length=400, blank=True)
```