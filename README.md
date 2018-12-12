
### Authoritarian overview

Authentication and authorization solution for microservices and the web

- [`authoritarian`](https://github.com/chase-moskal/authoritarian#authoritarian-overview) – node library for auth and user management
- [`authoritarian-client`](https://github.com/chase-moskal/authoritarian-client#authoritarian-overview) – browser ui library for login and user settings
- [`auth-server`](https://github.com/chase-moskal/auth-server#authoritarian-overview) – example standalone auth server
- ***[`auth-webapp`](https://github.com/chase-moskal/auth-webapp#authoritarian-overview) (you are here)*** – example microservice and frontend

---

# Example Auth Webapp

This example webapp has these components:

- **node api server**  
	uses `authoritarian` library to read and verify userTokens  
	does not talk to the `auth-server` at all  
	dishes out restricted content to privileged users

- **frontend ui**  
	uses `authoritarian-client` to allow login to obtain a userToken  

## `config.json`

```json
{
	"frontend": {
		"authConnection": {
			"host": "auth.chasemoskal.com",
			"post": 80
		}
	},
	"api": {
		"secrets": {
			"authKey": "~/auth-webapp/hs256.key"
		}
	}
}
```
