# DansPhotos
throwaway to work out porcess to make Dan's website

Step one:
- create a repo by clicking 'new' on 'my repos' page
   - name it DansPhotos
   - describe it thowaway ...
   - :check: public
   - :check: readme
   - :check: .gitignore
      - elixir

Edit Readme via webinterface to include step one info, and commit to main branch

Step 2:
Note some of the following tasks may be able to be performed from IDE instead of Terminal command line
- fork repo by clicking fork in upper right hand corner
   + this creates github copy (fork) of your own
- on your forked repo, click on green "code" button dropdown, and copy the link by clicking on the little clipboard
   + should put something like https://github.com/sparrell/DansPhotos.git in copy buffer
- open terminal window and cd to directory where you will keep your development (eg "mkdir MyDev", "cd MyDev")
- git clone "whatever in paste buffer eg https://github.com/sparrell/DansPhotos.git" # this creates a local copy of what in github
   + understand the difference between forking (how you made your github copy of repo) and cloning (how hou made your local copy of your github repo)
- git status #shows which 'branch' you are on (probably "main")
- git checkout step2 #switches to step2 branch
- edit readme in IDE to put in these comments
- git commit -m "step 2". # commit these changes to local copy of repo
- git push # push the commits to github
- look on github and see branch step3 has these changes
- make a pull request - ie request these changes be put in original github that your github repo was forked from

Step 3
- install homebrew if not already on mac
   * https://brew.sh/
- use brew to install elixir
   * https://elixir-lang.org/install.html
   * brew update
   * brew install elixir
   * should install erlang as well
- install phoenix
   * mix local.hex
   * mix archive.install hex phx_new 1.5.7
   * install node.js https://nodejs.org/en/download/
      - ???brew install node ??? or node.js?
   * install postgreSQL https://wiki.postgresql.org/wiki/Detailed_installation_guides
      - * ???brew install postgresql ??? + turn it on?
- phoenix up and running
   * https://hexdocs.pm/phoenix/up_and_running.html
   * NOTE - this is install without liveview. doing over using liveview is a later step
   * mix phx.new $WHATNAME
      - type Y to install dependencies
      - figure out .gitignore per webpage
   * cd $WHATNAME
   * ?? configure your database in config/dev.exs
   * mix ecto.create
   * Start your Phoenix app with either of
      - mix phx.server # foreground
      - iex -S mix phx.server # interactive elixir shell for developemnt
      - ? # in background
