# Starting Perl in 2020

> How to quickly set up a development environment and learn modern Perl with best practices.

## Why Perl

Why learn Perl in 2020? Unlike Ruby it's installed on pretty much any box you log in to, so you can use it like a faster and more portable version of bash scripting. Unlike Python or Go it has [great support for functional programming](https://hop.perl.plover.com/book/). Unlike JavaScript, the ecosystem is stable so you avoid framework churn. It has a proven track record of 40 years, so you're bound to run into it somewhere. Many best-in-class tools are written in Perl, like the famous [exiftool](https://exiftool.org/). It's one of the [highest paid programming languages](https://fossbytes.com/stack-overflow-highest-salary-programming-languages-2020/).

Perl has a strong presence in web development, system administration, and data science. It has unique security features like ["taint checking"](https://en.wikipedia.org/wiki/Taint_checking) that can prevent malicious users from executing commands in your application. It's string manipulation and regex capabilities are unparalleled. It will give you deep insight into the world of Unix, since it was made to work with command line tools and builds on the heritage of Sed and Awk. If you're familiar with C style languages like C++, JavaScript, PHP, Go, or Java, the syntax will mostly feel familiar. There is a massive and growing collection of modules available on [CPAN](https://metacpan.org/). And since Perl has a deep testing culture, the signal:noise ratio is much higher than you'd find on NPM.

## IDE

[Visual Studio Code](https://code.visualstudio.com/) makes for a great modern Perl IDE. Here are the main extensions that will make your life easier.

- [Perl](https://marketplace.visualstudio.com/items?itemName=richterger.perl) - Language server and debugger. Has syntax checking, code completion, goto definition, and find references.
- [perltidy-more](https://marketplace.visualstudio.com/items?itemName=Kaktus.perltidy-more) - Automatic code formatter.
- [Perl Toolbox](https://marketplace.visualstudio.com/items?itemName=d9705996.perl-toolbox) - Static analysis tool with linting provided by [Perlcritic](https://github.com/Perl-Critic/Perl-Critic).
- [Better Perl Syntax](https://marketplace.visualstudio.com/items?itemName=jeff-hykin.better-perl-syntax) - Great syntax highlighting.

## Perl version manager

[Perlbrew](https://perlbrew.pl/) let's you have multiple Perl versioned installed at once, and keep their CPAN packages separate. This way you can use a different Perl for different projects withoug them interfering with each other. These are equivalent to Python's [pyenv](https://github.com/pyenv/pyenv), Ruby's [rbenv](https://github.com/rbenv/rbenv), Node's [nvm](https://github.com/nvm-sh/nvm), or the multi-language [asdf-vm](https://asdf-vm.com/). To install run:

```bash
\curl -L https://install.perlbrew.pl | bash
```

Follow the post-install instructions at the prompt to add `source ~/perl5/perlbrew/etc/bashrc` to your `~/.bash_profile` or `~/.zshrc`. Then run:

```bash
perlbrew available
perlbrew install perl-5.xx.x #replace with latest version shown
```

Then run `perlbrew init`, and `perl --version` to make sure you are running the latest version.

## Package manager

Perl packages are called modules, and you can find them on [CPAN](https://www.cpan.org/). The main package manager is called [cpanminus](https://github.com/miyagawa/cpanminus). To install it run:

```bash
perlbrew install-cpanm
```

## REPL

To install a Perl REPL run this command:

```bash
cpanm App::perlsh
```

## Books

Perl's not on a hype cycle right now, so you can snag all of its best books for bargain prices. And because Perl is a really stable language, the're still relevant. A lot of these books are even free online. But paper books have great information density, you can quickly look things up with their index, and they help you get away from the computer screen for a bit.

- [Beginning Perl](https://www.goodreads.com/book/show/13837737-beginning-perl) - A comprehensive reference and modern introduction to Perl.

- [Effective Perl Programming, 2nd edition](https://www.goodreads.com/book/show/946128.Effective_Perl_Programming) - A list of expert tips that will have you quickly writing great Perl code. This is to Perl what the legendary "Effective C++" is to that language.

- [Modern Perl, 4th edition](https://www.goodreads.com/book/show/10198038-modern-perl) - A short book to quickly bring you up to speed on modern best practices Perl. Also available online [for free](http://modernperlbooks.com/books/modern_perl_2016/index.html).

- [Programming Perl, 4th edition](https://www.goodreads.com/book/show/154155.Programming_Perl) - The official reference. It's a massive tome and you can get it for \$10.

- [Higher Order Perl](https://www.goodreads.com/book/show/86365.Higher_Order_Perl) - A classic book on functional programming in Perl. More relevant than ever with the rise of multi-core CPUs. Also available online for [for free](https://hop.perl.plover.com/book/).

- [Mastering Perl, 2nd edition](https://www.goodreads.com/book/show/583634.Mastering_Perl) - Advanced techniques for the working Perl programmer, like secure programming techniques, debugging, profiling, benchmarking, configuration, logging, and error reporting.

## Docs

Simply add the Perl docset to one of these apps for

- [devdocs.io](https://devdocs.io) - free web app
- [Zeal](https://zealdocs.org/) - free desktop app
- [Dash](https://kapeli.com/dash) - paid Mac app

## Getting Help

There are active communities on [Discord](https://discord.com/invite/Mnbj6th) and [Reddit](https://reddit.com/r/perl/). For IRC the two main options are #perl on FreeNode #perl (irc.freenode.net) and #perl-help on [irc.perl.org](https://www.irc.perl.org/). Everyone is really friendly and helpful, so don't hesitate to swing by. If you need an IRC program to connect with try [HexChat](https://hexchat.github.io/) for Linux/Windows or [LimeChat](http://limechat.net/mac/) for Mac.

## News

[Perl Weekly](https://perlweekly.com/latest.html) is a popular curated news source. You can subscribe by email or visit the website directly.
