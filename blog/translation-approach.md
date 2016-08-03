# Localization Approach

Localization refers to making a piece of software adapted to the *locale* of the user.  Often, this starts with translation, but it can also include aspects beyond strict translation.

For a site like Participedia, the localization approach is both critical and somewhat complex, as the work being catalogued is both global in nature and highly local (a democratic innovation emerges in a specific political and social context, and it's important to not assume that everything fits a common mold).

# Two tiers of localization

For version 3, the localization approach will focus on the  improvements the community has identified as critical to the success of the site, specifically making the project more accessible to non-English speakers.  This includes both translating the overall site, as well as facilitating and managing multiple translations of the case and method descriptions.

## Site Translation

By *site translation*, we are referring to the words on the website which are not part of the user-submitted data: the menus, the headings, the copy blocks that describe the project as a whole.  These words change rarely, and having them available in a wide range of languages should make the project as a whole accessible to a broad range of users.  These words aren't stored in the database itself.

The approach we will use for site translation is derived from the best practices from the Mozilla project, which has been localizing websites for a long time.  Specifically:

* All translated copy (all words that aren't trademarks for example) will be wrapped in components using the `react-intl` package.
* The translation management will be done using a standalone instance of Mozilla's `Pontoon` application.

This should allow skilled translators from the community to both find out about all strings ("bits of text in a specific context") that need to be translated for each desired language, and to distribute the work without needing specific technical skills.

Site content is also different in that we can guarantee that the original, "source" language is English (this is also the assumption that Pontoon makes).

### References

The reader is encouraged to read up about [Pontoon](http://mozilla-pontoon.readthedocs.io/en/latest/)  and [React-Intl](https://github.com/yahoo/react-intl)

### Deployment

[Participedia's pontoon instance](translate.participedia.xyz) is live (but not yet in use).  The [Source code](https://github.com/participedia/pontoon) is also available for inspection.

## Content Translation

Much of the content in Participedia of course is user submitted, whether that's case data or method data.  These texts change all the time, and must live in the database (they *are* the data).  This content is not highly structured (e.g. case descriptions are just chunks of limited HTML), but they exist in a well defined structure (as part of a specific case).  We will implement a simple set of specific UI tools to let users translate case and method titles and descriptions from any supported language to any other supported language.

The translations will be stored as part of the case and method data:

```
  case: {
    case_id: CaseID123
    title:
      { 'en-us': 'case title in english',
        'fr': 'case title en français',
        '…'
      },
    description:
      { 'en-us': 'case description in english',
        'fr': 'case description en français',
        '…'
      },
    ...
  }
  ```
