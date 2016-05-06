# Remote Login UserManager for OctoPrint

## Install

pip install octoprint_remoteauth

## Usage

Change userManager in config file and add a key remoteAuthCheckPasswordUrl pointing to a url,
which supports a POST request with fields *username* and *password*. Response 200 = login

config.yaml

```yaml
accessControl:
  userManager: octoprint_remoteauth.RemoteAuthUserManager
  remoteAuthCheckPasswordUrl: https://url_to_login_post_api
```