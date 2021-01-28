# State And Settings

{% hint style="warning" %}
Work In Progress
{% endhint %}

{% api-method method="get" host="https://owner-api.teslamotors.com" path="/api/1/energy\_sites/:site\_id/status" %}
{% api-method-summary %}
Site Summary
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name=":site\_id" type="integer" required=true %}
The `{site_id}` from the products list
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer `{access_token}` from authentication
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://owner-api.teslamotors.com" path="/api/1/energy\_sites/:site\_id/live\_status" %}
{% api-method-summary %}
Site Data
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name=":site\_id" type="integer" required=true %}
The `{site_id}` from the products list
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer `{access_token}` from authentication
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://owner-api.teslamotors.com" path="/api/1/energy\_sites/:site\_id/site\_info" %}
{% api-method-summary %}
Site Configuration
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name=":site\_id" type="integer" required=true %}
The `{site_id}` from the products list
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer `{access_token}` from authentication
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://owner-api.teslamotors.com" path="/api/1/energy\_sites/:site\_id/history" %}
{% api-method-summary %}
Historical Data
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name=":site\_id" type="integer" required=true %}
The `{site_id}` from the products list
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer `{access_token}` from authentication
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://owner-api.teslamotors.com" path="/api/1/energy\_sites/:site\_id/calendar\_history?kind=:kind&period=:period&end_date=:end\_date" %}
{% api-method-summary %}
Calendar History Data
{% endapi-method-summary %}

{% api-method-description %}
Returns energy data for the specified period interval
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name=":site\_id" type="integer" required=true %}
The `{site_id}` from the products list
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer `{access_token}` from authentication
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name=":kind" type="string" required=true %}
Known valid values are energy or power
{% endapi-method-parameter %}

{% api-method-parameter name=":period" type="string" required=false %}
Values are day, month, year or lifetime and is required if kind is energy
{% endapi-method-parameter %}

{% api-method-parameter name=":end\_date" type="datetime" required=false %}
ISO 8601 formatted date time and timezone offset. Data is returned up to the supplied time, starting at the beginning of the period supplied
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "response": {
        "serial_number": ":serial_number",
        "period": "day",
        "installation_time_zone": "America/Los_Angeles",
        "time_series": [{
                "timestamp": "2021-01-27T01:00:00-08:00",
                "solar_energy_exported": 10325.15796698496,
                "generator_energy_exported": 0,
                "grid_energy_imported": 23967.007174718194,
                "grid_services_energy_imported": 0,
                "grid_services_energy_exported": 0,
                "grid_energy_exported_from_solar": 3538.661274429731,
                "grid_energy_exported_from_generator": 0,
                "grid_energy_exported_from_battery": 0,
                "battery_energy_exported": 0,
                "battery_energy_imported_from_grid": 14.601269266597228,
                "battery_energy_imported_from_solar": 775.3987307334028,
                "battery_energy_imported_from_generator": 0,
                "consumer_energy_imported_from_grid": 23952.405905451596,
                "consumer_energy_imported_from_solar": 6011.097961821826,
                "consumer_energy_imported_from_battery": 0,
                "consumer_energy_imported_from_generator": 0
            }
        ]
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

