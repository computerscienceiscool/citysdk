# Census API Docs for Javascript

Documentation, examples, guides primarily focused on using the Census API in frontend and backend Javascript applications by unitizing the CitySDK library.

Built on [uswds-jekyll](https://github.com/18F/uswds-jekyll)

---

## Development

If you have ruby + gems installed run the following

1. Fetch gems by running

```bash
bundle
```

2. Run Jekyll in development

```bash
jekyll serve --config _config.yml,_config_development.yml
```

#### Using Docker

```bash
docker build . -t citysdk-pages
docker run -p 4000:4000 -it --mount type=bind,source=$(pwd),target=/usr/app/ citysdk-pages
```

If you have Docker Compose

```bash
docker-compose up
```

Access the site at [http://0.0.0.0:4000/](0.0.0.0:4000)
---

#### Other notes

When adding images or assets make sure to include relative_url. This is so baseurl works for github pages.

```
{{ '/assets/something.png' | relative_url }}
```

To update ./assets/citysdk.js

```
cd assets
npm install
npm update citysdk
npm run build
```

Test by opening `./assets/browser-dist.html`

---

If you would like to add features and content, report an issue, or suggest changes submit a pull request on Github.