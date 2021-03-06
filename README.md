Kickster
========

[![Join the chat at https://gitter.im/nielsenramon/kickster](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/nielsenramon/kickster?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Kickster provides a basic Jekyll project setup packed with web best practises and useful optimization tools increasing your overall project quality. Kickster ships with automated and worry-free deployment scripts for GitHub Pages.

## Installation

Install the gem:

    gem install kickster

Execute gem and scaffold Kickster files:

    kickster new site_name

Setup your environment:

    bin/setup

## Development

Run Jekyll:

    bundle exec jekyll serve --watch

Used tools:
  - [Autoprefixer](https://github.com/postcss/autoprefixer)
  - [Bower](http://bower.io/)
  - [Circle CI](https://circleci.com/)
  - [Html-proofer](https://github.com/gjtorikian/html-proofer)
  - [Jekyll](http://jekyllrb.com/)
  - [Jekyll assets](https://github.com/jekyll/jekyll-assets)
  - [Jekyll Sitemap](https://github.com/jekyll/jekyll-sitemap)
  - [HTML5 Boilerplate](https://html5boilerplate.com/) (Influenced by)

*If you do not want the Kickster setup but just the deploy scripts then copy them from the `bin` folder.*

## Deploy to GitHub Pages

Run this in the root project folder in your console:

    bin/deploy

*Don't forget to enable your repository on [Circle CI](https://circleci.com/docs/getting-started) and update the `_config.yml` file!*

## Automated deployment with Circle CI

Automated deployment is by default not included in your Kickster generated Jekyll project. Please follow the steps below to include automated deployment.

*Note that changes will only deploy when your code is merged into master.*

#### 1. Copy the required automated deploy script

Copy the [automated](https://github.com/nielsenramon/kickster/blob/master/snippets/circle/automated) script inside the `/bin` folder of your project (make sure the file has execute permissions!).

#### 2. Update `circle.yml`

Replace your `circle.yml` file with [this](https://github.com/nielsenramon/kickster/blob/master/snippets/circle/circle.yml) one. And adjust the following 2 lines with your information:

    - USER_NAME: <your-github-username>
    - USER_EMAIL: <your-github-email>

#### 3. Enable Circle CI.

Make sure you enabled your repository on Circle CI. In Circle CI go to `Project settings > Checkout SSH Keys` and create a new User key. This is required to push to the GitHub repo from a script (permissions).

<img src="https://dl.dropboxusercontent.com/u/20823269/kickster-circle.jpg" alt="Screenshot of user key creating in Circle CI">

That's it, start pushing changes and enjoy your automated deployments from now on!

_Want to use Travis CI? [Click here](https://github.com/nielsenramon/kickster/tree/master/snippets/travis) to view all info on how to setup._

## Support

Need help with setting up Kickster? Join me on [Gitter](https://gitter.im/nielsenramon/kickster) and I help you out.

If you found a bug please report it in [GitHub issues](https://github.com/nielsenramon/kickster/issues).

## License

MIT License

## Contributing

1. Fork it ( https://github.com/[my-github-username]/kickster/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request

Big thanks to [@wouterw](https://github.com/wouterw) for helping out with his Ruby magic.
