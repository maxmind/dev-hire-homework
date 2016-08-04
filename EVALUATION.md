This is a guide for those involved with hiring at MaxMind to evaluate the
homework (but if you're an applicant you're welcome to read this).

## Questions to Ask When Reviewing Homework

* Is the code in one of the specified languages, or did the applicant get a
  special dispensation (papal or otherwise) to use another language?
* Is the code runnable on an Ubuntu Trusty or Xenial system without too much
  difficulty (installing 3rd party libraries is not too much difficulty as
  long as clear instructions are provided. Installing ten PPAs from ten
  different sources *is* too much difficulty)?
  * If the code is not in Perl or Go, are the instructions written for people
    without much experience in that language?
* Does the homework include instructions in a `README` or as the output of
  `command --help`?
  * If the code isn't in Perl or Go, there really needs to be a `README` of
    some sort!
* Does the code do more or less what it should (run it and eyeball the output
  for sanity)?
  * We should expect some slight variance from the internal answer we have
    because of small ambiguities in the instructions. For example seeing a
    slightly different order of countries or states, or one different top URL,
    is usually not an indication of any serious mistakes in the
    implementation. If all of the countries or states are different, it's
    worth investigating the applicant's implementation further to see if they
    did something really wrong.
* Does the output include the specified data?
  * Top 10 countries by visitor count, with name of country in English and
    visitor count for the country.
    * Plus top page for that country that is not the root page (`/`).
  * Same top 10 list for US states.
* Does the code handle the following cases sanely ...
  * IP does not exist in the GeoIP2 database?
  * IP exists but does not have country info?
  * IP exists and is in the US but does not have state info?
* Is the code organized in a reasonable manner?
  * Is the split between various packages (if any) done in a way that breaks
    down well across responsibilities?
  * Is the split between the invoking CLI program and the modules sensible?
* Does the code use appropriate 3rd party libraries?
* Does the code use a GeoIP2 client library?
  * It's ok if they just use a low level MaxMind DB reader too, since the
    distinction between the two types of libraries is not obvious if you're
    new to our products.
* Is the code written in a modern style for the language, avoiding known-bad
  idioms or techniques?
* Does the implementation avoid repeated code for easily abstracted things
  (like counting and/or displaying top N things)?

### Bonus points

These things are nice to have, but depending on the applicant's level of
experience, they may not be able to get to them in the time specified.

* Is there any sort of API documentation for some or all of the code?
  * If so, is it well organized and clearly written?
* Are there any sort of unit and/of functional tests?
  * If so, are they well organized and clearly written?
