# emdash

Simple blogging with node/iojs + GitHub.

## Details

The project goals/plans include:

* simple node/iojs-based blog management system with minimal dependencies:
	- [asynquence](http://github.com/getify/asynquence): async flow control
	- (possibly) [native promise only](http://github.com/getify/native-promise-only): ES6 promise polyfill, for interaction with other libs, and/or to replace *asynquence*
	- [grips](http://github.com/getify/grips): html & css templating
	- [JSON.minify](https://github.com/getify/JSON.minify): removes whitespace/comments from JSON; lets you make human-friendly JSON config files
	- markdown rendering
	- git/GitHub/oauth
* no database:
	- data persistence is either local or remote
	- git/GitHub/gist
* user/auth is GitHub accounts
* post content:
	- authored in markdown
	- stored/versioned in git/GitHub/gist
	- publishing can be "staged" via git branching
	- automation handled via git hooks
	- by default, all posts can be "forked" from the blog software with a "fork this" button on post; allows access to source markdown to any user
* comments:
	- authored in markdown
	- stored/versioned in git/GitHub/gist
	- (admin) comment approval workflow promotes store to static cache file (per post)
* simple html/text and css templating:
	- simple default theme(s)
	- custom themes easy
* incremental/partial caching in static files
* static site publishing (optional)
	- command-line tool to "build" site of static files
	- static files can be automatically pushed to gh-pages or other remote FTP/SCP target
* site architecture:
	- simple "middle end" adaptive hybrid techniques
	- server-side templating renders initial page view
	- client-side templating takes over, renders all pages SPA-style
	- client performance monitoring, middle-end can disable client-side rendering and fall back to server-side if needed
* admin tools:
	- permissions driven by GitHub user settings
	- all settings changes made either alter the code or JSON config files
	- blog authoring can (should) be done externally, and admin tools just ingest/publish from git/GitHub/gist source

## License

The code and all the documentation are released under the MIT license.

http://getify.mit-license.org/
