---
layout: post
title: 'Find all Text Files, recursively'
tags:
  - bash
  - hacked
  - programming
  - shortcut
  - simplification
  - snippet
categories:
  - linuxunix
  - shell
  - software
  - unix

---

Because I was thinking of something like that for a long time.



In bash/zsh (add it to your  `.rc` ):



{% highlight bash %}
textfiles ()
{
    file $(find $*) | /bin/grep -E 'text|empty' | cut -d ':' -f1
}
{% endhighlight %}



Using this function it's possible to open all text files of a project at once:



{% highlight bash %}
kate $(textfiles project/*)
{% endhighlight %}


