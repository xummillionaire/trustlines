function getData(json) {
  console.log(json)
}
bithompRequest("https://bithomp.com/api/v2/services", getData);
The above command returns JSON structured like this:

{
  "total": 467,
  "lastUpdate": 1579417546,
  "services": [
    {
      "name": "Bithomp",
      "domain": "bithomp.com",
      "socialAccounts": {
        "twitter": "bithomp",
        "youtube": "channel/UCTvrMnG-Tpqi5FN9zO7GcWw",
        "instagram": "bithomp"
      },
      "addresses": [
        {
          "address": "rsuUjfWxrACCAwGQDsNeZUhpzXf1n1NK5Z"
        },
        {
          "address": "rnk3N5hHnLS6nWncNh2R4D2ATiuEicjxXo"
        },
        {
          "address": "rhUYLd2aUiUVYkBZYwTc5RYgCAbNHAwkeZ",
          "name": "Bithomp activation"
        },
        {
          "address": "rBithomp3UNknnjo8HKNfyS5MN4kdPTZpW"
        },
        {
          "address": "rBithomp4vj5E2kUebx7tVwipBueg55XxS",
          "name": "Bithomp donations"
        },
        {
          "address": "rBithompKtixswR4bknJqYaxnm7yRhGYFq",
          "name": "Bithomp username"
        },
        {
          "address": "rKontEGtDju5MCEJCwtrvTWQQqVAw5juXe",
          "name": "Bithomp validator"
        }
      ]
    },
    {

    }
  ]
}
This endpoint retrieves a list of identified services.

HTTP Request
GET https://bithomp.com/api/v2/services

Response Format
Field	Value	Description
total	Integer	The amount of identified services.
lastUpdate	Integer	UNIX timestamp of the last data update.
services	Array	Array of services.
services[].name	String	A name of a service.
services[].domain	String	A domain of a service.
services[].socialAccounts	Object	An object with social account of a service. (twitter, youtube, instagram, facebook, medium, telegram, linkedin, reddit)
services[].addresses	Array	An array of service's addresses. Each address can have it's own (more specific) name, domain, socialAccounts.
 Before downloading the whole list again you can check if it was updated here: Last update (services)
Addresses from Services
function getData(json) {
  console.log(json)
}
bithompRequest("https://bithomp.com/api/v2/services/addresses", getData);
