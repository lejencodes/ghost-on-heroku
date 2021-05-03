# [Ghost 3.X](https://github.com/TryGhost/Ghost) on [Heroku](http://heroku.com)

Ghost is a free, open, simple blogging platform. Visit the project's website at <http://ghost.org>, or read the docs on <http://support.ghost.org>.

[![GitHub issues](https://img.shields.io/github/issues/SNathJr/ghost-on-heroku)](https://github.com/SNathJr/ghost-on-heroku/issues)
[![GitHub forks](https://img.shields.io/github/forks/SNathJr/ghost-on-heroku)](https://github.com/SNathJr/ghost-on-heroku/network)
[![GitHub stars](https://img.shields.io/github/stars/SNathJr/ghost-on-heroku)](https://github.com/SNathJr/ghost-on-heroku/stargazers)
[![Deploy to Heroku](https://img.shields.io/badge/deploy%20to-heroku-6762a6)](https://heroku.com/deploy)

## Disclaimer

Forked from SNathJr/ghost-on-heroku


## Updating source code

Optionally after deployment, to push Ghost upgrades or work with source code, clone this repo (or a fork) and connect it with the Heroku app:

```bash
git clone https://github.com/snathjr/ghost-on-heroku
cd ghost-on-heroku

heroku git:remote -a YOURAPPNAME
heroku info
```

Then you can push commits to the Heroku app, triggering new deployments:

```bash
git add .
git commit -m "Important changes"
git push heroku master
```

Watch the app's server-side behavior to see errors and request traffic:

```bash
heroku logs -t
```

See more about [deploying to Heroku with git](https://devcenter.heroku.com/articles/git).

### Upgrading Ghost

This repository locks Ghost to the "last tested good version" using the standard `package-lock.json` file. If you want to upgrade Ghost on your own,
you will need to clone or fork this repo as described above. You will then be able to run:

```bash
npm upgrade ghost
git add package.json package-lock.json
git commit -m 'Update dependencies'
git push heroku master
```

If you're worried about packages beyond the root `ghost` server being outdated, you can check using `npm outdated`.

## Problems?

If you have problems using your instance of Ghost, you should check the [official documentation](http://support.ghost.org/) or
open an issue on [the official issue tracker](https://github.com/TryGhost/Ghost/issues). If you discover an issue with the
deployment process provided by _this repository_, then [open an issue here](https://github.com/snathjr/ghost-on-heroku).

## License

Released under the [MIT license](./LICENSE), just like the Ghost project itself.
