# spring-rest-api-oauth2

What is OAuth2?
OAuth2 is an standardized authorization protocol/framework.

The OAuth 2.0 authorization framework enables a third-party application to obtain limited access to an HTTP service, either on behalf of a resource owner by orchestrating an approval interaction between the resource owner and the HTTP service, or by allowing the third-party application to obtain access on its own behalf.

Spring Security OAuth project provides all the necessary API we might need in order to develop an OAuth2 compliant implementation using Spring. 

1. OAuth2 Roles
OAuth2 defines four roles:

resource owner:
Could be you. An entity capable of granting access to a protected resource. When the resource owner is a person, it is referred to as an end-user.
resource server:
The server hosting the protected resources, capable of accepting and responding to protected resource requests using access tokens.
client:
An application making protected resource requests on behalf of the resource owner and with its authorization. It could be a mobile app asking your permission to access your Facebook feeds, a REST client trying to access REST API, a web site [Stackoverflow e.g.] providing an alternative login option using Facebook account.
authorization server:
The server issuing access tokens to the client after successfully authenticating the resource owner and obtaining authorization.

2. OAuth2 Authorization Grant types
An authorization grant is a credential representing the resource owner’s authorization (to access its protected resources) used by the client to obtain an access token. The specification defines four grant types:

authorization code
implicit
resource owner password credentials
client credentials

3. OAuth2 Tokens
Tokens are implementation specific random strings, generated by the authorization server and are issued when the client requests them.

Access Token : Sent with each request, usually valid for a very short life time [an hour e.g.]
Refresh Token : Mainly used to get a new access token, not sent with each request, usually lives longer than access token.

4. OAuth2 Access Token Scope
Client can ask for the resource with specific access rights using scope [want to access feeds & photos of this users facebook account], and authorization server in turn return scope showing what access rights were actually granted to the client

![image](https://user-images.githubusercontent.com/30445249/235386746-780298e3-0a8f-43bb-bfa4-ac5486ce0ef8.png)

![image](https://user-images.githubusercontent.com/30445249/235393430-f80d3c2e-d61b-48e6-911c-17724b19e08c.png)

