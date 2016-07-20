# Dokku Notify Curl

## Usage

1. Install it
2. Configure it: `dokku config:set --global DOKKU_NOTIFY_URL=https://example.com/whatever/path`.
3. It'll `POST` on the given url this:

```json
{
  "revision": "584b3ee15918fa74aeb6e4b97b07fc0f178b2e9b",
  "hostname": "fourcolor-bot-5",
  "public_ip": "139.59.210.80"
}
```

Disclaimer: in a real world it would send for example the url you could access
the app with. But we're doing it for a case where this url is meaningless, that's
why we look for the ip.
