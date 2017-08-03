Please note that while this is a relatively simple matter of programming, we are particularly interested in seeing the design of your solution. We will evaluate your code not only based on correctness but also based on design and organization. Pretend this is code being written to go into production.

The given log file is a standard log file in the [Apache combined log format](https://httpd.apache.org/docs/1.3/logs.html#combined) (with referrer information stripped out). You will write code to parse this file and generate a report which breaks down some of the information based on the country and US state where visitors came from. This code should be delivered in the form of one or more classes. Please include any tests you wrote along the way as well.

**Please write your example in Perl, Python, Ruby, JavaScript, PHP, or Go. If you want to use a different language please contact us first.** You are also encouraged to use any third party libraries you like. However, you must deliver the end result in a way that allows us to run the code on a standard Ubuntu Trusty or Xenial system. That means either packaging up all of your dependencies or giving us very clear instructions on how to install them. Unless the language you choose is Perl or Go, assume that we do not know anything about the package management tools for that language! We will run your code to look at the output, as well as looking at the code itself.

Include instructions on how to run the code, either as the output of `your-command --help` or as a separate README.md file. Your instructions should tell us how to specify the access log file to parse, as well as how to specify the MaxMind GeoIP2 City database to use. This can either be done via command line flags or by telling us where to put these files relative to your script.

The code you write should use one of the available GeoIP2 APIs to get geographical information about the IP addresses in the log. See [our developer site](http://dev.maxmind.com/geoip/geoip2/downloadable/) for details on the APIs which are available. Feel free to use either an official API or a third party one. **You must use one of the APIs linked from this page.** Use the [GeoLite2 City database](http://geolite.maxmind.com/download/geoip/database/GeoLite2-City.mmdb.gz) as your MaxMind database.

Include a command line program to run your code against an arbitrary file. The output of that program should be a report in the format of your choice. Don't worry too much about making this fancy. Printing lightly formatted text to the console is fine (so is an HTML page).

Ignore all requests for images, CSS, and JavaScript. This is any request path beginning with:

* `/[a-f0-9]+/css/`
* `/[a-f0-9]+/images/`
* `/[a-f0-9]+/js/`
* `/entry-images/`
* `/images/`
* `/user-images/`
* `/static/`
* `/robots.txt`
* `/favicon.ico`

Also ignore all paths ending in `.rss` or `.atom`.

The report itself should show the following information:

* Top 10 countries for visitors
    * include the name of the country in English and the number of visitors from that country
    * sort the results by number of visitors (most to least)
    * for each country show the page *other than `/`* that visitors from that country visited the most
* Top 10 US states, ignoring visitors outside the US
    * same as above for output

**For the purposes of this code, "the page" is the path including the query string.**

If there are less than 10 states or countries with visitors, only show those which have at least one visitor.

Note that the GeoLite2 data file may simply not have all the relevant information on some IP addresses. In this case, assign the visit to a state or country of "unknown" as needed.

## Sharing Your Code with Us

We do not want your answer to be publicly available on the Internet for anyone to find. You can share your code with us in one of several ways:

* Make a private repo and share it with us. We will tell you who to invite to the repo when we ask you to do this homework.
  * While GitHub charges for private repos, you can also use BitBucket or GitLab, both of which allow private repos on their free plans.
* Send us an email with a zip or tarball attachment. You can send this to your HR contact at MaxMind.

## Copyright

This repository is copyright MaxMind 2014-2017. You may distribute it under
the [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License](https://creativecommons.org/licenses/by-nc-nd/4.0/).
