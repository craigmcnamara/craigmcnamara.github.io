---
layout: post
title:  Clean feature branches using git-rebase
date:   2019-10-04 21:22:37 -0700
categories: rails git development-tips
---

WIP Outline

* Rebase is better than merging master
* Make separate commits of lockfiles and generated artifacts
* Deal with merge conflicts progressively instead of all at once.


Keeping long running git branches in a modern web application environment can be challenging. Keeping things up to date with the master branch can seem like a whole project over time.

The biggest challenge is code that changes in both sides of the merge. This challenge is exacerbated by package manager lock files and database scemas that support the testing code.

In a modern Ruby on Rails application you have package managers with lock files, ex: `Gemfile.lock, yarn.lock, package-lock.json`, `db/structure.sql` or schema files `db/schema.rb`

{% highlight shell %}
$ git rebase
{% endhighlight %}
