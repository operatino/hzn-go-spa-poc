# Horzion GO Web SPA POC

POC of Single Page Application architecture for current Horozion GO web (AEM based).

## Start

```
npm run dev
```

or for running with SSL for faking horizon.tv domain origin:

```
sudo npm run dev:ssl
```

## Faking horizon.tv

Use Firefox with [this addon](https://addons.mozilla.org/en-US/firefox/addon/cors-everywhere/). This will allow adressing OESP from `localhost`

OR

Update `/etc/hosts` to:

```
127.0.0.1   localhost horizon.tv www.horizon.tv
```

then run `sudo npm run dev:ssl` and open https://www.horizon.tv (which will lead to locally running version). Don't forget to revert `hosts` file after you finished ;)

## Certificates

```
openssl req -x509 -newkey rsa:4096 -keyout key.pem -out cert.pem -days 365 -nodes
```

Enter random answers to questions.