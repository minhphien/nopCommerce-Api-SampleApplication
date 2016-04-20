# nopCommerce-Api-Authorization

In this sample project we have demonstrated how clients can authorize and obtain Access/Refresh tokens that can be used to access the nopCommerce Web API, which is available as a plugin and provides a RESTful API to various resources in nopCommerce i.e Customers, Categories, Products, Shopping Cart Items, Orders. The nopCommerce Web API plugin is available for nopCommerce 3.70 and could be found in this repo - https://github.com/SevenSpikes/nopCommerce/tree/Web-Api-3.70

nopCommerce Web API plugin support OAuth 2.0 Authorization Code grant type. This grant type is suitable for server applications that want to have access to the Web API resources.

The standard Authorization Code Grant flow is described in Section 4.1 of the The OAuth 2.0 Authorization Framework - http://tools.ietf.org/html/rfc6749

Here is how the Authorization Code Grant Flow works in nopCommerce Web API.

1. The client application starts the flow by redirecting the user agent to the nopcommerce Web API authorization endpoint. 
2. The nopCommmerce authorization endpoint redirects the user agent back to the client application with an authorization code. The user agent returns authorization code to the client application’s redirect URI.
3. The client application requests an access token from the nopCommerce token issuance endpoint by presents=ing the authorization code that has just received.
4. The nopCommerce token issuance endpoint returns an access token and a refresh token. The refresh token can be used to request additional access tokens.
5. The client application uses the access token to authenticate to the Web API.
6. After authenticating the client application, the Web API returns the requested data.



