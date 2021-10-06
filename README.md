> How to implement Web Push Notifications with live demo and instructions: https://push-notifications-demo.netlify.app/

![A push notificatin][pushNotificaiton]

[pushNotificaiton]: https://github.com/vctrtvfrrr/push-notification/raw/master/push-notification.jpg "Push notification"

# push-notifications-test

This mono-repo project is a demo for this article https://itnext.io/an-introduction-to-web-push-notifications-in-javascript-a701783917ce

The project is composed by two parts: 

* a front end written is HTML + JavaScript 

* a back end written in JavaScript + NodeJS

## Run locally

### font-end

```
cd front-end 
npm install 
npm start
```
Next, open http://localhost:9000. 

### back-end

```
cd back-end
npm install
export CORS_ORIGIN=http://localhost:9000 && node src/server.js
```

`export CORS_ORIGIN=http://localhost:9000` means: accept Cross Origin call from this host. 

## deploying to your server

If you want to deploy the front-end to your server remember to modify the back-end host in the webpack config file: `webpack.config.prod.js`: `'process.env.PUSH_SERVER_URL': JSON.stringify('https://push-notifications-test-server.herokuapp.com'),`
