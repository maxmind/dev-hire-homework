The given log file is a standard Apache log file in the [common log format](https://en.wikipedia.org/wiki/Common_Log_Format). You will write code to parse this file and generate a report which breaks down some of the information based on the country and US state where visitors came from. This code should be delivered in the form of one or more classes, along with some unit tests.

You can use any language you are comfortable with, as long as that language has an API for the GeoIP2 databases (see below). You are also encouraged to use any third party libraries you like. However, you must deliver the end result in a way that allows us to run the code on a standard Ubuntu Precise or Trusty system. That means either packaging up all of your dependencies or giving us very clear instructions on how to install them. Unless the language you choose is Perl, assume that we do not know anything about the package management tools for that language! We will run your code to look at the output, as well as looking at the code itself.

The code you write should use one of the available GeoIP2 APIs to get geographical information about the IP addresses in the log. See [our developer site]http://dev.maxmind.com/geoip/geoip2/downloadable/) for details on the APIs which are available. Use the [GeoLite2 City database](http://dev.maxmind.com/geoip/geoip2/geolite2/) as your MaxMind database.

Include a command line program to run your code against an arbitrary file. The output of that program should be a report in the format of your choice. Don’t worry too much about making this fancy. Printing lightly formatted text to the console is fine (so is an HTML page).

The report itself should show the following information:

* Top 10 countries for visitors - include the name of the country in English and the number of visitors from that country - sort the results by number of visitors (most to least) - for each country show the page that visitors from that country visited the most
* Top 10 US states ignoring visitors outside the US - same as above for output
