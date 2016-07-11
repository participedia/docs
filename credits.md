Participedia is funded by a grant from Canada's [Social Sciences and Humanities Research Council](http://www.sshrc-crsh.gc.ca/).

Participedia's infrastructure currently uses a number of open source projects
for which we are very grateful, but a few deserve particular mention:

* Mozilla's [Pontoon](http://mozilla-pontoon.readthedocs.io/en/latest/) is making
localization by domain experts (rather than developers) possible.
* Facebook's [React](https://reactjs.com) simplified the front-end architecture
* [Leaflet](https://leafletjs.com) provides the mapping layer (with data from Open Street Maps and others)
* [Material-UI](https://material-ui.com) made it easy to build the layout
* [Harp](http://harpjs.com/) is a great way to make simple content sites like this site
* [ElasticSearch](https://github.com/elastic/elasticsearch) is a full-featured full-text search engine

Participedia's infrastructure currently uses the following service providers:

* [Auth0](https://auth0.com) provides the login system and user database, including social login,
* [Amazon Web Services](https://aws.amazon.com) host the ElasticSearch database,
* [Heroku](https://heroku.com) is the hosting provider for the Pontoon localization system,
* [Surge](https://surge.sh) is the hosting provider for the static assets (the website assets and this site),
* [Cloudflare](https://cloudflare.com) provides SSL and CDN (although the CDN isn't really needed as Surge has its own),
* [Google Analytics](https://analytics.google.com) provides usage metrics,
* [Mailgun](https://mailgun.com) provides email delivery, and
* [Github](https://github.com) provides open source collaboration infrastructure.
