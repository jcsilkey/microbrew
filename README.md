# Microbrew
Microbrew is a lightweight wrapper around [Homebrew](http://brew.sh) that will look for a configuration file named PREFIX/etc/homebrew/homebrew.yaml (where PREFIX/bin is where you install microbrew) and load it before invoking Homebrew. It started as a feature proposal to add this functionality natively to Homebrew (currently the only way to configure options for Homebrew is via environmental variables).

## Usage
Currently you must manually install the file into your path.

1. Install it into your path - I recommend putting it in HOMEBREW_PREFIX/bin (/usr/local by default).
2. Create a `homebrew` directory in the etc directory under the same prefix you installed microbrew. For example, if you installed microbrew to `/usr/local/bin/microbrew`, you would create the directory in `/usr/local/etc/homebrew`.
3. Create a file named homebrew.yaml in the directory you created in Step #2. As the name suggests, this file should be in [YAML format](http://www.yaml.org/spec/1.2/spec.html). A config file might look something like:

```
---
HOMEBREW_BOTTLE_DOMAIN: 'http://www.google.com'
HOMEBREW_NO_EMOJI: 1
```

As of this time, these are the settings I know of (list compiled from the brew manpage):

- HOMEBREW_ARTIFACT_DOMAIN
- HOMEBREW_AUTO_UPDATE_SECS
- HOMEBREW_BOTTLE_DOMAIN
- HOMEBREW_BROWSER
- HOMEBREW_BUILD_FROM_SOURCE
- HOMEBREW_CACHE
- HOMEBREW_CURL_VERBOSE
- HOMEBREW_DEBUG
- HOMEBREW_DEBUG_INSTALL
- HOMEBREW_DEBUG_PREFIX
- HOMEBREW_DEVELOPER
- HOMEBREW_EDITOR
- HOMEBREW_GITHUB_API_TOKEN
- HOMEBREW_INSTALL_BADGE
- HOMEBREW_LOGS
- HOMEBREW_MAKE_JOBS
- HOMEBREW_NO_ANALYTICS
- HOMEBREW_NO_AUTO_UPDATE
- HOMEBREW_NO_EMOJI
- HOMEBREW_NO_INSECURE_REDIRECT
- HOMEBREW_NO_GITHUB_API
- HOMEBREW_SVN
- HOMEBREW_TEMP
- HOMEBREW_VERBOSE
