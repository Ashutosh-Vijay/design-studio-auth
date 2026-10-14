# Design Studio sign-in clients

The Anypoint Connected Apps that [Design Studio](https://ashutosh-vijay.dev) signs in with, one per Anypoint cloud.

A desktop app can't keep a secret, so these are public on purpose. Each sign-in also needs a one-time PKCE value that never leaves the user's machine, and Anypoint only sends sign-ins back to `localhost`, so a copy of these can't be used to take anyone else's sign-in.

`clients.json` is updated by the app's rotation script when an org is renewed. The app reads it at startup and keeps the last good copy.
