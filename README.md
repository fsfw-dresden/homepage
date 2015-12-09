fsfw-dresden/homepage
=====================

This repo powers our homepage. On pushing to the remote
<git@github.com:fsfw-dresden/homepage.git> the template-engine will be
run to assemble the sites and copy them to the dir served by the
webserver.

All pushed branches that are not blacklisted are built and the results
are available at <http://staging.fsfw-dresden.de/branch-name.branch/>.
Slashes within the branch name are possible.

Example for the branch `staging-test`: http://staging.fsfw-dresden.de/staging-test.branch/.

The branch `master` is built and available at
<http://fsfw-dresden.de/>.

To push a local branch for the first time use: `git push origin my_new_branch`.


Local preview
-------------

One can also build the homepage locally by using the tools found in
the homepage-build repository
<https://github.com/fsfw-dresden/homepage-build>. The build process is
described in the README there. Then one can point a browser to
`file:///path/to/homepage/checkout/docroot` to inspect the results.

Short guide on editing
----------------------

We use the [jinja2](http://jinja.pocoo.org/docs/dev/) templating
language to construct the site. `templates/base.html` provides the
skeleton shared by all pages. If you add navigation elements, add them
here (and you will only have to add them once).

The pages the root of this repo are the individual pages, you can edit
the stuff between `{% block content %}` and `{% endblock %}` like
ordinary HTML. To set the title for an individual page use `{% set
title = "Title" %}` (compare `programm.html`).


See also
--------
https://wiki.fsfw-dresden.de/doku.php?id=orga:interne-infrastruktur:homepage