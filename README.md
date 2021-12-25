# passport-dingtalk2

dingtalk authentication strategy for passport  

[新版获取登录用户的访问凭证](https://open.dingtalk.com/document/orgapp-server/obtain-identity-credentials)


using the OAuth 2.0 API.  
使用OAuth 2.0 API


## Installation

    $ npm install passport-dingtalk2

## Usage
    passport.use(new dingtalkStrategy({
        clientID: client_id,
        clientSecret: client_secret,
        callbackURL: "http://127.0.0.1:3000/auth/dingtalk/callback"
      },
      function(accessToken, refreshToken, profile, done) {
        User.findOrCreate({ Id: profile.id }, function (err, user) {
          return done(err, user);
        });
      }
    ));
## License

The MIT License

