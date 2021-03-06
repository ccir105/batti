# batti [:link:][web]

load-shedding information.

![screenshot][screenshot]

![Creative Commons Attribution 3.0 Unported License](http://i.creativecommons.org/l/by/3.0/88x31.png)

batti Copyright © 2013 to the batti Authors.

___


#### Setting up

batti depends upon [2utf8][2utf8] to process non-unicode data,
which is now included in git [sub-module][submodule].


```bash

    $ git clone https://github.com/foss-np/batti
    $ cd batti
    $ git submodule init
    $ git submodule update
```


**Tip**: Add `alias batti="/path/to/batti/main.sh"` to your *.bashrc* so you can run `$ batti -g [GROUP_NO]`


#### HOW-TO USE

```bash
Usage: 	batti -g [1-7] [OPTIONS]
	-a | --all	Show All [default]
	-g | --group	Group number 1-7
	-t | --today	Show today's schedule [uses with group no]
	-w | --week	Show week's schedule
	-u | --update	Check for update [ignores extra options]
	-s | --sparrow	Check for update from loadshedding.sparrowsms.com
	-x | --xml	Dump to xml
	-h | --help	Display this message
```
**Tip**: Put `alias nea="batti -g YourGroupNumber -t"` in your .bashrc so that you can simply get todays schedule for your group by typing `nea`. 
___

#### Plugin & Extension

##### **[conky-forever][conky-forever]**:

To add plugin to [conky-forever][conky-forever] after installation run do the following.

```bash
	$ echo "_conky_forever=/path/to/conky-forever" >> path.config
	$ ./conky_plugin.sh [GROUP_NO]
```

##### **[Unity Indicator][unity]**

The applet for unity is made by the [samundra][samundra] as [Nepal-Loadshedding-Indicator][unity]

##### **Conky[:link:][conky]**

This plugin makes use of [conky][conky] only. You can enable this plugin via
```bash
	$./conky_independent.sh -g 7 -m 1
```

___

#### HOW-IT Works

* Downloads schedule form [nea][nea]
* Extract schedule and put into `~/.cache/batti.sch`
* Processes your query

#### Similar works on github we found!

* [nls](https://github.com/xtranophilist/nls)
* [losh](https://github.com/hardfire/losh)
* [nepalloadshedding](https://github.com/leosabbir/nepalloadshedding)

[nea]: http://www.nea.org.np/loadshedding.html
[2utf8]: https://github.com/foss-np/2utf8
[conky-forever]: https://github.com/rhoit/conky-forever
[submodule]: http://git-scm.com/book/en/Git-Tools-Submodules
[web]: http://foss-np.github.io/batti/
[screenshot]: https://raw.github.com/foss-np/batti/gh-pages/images/screenshot.png
[unity]: https://github.com/samundra/Nepal-Loadshedding-Indicater
[samundra]: https://github.com/samundra/
[conky]: http://conky.sourceforge.net/
