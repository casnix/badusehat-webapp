# badusehat-webapp

Badusehat is the name I've given to my hobby projects that consist of automating household systems, automating organization
of my life, playing with new technologies, cybersecurity research, and generally using the wrong tool for the job.  The
"bad use" part of the name is a reminder that I may be making a tool or component do something it wasn't designed to do,
"hacking" in the original meaning of the word.  The "hat" at the end of the name implies some connotation with cybersecurity,
of which I explore white-hat (ethical) topics and technologies.  

The Badusehat projects are intended to teach myself techniques for improvising when the right tools for the job aren't
available, making cost cutting decisions by using hardware or software that is not typically used to accomplish a particular
task, and making the technologies I work on more secure and robust against the growing threat of cyber-crime.

The purpose of this webapp is to give me a way to control automation from offsite, and to discuss my techniques and how
they work.

The source for this webapp is licensed under GPLv3.0, and uses my phpbuild utility to control source code output
and generation.  Using phpbuild will help control how the front end communicates with the backend depending on which
language/framework I use.  See below.

# Order of development

The order of webapp backends I will build are:

1) PHP backend with Apache
2) Ruby on Rails backend with Apache
3) Node.JS backend using Express with proxy and Apache

After a Node.JS webapp is built and satisfactory, I will expand to an Apache Cordova app which will be in another
Github repository: one for Android that can synchronize with my servers (for automation control and automating
organization), another for Windows/Electron(?), and probably—eventually—a raspberry pi environment.

# Source code organization

In this repo are 4 top level directories:

1) `/phpapp`
2) `/railsapp`
3) `/nodejsexpressapp`
4) `/htdocs`

The source code for the application backend is maintained in the respective of the first three directories.
The phpbuild HTML code for the front end is maintained in the `/htdocs` directory.

In each of the four directories is another tree of directories, mirroring this order:

1) `./appsrc`, the pre-phpbuild preprocessor source
2) `./maps`, function maps for space efficiency
3) `./targetsrc`, the post-phpbuild preprocessor source 
4) `./buildout`, the built/finished source code depending on phpbuild arguments