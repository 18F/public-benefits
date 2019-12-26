# 18F’s human services portfolio

This repo houses the site for the portfolio, which itself is a collection of work in the human services space led by teams within GSA's [Technology Transformation Service (TTS)](https://www.gsa.gov/about-us/organization/federal-acquisition-service/technology-transformation-services) (which includes [18F](https://18f.gsa.gov/)).

## Contents

Our site is powered by the [Jekyll static site generator](https://jekyllrb.com/).

The basic structure is:

```
.
├── index.md  # the landing page
├── about.md  # more about the portfolio
├── README.md # this file
├── _layouts  # templates for site pages
├── _site     # where Jekyll builds the site; do not edit
└── assets    # CSS, JS, images, fonts
```

## Running the site

### Installation

Using the Terminal, first get a copy of the source code:

```bash
git clone https://github.com/18F/human-services.git
cd human-services
```

Now, ensure that you have the correct version of [Ruby](https://www.ruby-lang.org/en/) installed, which is tracked in `.ruby-version`. We recommend using [`rbenv`](https://github.com/rbenv/rbenv) to manage Ruby versions on your system. If you have not previously installed it, [`Homebrew`](https://brew.sh/) is a friendly way to do so.

```bash
rbenv install $(cat .ruby-version)
```

With Ruby installed, get `bundler` to manage dependencies and run Jekyll:

```bash
gem install bundler
```

Now, install the site's dependencies, which are tracked in `Gemfile`:

```bash
bundle install
```

Finally, build and run the site:

```bash
bundle exec jekyll serve
```

Navigate to http://localhost:4000, and you should see the site running.

### Deploying

The site is deployed using the [Federalist](http://federalist.18f.gov/) platform, and automatically deploys from the `release` branch.

To get access to the site in the Federalist:
- Head to #federalist-support on the TTS Slack and ask for your GitHub account to be given access to Federalist
- Log in to the [Federalist app](https://federalistapp.18f.gov/) using that GitHub account
- Click the button to "Add site"
- Add this repo: "https://github.com/18F/human-services"

This will allow you to see the build progress, easily find preview sites for branches, and configure custom URLs.

## Contributing

See [CONTRIBUTING](CONTRIBUTING.md) for additional information.

## Public domain

This project is in the worldwide [public domain](LICENSE.md). As stated in [CONTRIBUTING](CONTRIBUTING.md):

> This project is in the public domain within the United States, and copyright and related rights in the work worldwide are waived through the [CC0 1.0 Universal public domain dedication](https://creativecommons.org/publicdomain/zero/1.0/).
>
> All contributions to this project will be released under the CC0 dedication. By submitting a pull request, you are agreeing to comply with this waiver of copyright interest.
