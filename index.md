# Welcome

This site documents the technical architecture for the third iteration of the
Participedia website.  It is primarily aimed at developers who are interested
in either contributing to the further development of the Participedia platform,
or who may want to create similar sites for other projects.

Because these technical docs inevitably use acronyms and jargon which the reader
may not be familiar with, we maintain a [glossary](glossary) with explanations behind
terms that may not be well understood.

The general architecture is a statically hosted single-page React app
that uses a third-party authentication provider and talks to the database
through a secured API gateway.

All of the code is available in our [github organization](https://github.com/participedia):

* the [front-end single-page app](https://github.com/participedia/frontend) that provides the website.
It is a so-called "single-page-app" using [React](https://reactjs.com).
* the [API gateway](https://github.com/participedia/api) which mediates access to the database,

All of the data is available through the [API endpoint](https://api.participedia.xyz). The API gateway implements the Swagger (*aka* OpenAPI) method to allow self-documentation
as well as easier use by many clients.

Participedia is built on a lot of software.  See our [credits](credits) page.

# Detailed Posts
