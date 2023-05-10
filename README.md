# bunnylol

Forked from [https://github.com/rithik/bunnylol](https://github.com/rithik/bunnylol). 

Tool that mimics the Facebook internally developed tool `bunnylol`. Currently, this is hosted on GitHub pages. 

A note: a lot of these commands are customized for me. It is probably most beneficial for you to fork this repo and add/remove commands so that it is optimized for commands you actually need.

## Example Commands

Command | Name | URL
--- | --- | ---
fb | Facebook | [https://facebook.com/](https://facebook.com/)
m | Messenger Desktop App | [messenger://](messenger://)
mw | Messenger Web | [https://www.messenger.com/](https://www.messenger.com/)
wa | WhatsApp Desktop App | [whatsapp://](whatsapp://)
waw | WhatsApp Web | [https://web.whatsapp.com/](https://web.whatsapp.com/)
gm | Gmail | [https://mail.google.com/mail/u/0](https://mail.google.com/mail/u/0)
gd | Google Drive | [https://drive.google.com/drive/u/0](https://drive.google.com/drive/u/0)
yt | YouTube | [https://youtube.com/](https://youtube.com/)
gh | GitHub | [https://github.com/](https://github.com/)
r | Reddit | [https://reddit.com/](https://reddit.com/)
ln | Linkedin | [https://linkedin.com/](https://linkedin.com/)
ig | Instagram | [https://instagram.com/](https://instagram.com/)
tw | Twitter | [https://twitter.com/](https://twitter.com/)
g | Google | [https://google.com/](https://google.com/)
wp | Washington Post | [https://www.washingtonpost.com/regional/](https://www.washingtonpost.com/regional/)
wsj | Wall Street Journal | [https://www.wsj.com/](https://www.wsj.com/)
cnn | CNN | [https://www.cnn.com/](https://www.cnn.com/)
n | Netflix | [https://netflix.com/](https://netflix.com/)
h | Hulu | [https://hulu.com/](https://hulu.com/)
pv | Amazon Prime Video | [https://www.amazon.com/Amazon-Video/b/?&node=2858778011&ref=dvm_MLP_ROWNA_US_1](https://www.amazon.com/Amazon-Video/b/?&node=2858778011&ref=dvm_MLP_ROWNA_US_1)
vs | VS Code | [vscode://](vscode://)
hs | Hubspot | [https://app.hubspot.com/live-messages/](https://app.hubspot.com/live-messages/)
$ | Robinhood | [https://robinhood.com/](https://robinhood.com/)
cal | Google Calendar | [https://calendar.google.com/calendar/r](https://calendar.google.com/calendar/r)
DEFAULT | Default - Google Search | [https://google.com/](https://google.com/)

## Setup

1. Open Chrome and click the three dots. Click `Settings` and scroll down to `Search Engines`.

2. Click `Manage Search Engines`.

3. Add a new search engine with the URL being `http://michalis-vitos.github.io/bunnylol?search=%s`.

4. Make this the default search engine.

## Adding a command

1. Run `npm install` so that `flow` (JavaScript type checker) can run.

2. Open up the `src/commands.js` file. Add your command to the `COMMANDS` object. You must include a `name` and `url` attribute and you can add an additional `searchurl` attribute if you would to be able to type a command like `yt NBA Highlights` (in which case, `bunnylol` will automatically search for NBA Highlights on YouTube).

3. Run `npm run prepublish`.

4. Publish to your website.

## Running locally

Since we use `import` module syntax, we need to run a server to bypass CORS issues. You can setup the server by running `npm install`, followed by `node server.js`. The server should be up and visible at `localhost:3000`.
