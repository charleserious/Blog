# Web Authentication API

## What/是什么

Web Authentication API简称为WebAuthn，是FIDO联盟指导下的FIDO2项目的核心组成部分，是一项由万维网联盟(W3C)发布的Web标准，是一种去密码化的用于登录网站/应用的一种验证实现，它使用[公钥密码学（非对称加密）](https://en.wikipedia.org/wiki/Public-key_cryptography)使得验证更强壮，不需要短信验证码就能实现无密码验证和安全的双因素验证（两步验证登录）。  

## Why/为什么

解决了[网络钓鱼/Phishing](https://en.wikipedia.org/wiki/Phishing)，[数据泄漏/Data breaches](https://en.wikipedia.org/wiki/Data_breach)，[短信验证码伪装](https://en.wikipedia.org/wiki/SMS_spoofing)，或其它[双因素验证](https://authy.com/what-is-2fa/)的重大安全问题，同时显著提高易用性，从此用户不必管理各种越来越复杂的密码。

## How/怎么做

![Entities](https://webauthn.me/img/1-Web-Authentication-Entities.svg)

上图中包含四类实体，验证者/Authenticator、用户/User、用户代理/User Agent(e.g. Browser)、依赖方(服务方)/Relying Party，这四个实体在两个单独的用例中协同工作：注册和身份验证。图中不同实体之间的所有通信都由用户代理（通常是Web浏览器）处理。

### Registration/注册

注册用例：注册使用验证者创建一组新的公钥证书，可用于签署依赖方生成的质询。 这些新凭证的公共部分以及签名的质询可以发送回依赖方进行存储。 随后，依赖方可以在需要时使用这些凭证来验证用户的身份。

![Registration](https://webauthn.me/img/2-Registration.svg)

### Authentication/身份验证(e.g. 登录)

登录用例：相反，身份验证允许依赖方向验证者发送质询。 然后可以使用先前生成的公钥证书对该挑战进行签名，并将其发送回依赖方。 这样，依赖方可以验证用户是否拥有所需的凭证，从而证明其身份。

![Authentication](https://webauthn.me/img/3-Login.svg)

## Glossary/名词解释

## Reference/引用

- [WebAuthn Guide](https://webauthn.guide/)

- [WebAuthn Introduction](https://webauthn.me/introduction)

## Demo

- Mozilla: [WebAuthn Checker](https://webauthn.bin.coffee/)

- Google: [WebAuthn Demo](http://webauthndemo.appspot.com/)

- WebAuthn [webauthn.io](https://webauthn.io/)

- Authn0: [Authn0](https://webauthn.me/)

![Security Key](https://www.yubico.com/wp-content/uploads/2018/04/Security-Key-by-Yubico-nl-opt.png)

![Security Key NFC](https://www.yubico.com/wp-content/uploads/2018/12/Security-Key-by-Yubico-ec-hero.png)