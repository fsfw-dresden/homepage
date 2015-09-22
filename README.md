fsfw-dresden/homepage
=====================

This repo powers our homepage. On pushing to the remote
<ssh://git@rosetta.fsfw-dresden.de/infra/homepage> the template-engine
will be run to assemble the sites and copy them to the dir served by
the webserver.

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
