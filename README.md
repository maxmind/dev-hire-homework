The exercise involves creating a single page application using the JavaScript
framework of your choice (such as AngularJS [preferred], Ember, or Backbone).
Feel free to use a CSS framework if you like.  Please include any tests you
wrote along the way.

**We want to make sure you have the best homework submission possible, so
please take your time to ensure that your submission is exemplary of your
skills and work.**

Use the GitHub REST API to create a simple single page app that can browse
information on GitHub. The single page app should start by prompting the user
to enter a repository name (**maxmind/libmaxminddb**) or a full repository URL
(https://github.com/maxmind/libmaxminddb).

Use that information to look up information about the repo and display it.
There is obviously a lot of information to display, and you don't need to show
all of it. Pick a few items to include, such as relevant links, name, owner,
etc.

For each repo entered, display a list of contributors. Each item in this list
should be clickable, and clicking on the contributor should show some
information about that GitHub account. Again, you don't need to display all the
information about the user. Just pick a few relevant items.

Do include a list of all the public repositories for the user, and do something
sane if there are none to display.

Finally, while this must be a single page application, make sure that the
browser's back and forward buttons works properly when using this application.
In addition, individual views should be bookmarkable.

None of the URLs used by this application should require authentication.

## Sharing Your Code with Us

We do not want your answer to be publicly available on the Internet for anyone
to find. You can share your code with us in one of several ways:

* Make a **private** repo and share it with us. We will tell you who to invite to
the repo when we ask you to do this homework.
	* While GitHub charges for private repos, you can also use BitBucket or
GitLab, both of which allow private repos on their free plans.
* Send us an email with a zip or tarball attachment. You can send this to your
HR contact at MaxMind.
