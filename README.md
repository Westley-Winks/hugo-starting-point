# Template for basic portfolio using Hugo

Easy starting point for a Hugo website. No setting up complicated themes and easy to change and modify. Contains scripts for automatically pulling GitHub projects but can also be used for a blog or anything else. Demo is located [here](https://westley-winks.github.io/hugo-starting-point/).

Built using [Goa theme](https://github.com/kaapiandcode/hugo-goa) and some code from [open source Twitter](https://opensource.twitter.dev/).

## Usage
1. First, clone this repo to your machine:
`git clone https://github.com/Westley-Winks/hugo-starting-point.git`

2. Then, go into `config.toml` and change parameters. Specifically, change the following:
- baseURL
- author
- title
- intro
- description
- uncomment whichever social accounts and add in the corresponding usernames
- copyright

3. Navigate to `static/img/` and replace `headshot.jpg` with a photo of yourself.

4. Change `repos-to-include.txt` to your GitHub repos that you want to display on the projects page

5. Create file called `.env` with these keys:
- GH_USERNAME=\<your GitHub username>
- OAUTH_TOKEN=\<your personal access token>

OAUTH_TOKEN is your Personal Access Token for GitHub

6. Run `fetch_projects.py`:
`python scripts/fetch_projects.py`

7. Check it out by running `hugo server`!

8. Deploy.
It is currently setup for GitHub Pages. A GH Action builds and deploys whenever code gets pushed to the `main` branch. Another Action is on cron and will run `fetch_projects.py` and rebuild the site once a week.