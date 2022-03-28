# Apps4Av

This github repository hosts the source for the Apps4Av
website. Public contributions are encouraged, especially in the form
of blog posts and page editing.

-   The primary goal of this site is to support the Avare (and
    aviation) community
	-   **Avare app documentation** is a high priority
	-   Posts should be of general interest to the Avare community
	-   Posts should minimize self-promotion and declare conflicts of interest
	-   Posts should use appropriate citations and attribution (including links)

## To contribute

To contribute, please submit patch requests by:

1.  [Cloning this
    repo](https://github.com/avare-docs/avare-docs.github.io/tree/pending),
    preferably the **pending** branch or create your own local branch
	-   You may also edit the **pending** branch directly on github!
1.  Edit in your local branch.
	-   Create new pages or edit files using github markdown syntax
1.  Commit your changes
1.  Push your branch back as a public branch
1.  Submit a merge request

### Local preview

-   The site is built with [Jekyll](https://jekyllrb.com/) on [GitHub
    Pages](https://pages.github.com/)
-   Within your local branch, execute the following commands (Linux)

```console
foo@bar:~$ gem install bundler jekyll
foo@bar:~$ bundle update
foo@bar:~$ bundle exec jekyll serve --livereload
```

-   This last command will serve your local version of the website,
	typically on [http://localhost:4000](http://localhost:4000)

## Alternative forms of submission

We recognize that some community members are **uncomfortable with the
use of git**.  You may send submissions by email.


## Please:

-   Strive to be concise and precise
-   Use graphics rather than text where possible
-   Add authorship information and attribution
-   Avoid redundancy
-   Add tags and categories to the file [yaml](https://jekyllrb.com/docs/front-matter/) header info
