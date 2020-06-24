# Starting Perl in 2020

> How to quickly set up a development environment and learn modern Perl with best practices.

## Why Perl

Why learn Perl in 2020? Unlike Ruby it's installed on pretty much any box you log in to, so you can use it like a faster and more portable version of bash scripting. Unlike Python or Go it has [great support for functional programming](https://hop.perl.plover.com/book/). Unlike JavaScript, the ecosystem is stable so you avoid framework churn. It has a proven track record of 30+ years, so you're bound to run into it somewhere. Many best-in-class tools are written in Perl, like the famous [exiftool](https://exiftool.org/). It has a strong presence in web development, system administration, and data science. It's one of the [highest paid programming languages](https://fossbytes.com/stack-overflow-highest-salary-programming-languages-2020/).

Perl has unique security features like ["taint checking"](https://en.wikipedia.org/wiki/Taint_checking) that can prevent malicious users from executing commands in your application. Its string manipulation and regex capabilities are unparalleled, and its Unicode support is excellent. It will give you deep insight into the world of Unix, since it was made to work with command line tools and builds on the heritage of sed and AWK. If you're familiar with C style languages like C++, JavaScript, PHP, Go, or Java, the syntax will mostly feel familiar. There is a massive and growing collection of modules available on [CPAN](https://metacpan.org/). And since Perl has a deep testing culture, the signal:noise ratio is much higher than you'd find on NPM.

## Table of Contents

- [Learning Perl](#learning-perl)
  - [Guided Learning](#guided-learning)
  - [Docs](#docs)
  - [Books](#books)
  - [Getting Help](#getting-help)
  - [Keeping Up to Date](#keeping-up-to-date)
- [Setting up a Development Environment](#setting-up-a-development-environment)
  - [IDE](#ide)
  - [Perl Version Manager](#perl-version-manager)
  - [Package Manager](#package-manager)
  - [REPL](#repl)
- [Building Software](#building-software)
  - [Finding Modules](#finding-modules)
  - [Equivalents from Other Languages](#equivalents-from-other-languages)

## Learning Perl

If you just want a quick introduction to Perl, check out [this guide](https://perldoc.perl.org/perlintro.html) or [this video](https://www.youtube.com/watch?v=WEghIXs8F6c) (watch at 2x speed to save time). The rest of this section will cover how to get beyond introductions and become a successful Perl programmer.

### Guided Learning

With [Exercism.io's Perl track](https://exercism.io/my/tracks/perl5) you get free training with mini projects of gradually increasing difficulty starting from Hello World. Each one comes with unit tests already set up, so all you have to do is make them pass. Unlike other programs you can use your own IDE (auto complete, code formatting, and static analysis are life savers), and you get personalized feedback from experienced mentors. This means that you will build good habits from the beginning, and always have someone to help if you get stuck.

### Docs

You can view the [language](https://perldoc.perl.org/perl.html), [functions](https://perldoc.pl/functions), and [core modules](https://perldoc.pl/modules) documentation online, or simply add the Perl docset to one of these apps for instant search results.

- [devdocs.io](https://devdocs.io) - free web app
- [Zeal](https://zealdocs.org/) - free desktop app
- [Dash](https://kapeli.com/dash) - paid Mac app

### Books

Perl's not on a hype cycle right now, so you can snag all of its best books for bargain prices. And because Perl is a really stable language, the're still relevant. A lot of these books are even free online. But paper books have great information density, you can quickly look things up with their index, and they help you get away from the computer screen for a bit.

- [Beginning Perl](https://www.goodreads.com/book/show/13837737-beginning-perl) - A comprehensive reference and modern introduction to Perl.

- [Effective Perl Programming, 2nd edition](https://www.goodreads.com/book/show/946128.Effective_Perl_Programming) - A list of expert tips that will have you quickly writing great Perl code. This is to Perl what the legendary "Effective C++" is to that language.

- [Modern Perl, 4th edition](https://www.goodreads.com/book/show/10198038-modern-perl) - A short book to quickly bring you up to speed on modern best practices Perl. Also available online [for free](http://modernperlbooks.com/books/modern_perl_2016/index.html).

- [Programming Perl, 4th edition](https://www.goodreads.com/book/show/154155.Programming_Perl) - The official reference. It's a massive tome and you can get it for \$10.

- [Higher Order Perl](https://www.goodreads.com/book/show/86365.Higher_Order_Perl) - A classic book on functional programming in Perl. More relevant than ever with the rise of multi-core CPUs. Also available online for [for free](https://hop.perl.plover.com/book/).

- [Mastering Perl, 2nd edition](https://www.goodreads.com/book/show/583634.Mastering_Perl) - Advanced techniques for the working Perl programmer, like secure programming techniques, debugging, profiling, benchmarking, configuration, logging, and error reporting.

### Getting Help

There are active communities on [Discord](https://discord.com/invite/Mnbj6th) and [Reddit](https://reddit.com/r/perl/). For IRC the two main options are #perl on FreeNode (irc.freenode.net) and #perl-help on [irc.perl.org](https://www.irc.perl.org/). Everyone is really friendly and helpful, so don't hesitate to swing by. If you need an IRC program to connect with try [HexChat](https://hexchat.github.io/) for Linux/Windows or [LimeChat](http://limechat.net/mac/) for Mac. You can also ask a question on [StackOverflow](https://stackoverflow.com/questions/tagged/perl), or check the [Perl FAQ](https://perldoc.pl/perlfaq).

### Keeping Up to Date

[Perl Weekly](https://perlweekly.com/latest.html) is a popular curated news source. You can subscribe by email or visit the website directly.

## Setting up a Development Environment

### IDE

[Visual Studio Code](https://code.visualstudio.com/) makes for a great modern Perl IDE. Here are the main extensions that will make your life easier.

- [Perl](https://marketplace.visualstudio.com/items?itemName=richterger.perl) - Language server and debugger. Has syntax checking, code completion, goto definition, and find references.
- [perltidy-more](https://marketplace.visualstudio.com/items?itemName=Kaktus.perltidy-more) - Automatic code formatter.
- [Perl Toolbox](https://marketplace.visualstudio.com/items?itemName=d9705996.perl-toolbox) - Static analysis tool with linting provided by [Perlcritic](https://github.com/Perl-Critic/Perl-Critic).
- [Better Perl Syntax](https://marketplace.visualstudio.com/items?itemName=jeff-hykin.better-perl-syntax) - Great syntax highlighting.

### Perl version manager

[plenv](https://github.com/tokuhirom/plenv) let's you have multiple Perl versioned installed at once, and keep their CPAN packages separate. This way you can use a different Perl for different projects without them interfering with each other or the system installed `perl`. It's equivalent to Python's [pyenv](https://github.com/pyenv/pyenv), Ruby's [rbenv](https://github.com/rbenv/rbenv), Node's [nvm](https://github.com/nvm-sh/nvm), or the multi-language [asdf-vm](https://asdf-vm.com/). Simply [follow the instructions here](https://github.com/tokuhirom/plenv#installation) to install plenv, then run the following commands to install Perl:

```bash
plenv install --list #List available versions
plenv install 5.32.0 #Install latest version
plenv global 5.32.0 #Use as default Perl
perl --version #Confirm latest version is installed properly
```

If the latest Perl version does not show up, double-check the plenv install instructions and make sure you've run `source ~/.bash_profile` or `source ~/.zshrc`

### Module Installer

You can install Perl modules with [cpanminus](https://github.com/miyagawa/cpanminus). To set it up run:

```bash
curl -L https://cpanmin.us | perl - App::cpanminus
```

### Module Dependencies Manager

Module dependencies in Perl are managed with [Carton](https://metacpan.org/pod/Carton). This is equivalent to pyenv in Python, Bundler in Ruby, or NPM in JavaScript. To install it run:

```bash
cpanm Carton
```

Then you can install dependencies for any project using a [`cpanfile`](https://metacpan.org/pod/cpanfile) with:

```bash
carton install
```

### REPL

To install a Perl REPL run this command:

```bash
cpanm App::perlsh
```

### Finding Modules

There are almost 200k Perl modules on CPAN, which is easily searchable from [metacpan](https://metacpan.org/). If you are looking for something but don't know where to start, here is a [curated list of modules](https://metacpan.org/pod/Task::Kensho).

### Equivalents from Other Languages

- **Web app interface** - [Plack](https://plackperl.org/) - like WSGI (Python), or Rack (Ruby)
- **Version manager** - [Perlbrew](https://perlbrew.pl/) - like perlenv (Python), rbenv (Ruby), or nvm (JavaScript)
- **Dependency manager** - [Carton](https://metacpan.org/pod/Carton) - like Poetry (Python), Bundler (Ruby), or NPM (JavaScript)
- **Lightweight web framework** - [Dancer](http://perldancer.org/) - like Flask (Python), Sinatra (Ruby), or Express (JavaScript)
- **MVC web framework** - [Catalyst](http://www.catalystframework.org/) - like Django (Python), Rails (Ruby), or Nest (JavaScript)
- **Real-time web framework** - [Mojolicious](https://mojolicious.org/) - like Twisted (Python)
