## Buildme

* [Website](https://maurolepore.github.io/2020-05-12-rice/)
* [How to customize your website](https://github.com/carpentries/workshop-template#customizing-your-website)
* [Customize your website](https://github.com/maurolepore/2020-05-12-rice/edit/gh-pages/index.md)
* [Original carpentries/workshop-template](https://github.com/carpentries/workshop-template)

## TODO

* [x] Link website from repo
* [ ] Customize website
* [ ] Share website URL with workshop organizers
* [ ] Share website URL with workshop the [Carpentries][email]. 
* [ ] If this is a self-organised workshop, [fill in the self-organized workshop form][self-organized-workshop-form].

## Legacy

## Customizing Your Website

1.  Go into your newly-created repository,
    which will be at `https://github.com/your_username/YYYY-MM-DD-site`.
    For example,
    if your username is `gvwilson`,
    the repository's URL will be `https://github.com/gvwilson/2016-12-01-miskatonic`.

3.  Ensure you are on the gh-pages branch by clicking on the branch under the drop 
    down in the menu bar (see the note below):

    ![](fig/select-gh-pages-branch.png?raw=true)

3.  Edit the header of `index.md` to customize the list of instructors,
    workshop venue, etc. 
    You can do this in the browser by clicking on it in the file view on GitHub
    and then selecting the pencil icon in the menu bar:

    ![](fig/edit-index-file-menu-bar.png?raw=true)
    
    Editing hints are embedded in `index.md`,
    and full instructions are in [the customization instructions][customization].
    
4.  Edit `_config.yml` to customize certain site-wide variables, such as: `carpentry` (to tell us which carpentry workshop this is), `title` (overall title for all pages), `workshop_repo` (the URL of the workshop repository on GitHub) and `workshop_site` (the repository's GitHub Pages URL).

    Editing hints are embedded in `_config.yml`,
    and full instructions are in [the customization instructions][customization].
    
5. Edit the `schedule.html` file to edit the schedule for your upcoming workshop. This file is located in the `_includes` directory, make sure to choose the one from the appropriate `dc` (Data Carpentry workshop), `lc` (Library Carpentry), or `swc` (Software Carpentry) subdirectory.

6.  Alternatively,
    if you are already familiar with Git,
    you can clone the repository to your desktop,
    edit `index.md`, `_config.yml`, and `schedule.html` there,
    and push your changes back to the repository.

    ~~~
    git clone -b gh-pages https://github.com/your_username/YYYY-MM-DD-site
    ~~~

    You should specify `-b gh-pages` to checkout the gh-pages branch because the imported 
    repository doesn't have a `master` branch.

    In order to view your changes once you are done editing,
    you must push to your GitHub repository:

    ~~~
    git push origin gh-pages
    ~~~

7.  When you are done editing,
    go to the GitHub Pages URL for your workshop and preview your changes.
    In the example above, this is `https://gvwilson.github.io/2016-12-01-miskatonic`.
    The finished page should look [something like this](fig/completed-page.png?raw=true).

8.  Optional: you can now change the README.md file in your website's repository, which contains these instructions, so that it contains a short description of your workshop and a link to the workshop website.

9.  Optional: Add a link to your workshop website on the repository main page in the description/website section (look for the `Edit` button on the right to add).  

**Note:**
please do all of your work in your repository's `gh-pages` branch,
since [GitHub automatically publishes that as a website][github-project-pages].

**Note:**
this template includes some files and directories that most workshops do not need,
but which provide a standard place to put extra content if desired.
See the [design notes][design] for more information about these.

Further instructions are available in [the customization instructions][customization].
This [FAQ][faq] includes a few extra tips (additions are always welcome)
and these notes on [the background and design][design] of this template may help as well.

## Checking Your Changes Locally

If you want to preview your changes on your own machine before publishing them on GitHub,
you can do so as described below.

1.  Install the software [described below](#installing-software).
    This may require some work,
    so feel free to preview by pushing to the website.

2.  Run the command

    ~~~
    make serve
    ~~~

    and go to <http://0.0.0.0:4000> to preview your site.
    You can also run this command by typing `make serve`
    (assuming you have Make installed).

3.  Run the command

    ~~~
    make workshop-check
    ~~~

    to check for a few common errors in your workshop's home page.
    (You must have Python 3 installed to do this.)

## Creating Extra Pages

In rare cases,
you may want to add extra pages to your workshop website.
You can do this by putting either Markdown or HTML pages in the website's root directory
and styling them according to the instructions give in
[the lesson template][lesson-example].
If you do this,
you *must* also edit `_config.yml` to set these three values:

1.  `carpentry` is either "dc" (for Data Carpentry), "swc" (for Software Carpentry),
    or "lc" (for Library Carpentry). This determines which logos are loaded.

2.  `title` is the title of your workshop (typically the venue and date).

3.  `email` is the contact email address for your workshop,
    e.g., `gvwilson@miskatonic.edu`.

Note: `carpentry` and `email` duplicate information that's in `index.md`,
but there is no way to avoid this
without requiring people to edit both files in the usual case
where no extra pages are created.






[email]: mailto:team@carpentries.org
[customization]: https://carpentries.github.io/workshop-template/customization/index.html
[dc-site]: http://datacarpentry.org
[design]: https://carpentries.github.io/workshop-template/design/
[faq]: https://carpentries.github.io/workshop-template/faq/index.html
[github-project-pages]: https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site
[importer]: https://github.com/new/import
[issues]: https://github.com/carpentries/workshop-template/issues
[jekyll-windows]: http://jekyll-windows.juthilo.com/
[jekyll]: https://jekyllrb.com/
[lesson-example]: https://carpentries.github.io/lesson-example/
[pyyaml]: https://pypi.python.org/pypi/PyYAML
[ruby-install-guide]: https://www.ruby-lang.org/en/downloads/
[ruby-installer]: http://rubyinstaller.org/
[rubygems]: https://rubygems.org/pages/download/
[self-organized-workshop-form]: https://amy.carpentries.org/forms/self-organised/
[swc-site]: http://software-carpentry.org
[lc-site]: https://librarycarpentry.org
