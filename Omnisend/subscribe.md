```
var options = {
  vendor: 'omnisend-subscribe',
  action: 'subscribe',
  email: 'foo@google.co',
  signup_location: 'footer'
}
wb_apihelper(options, function(err, res){
  if ( err ) return alert(res.message)
  console.log(res)
})
```
[Omnisend API key instructions](instructions.md) | [Example html](../example.html)
## Required `options`
* `vendor`
* `action`
* `email`
* `signup_location`

## Standard `options`
API Helper supports the following standard options. These options will be mapped to the appropriate location in Omnisend.
```
var options = {
  (...)
  first_name: 'Darryl',
  last_name: 'Strawberry',
  full_name: 'Darryl Strawberry',
  phone: '911',
  organization: 'GBY Ultralight',
  title: 'Lead Designer',
  address_1: '123 Street St',
  address_2: 'Unit A',
  city: 'Hermosa Beach',
  state: 'CA',
  zip: '90254',
  country: 'United States',
  timezone_iana: 'America/Los_Angeles'
}
```
\* `options.state`, `options.region` and `options.province` are interchangeable
## Custom Properties
You can pass any custom properties by key/value like below. These are popuplated as `Custom properties` in Omnisend.
```
var options = {
  (...)
  'Custom Property 1': 'foobar',
  'Custom Property 2': 'bananas'
}
```
