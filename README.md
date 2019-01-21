# quick301
## the stupidest url shortener

go away, yourls, polr and similar things. shorten urls by adding 301 redirects to your nginx config.

### usage
+ first do `quick301 --deploy` and put the output in the right place of your nginx configuration (a place where a bunch of `location` directives would fit within your server block)
+ then do `quick301 --file /etc/nginx/sites-available/your-config --target https://youtu.be/J---aiyznGQ --link cat`
+ you now have a working shortened url. run quick301 again only specifying the `--file` argument to get a list of shortlinks already set.

### to do
+ use a proper tool like [python-nginx](https://github.com/peakwinter/python-nginx) to parse nginx config files and not this shit
+ check if entries already exist
+ if possible, find servername and output it with the link at the end
