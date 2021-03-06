# API Helper for Shopify docs

![API Helper for Shopify logo](images/api-helper-for-shopify-logo.png)

The [API Helper app for Shopify](https://apps.shopify.com/api-helper) is available here for install from the Shopify App Store with modules starting at $2 / month. Read more about the app here on Medium.

API Helper simplifies AJAX email sign ups and discount code creation for Shopify. The app provides a secure frontend API that provides access to important functions from [Klaviyo](#modules), [Mailchimp](#modules), [Omnisend](#modules) and [Shopify](#modules) that are not accessible due to CORS policies inside of Shopify themes. [Jump to docs](#modules)

API Helper provides a simple callback and standard response structure that makes life so much easier. API Helper also allows for plug-and-play or 'hot swap' customer sign-ups between Klaviyo, Mailchimp, Omnisend, and Shopify.

There are no scripts required to use the app. After enabling your first app module inside of the app, our js file from the API Helper app is injected into your theme at the end of page load. This file is __1.6KB__ and served from Google's CDN. The file is removed immediately when the app's modules are disabled or the app is uninstalled.

## Getting Started

1. Enable your desired modules in the app admin on Shopify
2. Save your API keys (if applicable)
3. Review the docs for the [modules](#modules) below. Just copy/paste the example code into your theme and you are ready to go. You can also paste the code directly into your browser console for testing.
4. Follow our newsletter subscription screencast [here on Youtube](https://www.youtube.com/watch?v=Bl-TfmwawUU).

## Example Code
```
var options = {
  vendor: 'klaviyo-subscribe',
  action: 'subscribe',
  email: 'foo@google.co',
  list_id: 'jWks87j',
  signup_location: 'footer'
}
wb_apihelper(options, function(err, res){
  if ( err ) return alert(res.message)
  console.log(res)
})
```
![API Helper for Shopify Klaviyo subscribe](images/api-helper-for-shopify-klaviyo-subscribe.gif)
![API Helper for Shopify generate unique discount code](images/api-helper-for-shopify-theme-generate-discount.gif)
## Shopify Admin
![API Helper for Shopify admin](images/api-helper-for-shopify-admin.gif)

## Modules
Modules starting at $2 / month. Each module includes all `action` components shown below. For example, the Klaviyo module costs $3 / month and gives you access to the `subscribe, unsubscribe, backinstock, track, identify` actions.
### Klaviyo - $3 / month
* [subscribe](/Klaviyo/subscribe.md)
* [unsubscribe](/Klaviyo/unsubscribe.md)
* [backinstock](/Klaviyo/backinstock.md)
* [track](/Klaviyo/track.md)
* [identify](/Klaviyo/identify.md)
* [API key instructions](/Klaviyo/instructions.md)
### Mailchimp - $3 / month
* [subscribe](/Mailchimp/subscribe.md)
* [unsubscribe](/Mailchimp/unsubscribe.md)
* [API key instructions](/Mailchimp/instructions.md)
### Omnisend - $3 / month
* [subscribe](/Omnisend/subscribe.md)
* [unsubscribe](/Omnisend/unsubscribe.md)
### Shopify \- Subscribe - $2 / month
* [subscribe](/Shopify/Subscribe/subscribe.md)
* [unsubscribe](/Shopify/Subscribe/unsubscribe.md)
### Shopify \- Discount - $2 / month
* [discount](/Shopify/Discount/discount.md)
### Google UTM Params
* [BONUS: utm params](/utms.md)
