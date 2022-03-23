# Starting Perl in 2021

> How to quickly set up a development environment and learn modern Perl with best practices.

## Why Perl

Why learn Perl in 2021? It has many outstanding qualities you won't find elsewhere that make it worth adding to your toolkit. Unlike Ruby and Python3, it's installed on almost any box you SSH into, like the Vim of programming languages. Because of this and its [famously quick startup time](https://github.com/bdrung/startup-time), you can use Perl like a faster, more portable and robust Bash script. Unlike Python and Go it has [great support for functional programming](https://hop.perl.plover.com/book/), including filter/map/reduce and tail call optimization. Unlike [JavaScript](https://www.madetech.com/blog/javascript-fatigue/), the ecosystem is stable so you avoid constant framework churn. Unlike [Python](https://learning-python.com/python-changes-2014-plus.html), avoiding breaking changes is top priority for Perl. It has a proven track record of 30+ years, so you're bound to run into it somewhere. Many best-in-class tools are written in Perl such as the famous [exiftool](https://exiftool.org/). It has a strong presence in web development, system administration, and [data science](https://bioperl.org/). It's one of the [highest paid programming languages](https://fossbytes.com/stack-overflow-highest-salary-programming-languages-2020/).

Perl's string manipulation and regex capabilities are unparalleled and it has excellent Unicode support. Perl will give you deep insight into the world of Unix since it builds on the heritage of sed/AWK and was made to pipe command line programs. If you're familiar with C style languages like C++, JavaScript, PHP, Go, or Java, the syntax will be familiar. There is a massive and still growing collection of packages available on [CPAN](https://metacpan.org/), each with its documentation and list of dependencies uniformly laid out front and center. Combined with CPAN's [deep testing culture](https://qa.perl.org/cpan-testers/), you get the highest signal:noise package ecosystem of any scripting language.

> "Perl is, in intent, a cleaned up and summarized version of that wonderful semi-natural language known as 'Unix'."
> – Larry Wall, creator of Perl

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
  - [Language Server](#language-server)
  - [Linter/Static Analysis](#linter/static-analysis)
  - [Code Formatter](#code-formatter)
  - [Debugger](#debugger)
  - [Syntax Highlighting for Mojolicious Templates](#syntax-highlighting-for-mojolicious-templates)
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

Perl's not on a hype cycle right now, so you can snag its best books at bargain prices. And because Perl is an incredibly stable language, they're still relevant. A lot of these books are even free online. But paper books have great information density, you can quickly look things up from their index, and they help you get away from the computer screen for a bit.

- [Beginning Perl](https://www.goodreads.com/book/show/13837737-beginning-perl) - A comprehensive reference and modern introduction to Perl.

- [Effective Perl Programming, 2nd edition](https://www.goodreads.com/book/show/946128.Effective_Perl_Programming) - A list of expert tips that will have you quickly writing great Perl code. This is to Perl what the legendary "Effective C++" is to C++.

- [Modern Perl, 4th edition](https://www.goodreads.com/book/show/10198038-modern-perl) - A short book to quickly bring you up to speed on modern "best practices" Perl. Also available online [for free](http://modernperlbooks.com/books/modern_perl_2016/index.html).

- [Programming Perl, 4th edition](https://www.goodreads.com/book/show/154155.Programming_Perl) - The official reference. A massive tome that is essentially a printed version of the Perl documentation with many more examples.

- [Higher Order Perl](https://www.goodreads.com/book/show/86365.Higher_Order_Perl) - A classic book on functional programming in Perl. More relevant than ever with the rise of multi-core CPUs. Also available online for [for free](https://hop.perl.plover.com/book/).

- [Mastering Perl, 2nd edition](https://www.goodreads.com/book/show/583634.Mastering_Perl) - Advanced techniques for the working Perl programmer, like secure programming, debugging, profiling, benchmarking, configuration, logging, and error reporting.

- [Advanced Perl Programming, 1st edition](https://www.goodreads.com/book/show/583608.Advanced_Perl_Programming) - Full of sage insight into advanced Perl topics and internals. Get the 1st edition. The 2nd edition is a totally different book and doesn't cover the same information.

### Getting Help

There are active communities on [Discord](https://discord.com/invite/Mnbj6th) and [Reddit](https://reddit.com/r/perl/), but IRC is still the most popular. The two main options there are #perl on [FreeNode](https://freenode.net/) (irc.freenode.net) and #perl-help on [Perl.org](https://www.irc.perl.org/) (irc.perl.org). Everyone is really friendly and helpful, so don't hesitate to swing by. If you need an IRC program to connect with try [HexChat](https://hexchat.github.io/) for Linux/Windows or [LimeChat](http://limechat.net/mac/) for Mac. You can also ask a question on [StackOverflow](https://stackoverflow.com/questions/tagged/perl), or check the [Perl FAQ](https://perldoc.pl/perlfaq).

### Keeping Up to Date

[Perl Weekly](https://perlweekly.com/latest.html) is a popular curated news source. You can subscribe by email or visit the website directly.

## Setting up a Development Environment

### Perl Version Manager

[asdf](https://asdf-vm.com/) let's you have multiple Perl versions installed at once and keep their CPAN modules separate. This way you can use a different Perl for different projects without them interfering with each other or the system installed `perl`. It also works with other programming languages, so you can use the same version manager for Node, Ruby, Python, Go, Rust, etc. Simply [follow the instructions here](https://asdf-vm.com/#/core-manage-asdf?id=install) to install asdf, then run the following commands to install Perl:

```bash
asdf plugin add perl https://github.com/ouest/asdf-perl.git #Install Perl plugin for asdf
asdf install perl 5.32.1 #Install latest Perl version at time of writing
asdf global perl 5.32.1 #Use as default Perl
perl --version #Confirm latest version is installed properly
```

If the latest Perl version does not show up, double-check the asdf install instructions and make sure you've run `source ~/.bash_profile` or `source ~/.zshrc`

### Module Installer

You can install Perl modules with [cpanminus](https://github.com/miyagawa/cpanminus). This lets you run `cpanm modulenamehere` to quickly install any module from CPAN. To set it up run:

```bash
curl -L https://cpanmin.us > cpanm_setup.pl #Download cpanm setup script
perl cpanm_setup.pl App::cpanminus #Run cpanm setup state
```

### Dependencies Manager

Module dependencies in Perl are managed with [Carton](https://metacpan.org/pod/Carton). It lets you list your project dependencies with a [`cpanfile`](https://metacpan.org/pod/cpanfile), then you can run `carton install` to install them. This is equivalent to pipenv/Poetry for Python, Bundler for Ruby, or NPM for JavaScript. To install it run:

```bash
cpanm Carton #Install Carton
asdf reshim perl #Set up binary "shim" (command line shortcut)
carton install #Install module deps for project from the cpanfile
```

Then when you have a script that uses a Carton installed package (for example `use JSON::MaybeXS;`), run it with `perl -Ilocal/lib/perl5` or the shorcut `carton exec perl` and it will link up to the package install path:

```bash
perl -Ilocal/lib/perl5 myscript.pl #the long way
carton exec perl myscript.pl #the short way
```

You might want to alias `carton exec` in your `~/.bash_profile` or `~/.zshrc`

```bash
alias ce="carton exec"
alias cep="carton exec perl"
```

Then you can do one of

```bash
ce perl myscript.pl
cep myscript.pl
```

### REPL

To install a Perl REPL run this command:

```bash
cpanm Reply #Install Reply REPL
cpanm Term::ReadLine::Gnu #Enable up/down arrow keys for command history
asdf reshim perl #Set up binary "shim" (command line shortcut)
reply #Enter the REPL
```

To launch Reply with your Carton dependencies loaded:

```bash
carton exec reply
```

Then you can include packages you want to use from the REPL with `use My::Dependency::Name;` and they will work without issue.

### IDE

[Visual Studio Code](https://code.visualstudio.com/) makes for a great modern Perl IDE. Here are the main extensions that will make your life easier.

#### Language Server

The [Perl](https://marketplace.visualstudio.com/items?itemName=richterger.perl) extension is a language server and debugger, with syntax checking, code completion, goto definition, and find references. Requires install of Perl::LanguageServer module.

```bash
cpanm Perl::LanguageServer #Install Perl::LanguageServer
asdf reshim perl #Set up binary "shim" (command line shortcut)
```

#### Linter/Static Analysis

The [Perl Toolbox](https://marketplace.visualstudio.com/items?itemName=d9705996.perl-toolbox) extension provides static analysis with the [Perlcritic](https://github.com/Perl-Critic/Perl-Critic) linter. Requires install of Perl::Critic module.

```bash
cpanm Perl::Critic #Install Perl::Critic
cpanm Perl::Critic::Freenode #Install extra linter rules
asdf reshim perl #Set up binary "shim" (command line shortcut)
```

After running these commands, Create a `~/.perlcriticrc` file and add the following to use a default set of linter rules that enforces good code without nagging over subjective styles. You can always customize the rules once you have more experience.

```.perlcriticrc
theme = core || freenode
severity = 1
exclude = RegularExpressions::RequireLineBoundaryMatching RegularExpressions::RequireDotMatchAnything RegularExpressions::RequireExtendedFormatting ControlStructures::ProhibitCascadingIfElse ValuesAndExpressions::ProhibitMagicNumbers ControlStructures::ProhibitUnlessBlocks ControlStructures::ProhibitPostfixControls ValuesAndExpressions::ProhibitConstantPragma RegularExpressions::ProhibitEscapedMetacharacters Variables::ProhibitPunctuationVars ErrorHandling::RequireCarping ValuesAndExpressions::ProhibitEmptyQuotes CodeLayout::RequireTrailingCommas CodeLayout::ProhibitParensWithBuiltins ValuesAndExpressions::RequireInterpolationOfMetachars

[InputOutput::RequireCheckedSyscalls]
functions = :builtins
exclude_functions = print

[InputOutput::ProhibitBacktickOperators]
only_in_void_context = 1
```

Then open the Visual Studio Code preferences and set `perl-toolbox.lint.useProfile` to `true`. You can do this by manually editing your settings.json file, or going to Settings (`ctrl/cmd + ,`), searching for `perl-toolbox.lint.useProfile`, and clicking the check box.

#### Code Formatter

The [perltidy-more](https://marketplace.visualstudio.com/items?itemName=Kaktus.perltidy-more) extension provides automatic code formatting. Requires install of Perl::Tidy module.

```bash
cpanm Perl::Tidy #Install Perl::Tidy
asdf reshim perl #Set up binary "shim" (command line shortcut)
```

Formatting options are controlled by a `~/.perltidyrc` file. Here's a good starting default:

```.perltidyrc
-i=2 #indent with 2 spaces instead of 4
```

#### Debugger

Perl comes with a built-in debugger that is like Ruby's Pry or Byebug. NOTE: To get up/down arrows working for command history in the debugger, you must install Readline support. You'll also want to install Reply which integrates nicely with the debugger.

```bash
cpanm Reply #Install Reply REPL
cpanm Term::ReadLine::Gnu #Enable up/down arrow keys for command history
asdf reshim perl #Set up binary "shim" (command line shortcut)
```

To set a breakpoint in your code just add this line anywhere in your program:

```perl
$DB::single = 1;
```

Then run your program with the `-d` flag like so:

```perl
perl -d myprogram.pl
```

That will boot you into a prompt and immediately stop execution. Press `c` to continue execution to the breakpoint you set. Then print variables with `p` or `x` for more detail, like so:

```perl
DB<3> p $link_regex;
(https://haxe.io/roundups/\d+/)

DB<4> x $newsletter_entry;
0  HASH(0x7fafef8cd0b0)
   'category' => 'Programming Languages'
   'feed_url' => 'https://blog.skialbainn.com/rss'
   'link_regex' => '(https://haxe.io/roundups/\\d+/)'
   'link_selector' => '//item/description'
   'name' => 'Haxe Roundup'
   'updated_selector' => '//item/pubDate'
   'url' => 'https://haxe.io/'
```

Cheatsheet of common commands:

##### Execution

- `c` - continue execution
- `n` - step execution to the next line
- `s` - step into the next executable statement including subroutines
- `r` - run through the current subroutine and stop on the return statement

###### Printing

- `x` - print a detailed inspection of a variable
- `p` - print out a variable (hides empty values, unlike `x`)
- `v` - see the current line you're on with code surrounding it for context
- `T` - print the current stacktrace

###### Other

- `h` - help listing of commands
- `q` - quit the debugger.

There are two books on Perl debugging that you can get for about $5 or $10 each.

- [Perl Debugger Pocket Reference](https://www.goodreads.com/book/show/1036840.Perl_Debugger_Pocket_Reference)
- [Pro Perl Debugging](https://www.goodreads.com/book/show/605612.Pro_Perl_Debugging)

#### Syntax Highlighting for Mojolicious Templates

If you're using `Mojo::Template` then install [the official Mojolicious Templates extension](https://marketplace.visualstudio.com/items?itemName=kraih.mojolicious), made by the creator of Mojlicious. It adds syntax highlighting for the templates, even when they are embedded directly into Perl code. To make sure HTML emmet snippets also work within Mojolicious templates, add the following to your `settings.json` file:

```json
"emmet.includeLanguages": {
  "mojolicious": "html"
}
```

## Integrating with Third-Party Code

### Finding Modules

A lot of hard problems have already been solved by the Perl community. There are almost 200k Perl modules on CPAN, all of which are easily searchable from [metacpan](https://metacpan.org/). If you are looking for something but don't know where to start, here is a [community-curated list of modules](https://metacpan.org/pod/Task::Kensho).

### Equivalents from Other Languages

- **Dependency manager** - [Carton](https://metacpan.org/pod/Carton) - like pipenv/Poetry (Python), Bundler (Ruby), or NPM (JavaScript)
- **Linter** - [perlcritic](https://metacpan.org/pod/perlcritic) - like Pylint (Python), Rubocop (Ruby), or ESLint (JavaScript)
- **Formatter** - [perltidy](https://metacpan.org/pod/perltidy) - like Black (Python), Standard (Ruby), or Prettier (JavaScript)
- **Debugger** - [perldebug](https://perldoc.perl.org/perldebug) - like Pry or Byebug (Ruby)
- **Web app interface** - [Plack](https://plackperl.org/) - like WSGI (Python), or Rack (Ruby)
- **Lightweight web framework** - [Dancer](http://perldancer.org/) - like Flask (Python), Sinatra (Ruby), or Express (JavaScript)
- **Real-time web framework** - [Mojolicious](https://mojolicious.org/) - like Twisted (Python)
- **MVC web framework** - [Catalyst](http://www.catalystframework.org/) - like Django (Python), Rails (Ruby), or Nest (JavaScript)
- **ORM (Active Record pattern)** - [DBIx::Class](https://metacpan.org/pod/DBIx::Class) - like ActiveRecord (Ruby), Django ORM (Python)
- **Templating** - [Mojo::Template](https://docs.mojolicious.org/Mojo/Template) and [Template::Toolkit](http://template-toolkit.org/) - like erb (Ruby), Django templates (Python), Mustache/Handlbards (JavaScript)
- **Web Scraping** - [Mojo::UserAgent](https://docs.mojolicious.org/Mojo/UserAgent), [WWW::Mechanize](https://metacpan.org/pod/WWW::Mechanize) - like Mechanize (Ruby), MechanicalSoup (Python), Puppeteer (JavaScript)
- **DOM Parsing** - [Mojo::DOM](https://docs.mojolicious.org/Mojo/DOM) - like Nokogiri (Ruby), Beautiful Soup (Python)
- **Browser Automation** - [WWW::Selenium](https://metacpan.org/pod/WWW::Selenium) - Like WebDriver (Ruby), Selenium (Python), Nightwatch.js (JavaScript), Nightwatch.js/Puppeteer (JavaScript)
- **Minify JavaScript** - [JavaScript::Packer](https://metacpan.org/pod/JavaScript::Packer) - Like Uglifier (Ruby), jsmin (Python), minify (JavaScript)
- **Minify HTML** - [HTML::Packer](https://metacpan.org/pod/HTML::Packer) - Like html_minifier (Ruby), minify-html (Python), HTMLMinifier (JavaScript)
- **Minify CSS** - [CSS::Packer](https://metacpan.org/pod/CSS::Packer) - Like cssmin (Ruby), minify (JavaScript)
