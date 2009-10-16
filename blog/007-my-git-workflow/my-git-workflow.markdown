{{
title: My Git Workflow
published-on: 2009-10-15 21:59:19
summary: "Recently at work we've taken a giant leap forward in our software stack: We ditched CVS and are riding the [git](http://gitscm.org) bandwagon.\n\n
And oh what a pretty red wagon it is. Drawn by the big Clydesdales with fancy harnesses. In this article I aim to show the workflow I've been using that I feel will help other people just getting in to git."
tags:
  - Git
  - "Version Control Systems"
}}

### What's this "git" you speak of?

Just a small caveat: if you already know what git is, or if you don't care about how I got into git, [skip ahead](#workflow). Sometimes I'm boring and I can't help it.

Git's been coming along nicely for the last few years gaining all sorts of popularity in the face of Subversion's apparent lead, and CVS's mind-boggling IE6-like stranglehold on the Version Control Systems universe. A lot of the current fervor attributed to git is attributed to several popular open source projects changing their SCM from Subversion to Git, most notably (for me at least) [Ruby on Rails][rails] and their switch to [Github][rails-github].

I'll admit that I had no idea who or what git was until mid-2008 when a co-worker of mine told me he wanted to get into it (no pun intended). I was in my nice cozy comfortable Subversion shell at the time and thought how could one possible want anything more than SVN? Ironically, after using git for the past year or so, I'm thinking the same thing from the git perspective. *How in the world* are people still using SVN (assuming they have the choice)? Ya, I don't know either.

Due to much of git's current popularity coming from the Rails switch, a lot of the git info you read online comes from people doing stuff in [Ruby][ruby]. This was certainly my main usage of git after I finally took the plunge late last year, using it to manage the version control of all my Rails/Sinatra projects. Of course, with any VCS, the content you are versioning need not be a specific software project at all. You could use it to version your photoshop design files if you wanted to.

### How sweet it is to be loved by git

Anyways, at work we use Java. And up until about a month ago, we were using CVS to manage our software versioning. We've been doing a great round of tech discussions to improve our stack, and the CVS to Git migration was one of the first targets we moved against, due to the relatively simple nature of the change. I've got to credit [Ben][] for randomly deciding to demo git to everybody in one meeting. I just let him run with it, though I probably know git a lot better. By the end of the meeting we were all like, "Okay, so when do we start using it?". I was floored. I thought for sure there'd be reservations and assumed that if we ever did get off of CVS it'd be to Subversion. Well, just a few short weeks later we had imported our entire repo into Git (approximately 900 mb). A few weeks after that, we were completely dependent on git for our VCS of choice. And boy does it feel sweet.

Not a day goes by when *someone* in dev just randomly exclaims, "How freaking sweet is Git?!", or, "Git is just so fast!". I love hearing this stuff, cause it reinforces my belief that git really is a superior VCS. It brings some passion back into what we do each day. A software developer's tools should always enhance their ability to put out great software. Git does just that.

Okay, so that was the boring back story, here's some of the meat of git that we've been working with. Most of these concepts were taken in one form or another from the [Git Workflow manpage][workflow]. 

<a name="workflow"></a>
### Topic Branches

The best thing I pulled from the git workflow article is the concept of the **topic branch**. In git, branching doesn't create new filesystem directories, it just magically handles it all in the cloned repository. This was a huge upgrade from CVS and even Subversion in my opinion. It's one of the biggest reasons I love git so much. Branching is cheap, therefore much more useful.

Topic branches aren't a special kind of branch, it's just a way of thinking about how to use branches for effective project development. Git creates a default branch for your trunk or mainline of development and calls it "master". Each time the project manager assigns me a project (in this case say the project is called "widget"), I follow this workflow:

<script src="http://gist.github.com/211594.js"></script>

**How do you manage your projects with git?**

  [ruby]: http://ruby-lang.org "Ruby the programming language"
  [rails]: http://rubyonrails.org "Ruby on Rails"
  [rails-github]: http://www.github.com/rails/rails "Rails on Github"
  [Ben]: http://benmatz.wordpress.com "Ben"
  [workflow]: http://www.kernel.org/pub/software/scm/git-core/docs/gitworkflows.html "Git workflow suggestions"