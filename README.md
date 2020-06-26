# Starting Perl in 2020

> How to quickly set up a development environment and learn modern Perl with best practices.

## Why Perl

Why learn Perl in 2020? Unlike Ruby it's installed on pretty much any box you log in to and has [blazing fast startup times](https://github.com/bdrung/startup-time), so you can use it like a faster and more portable version of bash scripting. Unlike Python or Go it has [great support for functional programming](https://hop.perl.plover.com/book/). Unlike JavaScript, the ecosystem is stable so you avoid framework churn. It has a proven track record of 30+ years, so you're bound to run into it somewhere. Many best-in-class tools are written in Perl, like the famous [exiftool](https://exiftool.org/). It has a strong presence in web development, system administration, and data science. It's one of the [highest paid programming languages](https://fossbytes.com/stack-overflow-highest-salary-programming-languages-2020/).

Perl has unique security features like ["taint checking"](https://en.wikipedia.org/wiki/Taint_checking) that can prevent malicious users from executing commands in your application. Its string manipulation and regex capabilities are unparalleled, and its Unicode support is excellent. It will give you deep insight into the world of Unix, since it was made to work with command line tools and builds on the heritage of sed and AWK. If you're familiar with C style languages like C++, JavaScript, PHP, Go, or Java, the syntax will be familiar. There is a massive and growing collection of modules available on [CPAN](https://metacpan.org/). And since Perl has a deep testing culture, the signal:noise ratio is much higher than you'd find on NPM.

## Table of Contents

- [Learning Perl](#learning-perl)
  - [Guided Learning](#guided-learning)
  - [Docs](#docs)
  - [Books](#books)
  - [Getting Help](#getting-help)
  - [Keeping Up to Date](#keeping-up-to-date)
- [Setting up a Development Environment](#setting-up-a-development-environment)
  - [Perl Version Manager](#perl-version-manager)
  - [Module Installer](#module-installer)
  - [Dependencies Manager](#dependencies-manager)
  - [REPL](#repl)
  - [IDE](#ide)
- [Integrating with Third-Party Code](#integrating-with-third-party-code)
  - [Finding Modules](#finding-modules)
  - [Equivalents from Other Languages](#equivalents-from-other-languages)

## Learning Perl

If you just want a quick introduction to Perl, check out [this guide](https://perldoc.perl.org/perlintro.html), [this cheat sheet](https://learnxinyminutes.com/docs/perl/), or [this video](https://www.youtube.com/watch?v=WEghIXs8F6c) (watch at 2x speed to save time). The rest of this section will cover how to get beyond introductions and become a successful Perl programmer.

### Guided Learning

With [Exercism.io's Perl track](https://exercism.io/my/tracks/perl5) you get free training with mini projects of gradually increasing difficulty starting from Hello World. Each one comes with unit tests already set up, so all you have to do is make them pass. Unlike other websites you can use your own IDE with Exercism (auto complete, code formatting, and linting are life savers), and you get personalized feedback from experienced mentors. This means that you will build good habits from the start, and always have someone to help if you get stuck.

### Docs

You can view the [language](https://perldoc.perl.org/perl.html), [functions](https://perldoc.pl/functions), and [core modules](https://perldoc.pl/modules) documentation online, or simply add the Perl docset to one of these apps for instant search results as you type.

- [devdocs.io](https://devdocs.io) - free web app
- [Zeal](https://zealdocs.org/) - free desktop app
- [Dash](https://kapeli.com/dash) - paid Mac app

### Books

Perl's not on a hype cycle right now, so you can snag its best books for bargain prices. And because Perl is an incredibly stable language, they're still relevant. A lot of these books are even free online. But paper books have great information density, you can quickly look things up from their index, and they help you get away from the computer screen for a bit.

- [Beginning Perl](https://www.goodreads.com/book/show/13837737-beginning-perl) - A comprehensive reference and modern introduction to Perl.

- [Effective Perl Programming, 2nd edition](https://www.goodreads.com/book/show/946128.Effective_Perl_Programming) - A list of expert tips that will have you quickly writing great Perl code. This is to Perl what the legendary "Effective C++" is to C++.

- [Modern Perl, 4th edition](https://www.goodreads.com/book/show/10198038-modern-perl) - A short book to quickly bring you up to speed on modern "best practices" Perl. Also available online [for free](http://modernperlbooks.com/books/modern_perl_2016/index.html).

- [Programming Perl, 4th edition](https://www.goodreads.com/book/show/154155.Programming_Perl) - The official reference. It's a massive tome and you can get it for \$10.

- [Higher Order Perl](https://www.goodreads.com/book/show/86365.Higher_Order_Perl) - A classic book on functional programming in Perl. More relevant than ever with the rise of multi-core CPUs. Also available online for [for free](https://hop.perl.plover.com/book/).

- [Mastering Perl, 2nd edition](https://www.goodreads.com/book/show/583634.Mastering_Perl) - Advanced techniques for the working Perl programmer, like secure programming, debugging, profiling, benchmarking, configuration, logging, and error reporting.

### Getting Help

There are active communities on [Discord](https://discord.com/invite/Mnbj6th) and [Reddit](https://reddit.com/r/perl/), but IRC is still the most popular. The two main options there are #perl on [FreeNode](https://freenode.net/) (irc.freenode.net) and #perl-help on [Perl.org](https://www.irc.perl.org/) (irc.perl.org). Everyone is really friendly and helpful, so don't hesitate to swing by. If you need an IRC program to connect with try [HexChat](https://hexchat.github.io/) for Linux/Windows or [LimeChat](http://limechat.net/mac/) for Mac. You can also ask a question on [StackOverflow](https://stackoverflow.com/questions/tagged/perl), or check the [Perl FAQ](https://perldoc.pl/perlfaq).

### Keeping Up to Date

[Perl Weekly](https://perlweekly.com/latest.html) is a popular curated news source. You can subscribe by email or visit the website directly.

## Setting up a Development Environment

### Perl Version Manager

[plenv](https://github.com/tokuhirom/plenv) let's you have multiple Perl versions installed at once and keep their CPAN modules separate. This way you can use a different Perl for different projects without them interfering with each other or the system installed `perl`. It's equivalent to Python's pyenv, Ruby's rbenv, or Node's nvm. Simply [follow the instructions here](https://github.com/tokuhirom/plenv#installation) to install plenv, then run the following commands to install Perl:

```bash
plenv install --list #List available versions
plenv install 5.32.0 #Install latest version
plenv global 5.32.0 #Use as default Perl
perl --version #Confirm latest version is installed properly
```

If the latest Perl version does not show up, double-check the plenv install instructions and make sure you've run `source ~/.bash_profile` or `source ~/.zshrc`

### Module Installer

You can install Perl modules with [cpanminus](https://github.com/miyagawa/cpanminus). This lets you run `cpanm modulenamehere` to quickly install any module from CPAN. To set it up run:

```bash
plenv install-cpanm #Install cpanm
```

### Dependencies Manager

Module dependencies in Perl are managed with [Carton](https://metacpan.org/pod/Carton). It lets you list your project dependencies with a [`cpanfile`](https://metacpan.org/pod/cpanfile), then you can run `carton install` to install them. This is equivalent to pyenv for Python, Bundler for Ruby, or NPM for JavaScript. To install it run:

```bash
cpanm Carton #Install Carton
plenv rehash #Set up "shim" shortcut
carton install #Install module deps for project from the cpanfile
```

### REPL

To install a Perl REPL run this command:

```bash
cpanm Reply #Install Reply REPL
cpanm Term::ReadLine::Gnu #Enable up/down arrow keys for command history
plenv rehash #Set up "shim" shortcut
reply #Enter the REPL
```

### IDE

[Visual Studio Code](https://code.visualstudio.com/) makes for a great modern Perl IDE. Here are the main extensions that will make your life easier.

#### Language Server

The [Perl](https://marketplace.visualstudio.com/items?itemName=richterger.perl) extension is a language server and debugger, with syntax checking, code completion, goto definition, and find references. Requires install of Perl::LanguageServer module.

```bash
cpanm Perl::LanguageServer #Install Perl::LanguageServer
plenv rehash #Set up "shim" shortcut
```

#### Linter/Static Analysis

The [Perl Toolbox](https://marketplace.visualstudio.com/items?itemName=d9705996.perl-toolbox) extension provides static analysis with the [Perlcritic](https://github.com/Perl-Critic/Perl-Critic) linter. Requires install of Perl::Critic module.

```bash
cpanm Perl::Critic #Install Perl::Critic
cpanm Perl::Critic::Freenode #Install extra linter rules
plenv rehash #Set up "shim" shortcut
```

After running these commands, Create a `~/.perlcriticrc` file and add the following to use a good default set of linter rules that enforces good code without nagging over subjective styles. You can always customize the rules once you have more experience.

```.perlcriticrc
theme = core || freenode
severity = 1
exclude = RegularExpressions::RequireLineBoundaryMatching RegularExpressions::RequireDotMatchAnything RegularExpressions::RequireExtendedFormatting ControlStructures::ProhibitCascadingIfElse ValuesAndExpressions::ProhibitMagicNumbers
```

Then open the Visual Studio Code preferences and set `perl-toolbox.lint.useProfile` to `true`. You can do this by manually editing your settings.json file, or going to Settings (`ctrl/cmd + ,`), searching for `perl-toolbox.lint.useProfile`, and clicking the check box.

#### Code Formatter

The [perltidy-more](https://marketplace.visualstudio.com/items?itemName=Kaktus.perltidy-more) extension provides automatic code formatting. Requires install of Perl::Tidy module.

```bash
cpanm Perl::Tidy #Install Perl::Tidy
plenv rehash #Set up "shim" shortcut
```

## Integrating with Third-Party Code

### Finding Modules

A lot of hard problems have already been solved by the Perl community. There are almost 200k Perl modules on CPAN, which is easily searchable from [metacpan](https://metacpan.org/). If you are looking for something but don't know where to start, here is a [curated list of modules](https://metacpan.org/pod/Task::Kensho).

### Equivalents from Other Languages

- **Version manager** - [plenv](https://github.com/tokuhirom/plenv) - like perlenv (Python), rbenv (Ruby), or nvm (JavaScript)
- **Dependency manager** - [Carton](https://metacpan.org/pod/Carton) - like Poetry (Python), Bundler (Ruby), or NPM (JavaScript)
- **Linter** - [perlcritic](https://metacpan.org/pod/perlcritic) - like Pylint (Python), Rubocop (Ruby), or ESLint (JavaScript)
- **Formatter** - [perltidy](https://metacpan.org/pod/perltidy) - like Black (Python), Standard (Ruby), or Prettier (JavaScript)
- **Web app interface** - [Plack](https://plackperl.org/) - like WSGI (Python), or Rack (Ruby)
- **Lightweight web framework** - [Dancer](http://perldancer.org/) - like Flask (Python), Sinatra (Ruby), or Express (JavaScript)
- **MVC web framework** - [Catalyst](http://www.catalystframework.org/) - like Django (Python), Rails (Ruby), or Nest (JavaScript)
- **Real-time web framework** - [Mojolicious](https://mojolicious.org/) - like Twisted (Python)
- **ORM (Active Record pattern)** - [DBIx::Class](https://metacpan.org/pod/DBIx::Class) - like ActiveRecord (Ruby), Django ORM (Python)
- **Web Scraping** - [WWW::Mechanize](https://metacpan.org/pod/WWW::Mechanize) - like Mechanize (Ruby), mechanize (Python)
- **Browser Automation** - [WWW::Selenium](https://metacpan.org/pod/WWW::Selenium) - Like WebDriver (Ruby), Selenium (Python), Nightwatch.js (JavaScript), Nightwatch.js/Puppeteer (JavaScript)
