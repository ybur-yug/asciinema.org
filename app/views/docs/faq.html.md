<% content_for(:title, 'FAQ') %>

# Frequently Asked Questions

## Can I embed the asciicast player on my blog?

Yes, see [embedding docs](<%= docs_path(:embedding) %>).

## How can I delete my asciicast?

In order to delete your asciicast you need to associate your local API token
(which was assigned to the recorded asciicast) with the asciinema.org
account. Just run `asciinema auth` in your terminal and open the printed URL
in your browser.  Once you sign in you'll see a "Delete" link on your
asciicast's page.

## Can I have my own asciinema site instance?

Yes, you can set up your own asciinema site. The source code of the app that
runs asciinema.org is available
[here](https://github.com/asciinema/asciinema.org).

When you have the site up and running you can easily tell asciinema client to
use it by adding following setting to _~/.config/asciinema/config_ file:

    [api]
    url = http://asciinema.example.com

Alternatively, you can set `ASCIINEMA_API_URL` env variable:

    ASCIINEMA_API_URL=http://asciinema.example.com asciinema rec

## Can I edit/post-process the recorded asciicast?

Yes, if you know how to deal with [ansi escape
sequences](https://en.wikipedia.org/wiki/ANSI_escape_code). Asciicasts are
self-contained JSON files which you can edit before uploading. Look at
`stdout` attribute in [asciicast format doc](https://github.com/asciinema/asciinema/blob/master/doc/asciicast-v1.md)
for inspiration.
