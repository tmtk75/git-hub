README
======
git extension for [github](http://github.com/)

*You don't have to dig into source tree by click and click anymore.*

Easy to view each page of github from command line
as you can directly open the page you want.

Especially, blob and commit of me are two of powerful sub-commands.
For instance,
if you develop in Java, you have many POM files like server/pom.xml, client/pom.xml,
tools/pom.xml and so on. 

If you want to see one of them, then you can type like

    $ git hub blob pom.xml

And I'll say like

    INFO: more than two lines matched like
         1  client/pom.xml
         2  server/pom.xml
         3  tools/pom.xml
    --(snip)--
    please try specifying index to select like

      git hub blob pom.xml:2

If you want to see server/pom.xml, as the suggssion,
you type again adding ":2" which is the index of server/pom.xml.
So your default browser will open the page of server/pom.xml on github.com.

Furthermore, commit is similar, too. commit is the sub-command to see a change of file.

    $ git hub commit pom.xml
    INFO: more than two lines matched like
         1  client/pom.xml
         2  server/pom.xml
         3  tools/pom.xml
    --(snip)--

    $ git hub commit pom.xml:2

Until here, it's same to blob.

commit says following.

    INFO: more than two lines matched like
    Specify a ref with index like, git hub commit pom.xml:2:3
        1  5525ace - Tomotaka Sakuma  9 days ago - update pom version
        2  b76b161 - Tomotaka Sakuma  9 days ago - minor change
        3  423771d - Tomotaka Sakuma  12 days ago - add comment
        4  a66cd2a - Tomotaka Sakuma  2 weeks ago - minor change
        --(snip)--

It shows all changes of server/pom.xml with ref, author name, relative commit time and commit log.
So you can type like this if you want to see the change 12 days ago, which is index 3.

    $ git hub commit pom.xml:2:3

Your default browser will open the diff page of github.com.
You can certainlly jump to another related pages from the page.
 

Do you think it's a bit useful?


But sorry for MacOS only now =)


INSTALL
-------
set PATH to git-hub

    $ sudo curl https://raw.github.com/tmtk75/git-hub/master/git-hub > /usr/local/bin/git-hub
    $ chmod +x !$

or

    $ git clone git://github.com/tmtk75/git-hub.git ~/.git-hub
    $ PATH=$PATH:~/.git-hub
    $ git hub


LICENSE
-------
MIT License
