# Sky Theme for Hugo

Sky is a simple, minimal theme for Hugo

![Hugo Theme Sky](https://raw.githubusercontent.com/cfrome77/hugo-theme-sky/master/images/screenshot.png)

## Usage

Clone the repository to your hugo theme directory

```
mkdir themes
cd themes
git clone https://github.com/cfrome77/hugo-theme-sky
```

## Configuration

Put your profile picture under the `static` folder with the file name `profile.jpg`

Add these parameters to your `config.toml`:

```
[params]
  Name = "your_name"
  tagline = "your_industry_or_job_tagline"
  About = "info_about_you"
```

`name` will be displayed in navbar on left side next to the cloud icon.  

Optionally you can add any of these social networks to the \[params\] section.

```
  GnuPGFingerprint = "your_gpg_fingerprint"
  StackExchangeID = "your_stackexchange_id"
  StackOverflowID = "your_stackoverflow_id"
  GithubID = "your_github"
  GitlabId = "your_gitlab"
  BitbucketID = "your_bitbucket_id"
  TwitterID = "your_twitter"
  CodepenID = "your_codepen"
  LinkedInID = "your_linkedin"
  GoogleplusID = "your_googleplus"
  FacebookID = "your_facebook"
  InstagramID = "your_instagram"
  TelegramID = "your_telegram"
  Email = "your_email"
  Phone = "+1-201-555-0123"
  Mobile = "+1-201-555-0123"
  GoogleAnalytics = "your_google_analytics_id"
  SlackURL = "https://join.slack.com/..."
  PayPalMeID = "https://www.paypal.me/..."
  XingURL = "https://www.xing.com/profile/..."
  CvURL = "your_cv_url"
```

To add a menu item add `[[menu.header]]` item to `config.toml`. For example:

```
[menu]
  [[menu.header]]
    name = "blog"
    weight = 0
    url = "/post"
  [[menu.header]]
    name = "about"
    weight = 0
    url = "/about"
```

To add a submenu item add `[[menu.header]]` item with a parent parameter to `config.toml`. For example:

```
[menu]
  [[menu.header]]
    identifier = "post"
    name = "posts"
    weight = 0
    url = "/post"
  [[menu.header]]
    parent = "post"
    name = "All Posts"
    url = "/post"
  [[menu.header]]
    parent = "post"
    name = "categories"
    url = "/categories"
  [[menu.header]]
    parent = "post"
    name = "tags"
    url = "/tags"
```

To enable disqus comments add `disqusShortname` to your `config.toml`.

You can turn off disqus comments per page by adding `nocomments = true` to the front matter.

## License

Sky is licensed under the [MIT License](LICENSE)
