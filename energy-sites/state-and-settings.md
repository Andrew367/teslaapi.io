# State And Settings

{% hint style="warning" %}
Work In Progress
{% endhint %}

{% api-method method="get" host="https://owner-api.teslamotors.com" path="/api/1/energy\_sites/:site\_id/status" %}
{% api-method-summary %}
Site Summary - this endpoint seems to no longer function. Returns 404.
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

```javascript
{
    "response": {
        "solar_power": 0,
        "energy_left": 27701,
        "total_pack_energy": 27701,
        "percentage_charged": 100,
        "backup_capable": true,
        "battery_power": 0,
        "load_power": 525,
        "grid_status": "Active",
        "grid_services_active": false,
        "grid_power": 525,
        "grid_services_power": 0,
        "generator_power": 0,
        "storm_mode_active": false,
        "timestamp": "2021-01-27T21:51:56-08:00"
    }
}
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

```javascript
{
    "response": {
        "id": ":id",
        "site_name": ":site_name",
        "backup_reserve_percent": 100,
        "default_real_mode": "self_consumption",
        "installation_date": "2020-08-12T11:40:00-07:00",
        "user_settings": {
            "storm_mode_enabled": true,
            "sync_grid_alert_enabled": true,
            "breaker_alert_enabled": false
        },
        "components": {
            "solar": true,
            "solar_type": "pv_panel",
            "battery": true,
            "grid": true,
            "backup": true,
            "gateway": "teg",
            "load_meter": true,
            "tou_capable": true,
            "storm_mode_capable": true,
            "flex_energy_request_capable": false,
            "car_charging_data_supported": false,
            "off_grid_vehicle_charging_reserve_supported": true,
            "vehicle_charging_performance_view_enabled": false,
            "vehicle_charging_solar_offset_view_enabled": false,
            "battery_solar_offset_view_enabled": true,
            "battery_type": "ac_powerwall",
            "configurable": true,
            "grid_services_enabled": false
        },
        "version": "20.40.3",
        "battery_count": 2,
        "tou_settings": {
            "optimization_strategy": "economics",
            "schedule": [{
                    "target": "off_peak",
                    "week_days": [6, 0],
                    "start_seconds": 68400,
                    "end_seconds": 54000
                }, {
                    "target": "peak",
                    "week_days": [6, 0],
                    "start_seconds": 54000,
                    "end_seconds": 68400
                }, {
                    "target": "off_peak",
                    "week_days": [1, 2, 3, 4, 5],
                    "start_seconds": 82800,
                    "end_seconds": 25200
                }, {
                    "target": "peak",
                    "week_days": [1, 2, 3, 4, 5],
                    "start_seconds": 50400,
                    "end_seconds": 75600
                }
            ]
        },
        "nameplate_power": 10000,
        "nameplate_energy": 27000,
        "installation_time_zone": "America/Los_Angeles",
        "off_grid_vehicle_charging_reserve_percent": 75
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://owner-api.teslamotors.com" path="/api/1/energy\_sites/:site\_id/history?kind=:kind&period=:period" %}
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

{% api-method-query-parameters %}
{% api-method-parameter name=":kind" type="string" required=true %}
Known valid values are energy or power
{% endapi-method-parameter %}

{% api-method-parameter name=":period" type="string" required=false %}
Values are day, month, year or lifetime and is required if kind is energy
{% endapi-method-parameter %}
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

{% api-method method="get" host="https://owner-api.teslamotors.com" path="/api/1/energy\_sites/:site\_id/savings\_forecast" %}
{% api-method-summary %}
Savings Forecast
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

```javascript
{
    "response": null,
    "error": "/api/v3/energy_site/savings_forecast => Tariff not found by tariffID:",
    "error_description": ""
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://owner-api.teslamotors.com" path="/api/1/energy\_sites/:site\_id/tariff\_rates" %}
{% api-method-summary %}
Tariff Rates
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

```javascript
{
    "response": [{
            "tariffID": "CCA-SCE-PRIME",
            "description": "Clean Power Alliance of Southern California - TOU-PRIME",
            "utility": "Clean Power Alliance of Southern California"
        }, {
            "tariffID": "CCA-SCE-TOU-D4",
            "description": "Clean Power Alliance of Southern California - TOU-D-4-9",
            "utility": "Clean Power Alliance of Southern California"
        }, {
            "tariffID": "CCA-SCE-TOU-D5",
            "description": "Clean Power Alliance of Southern California - TOU-D-5-8",
            "utility": "Clean Power Alliance of Southern California"
        }, {
            "tariffID": "CPSF-E-TOU-A",
            "description": "Clean Power SF - E-TOU-A",
            "utility": "Clean Power SF"
        }, {
            "tariffID": "CPSF-E-TOU-B",
            "description": "Clean Power SF - E-TOU-B",
            "utility": "Clean Power SF"
        }, {
            "tariffID": "CPSF-E-TOU-C",
            "description": "Clean Power SF - E-TOU-C",
            "utility": "Clean Power SF"
        }, {
            "tariffID": "CPSF-EV2-A",
            "description": "Clean Power SF - EV2-A",
            "utility": "Clean Power SF"
        }, {
            "tariffID": "MCE-E-TOU-A",
            "description": "Marin Clean Energy (MCE) - E-TOU-A",
            "utility": "Marin Clean Energy"
        }, {
            "tariffID": "MCE-E-TOU-B",
            "description": "Marin Clean Energy (MCE) - E-TOU-B",
            "utility": "Marin Clean Energy"
        }, {
            "tariffID": "MCE-E-TOU-C",
            "description": "Marin Clean Energy (MCE) - E-TOU-C",
            "utility": "Marin Clean Energy"
        }, {
            "tariffID": "MCE-EV2-A",
            "description": "Marin Clean Energy (MCE) - EV2-A",
            "utility": "Marin Clean Energy"
        }, {
            "tariffID": "PCE-E-TOU-A",
            "description": "Peninsula Clean Energy - E-TOU-A",
            "utility": "Peninsula Clean Energy"
        }, {
            "tariffID": "PCE-E-TOU-B",
            "description": "Peninsula Clean Energy - E-TOU-B",
            "utility": "Peninsula Clean Energy"
        }, {
            "tariffID": "PCE-E-TOU-C",
            "description": "Peninsula Clean Energy - E-TOU-C",
            "utility": "Peninsula Clean Energy"
        }, {
            "tariffID": "PCE-EV2-A",
            "description": "Peninsula Clean Energy - EV2-A",
            "utility": "Peninsula Clean Energy"
        }, {
            "tariffID": "PGE-E-TOU-A",
            "description": "Pacific Gas & Electric - E-TOU-A",
            "utility": "Pacific Gas & Electric",
            "isDefault": true
        }, {
            "tariffID": "PGE-E-TOU-B",
            "description": "Pacific Gas & Electric - E-TOU-B",
            "utility": "Pacific Gas & Electric"
        }, {
            "tariffID": "PGE-E-TOU-C",
            "description": "Pacific Gas & Electric - E-TOU-C",
            "utility": "Pacific Gas & Electric"
        }, {
            "tariffID": "PGE-EV2-A",
            "description": "Pacific Gas & Electric - EV2-A",
            "utility": "Pacific Gas & Electric"
        }, {
            "tariffID": "SCE-TOU-D-4_9",
            "description": "Southern California Edison - TOU-D-4-9",
            "utility": "Southern California Edison"
        }, {
            "tariffID": "SCE-TOU-D-5_8",
            "description": "Southern California Edison - TOU-D-5-8",
            "utility": "Southern California Edison"
        }, {
            "tariffID": "SCE-TOU-PRIME",
            "description": "Southern California Edison - TOU-PRIME",
            "utility": "Southern California Edison"
        }, {
            "tariffID": "SCP-E-TOU-A",
            "description": "Sonoma Clean Power - E-TOU-A",
            "utility": "Sonoma Clean Power"
        }, {
            "tariffID": "SCP-E-TOU-B",
            "description": "Sonoma Clean Power - E-TOU-B",
            "utility": "Sonoma Clean Power"
        }, {
            "tariffID": "SCP-E-TOU-C",
            "description": "Sonoma Clean Power - E-TOU-C",
            "utility": "Sonoma Clean Power"
        }, {
            "tariffID": "SCP-EV2-A",
            "description": "Sonoma Clean Power - EV2-A",
            "utility": "Sonoma Clean Power"
        }, {
            "tariffID": "SDGE-DR-SES",
            "description": "San Diego Gas & Electric - DR-SES",
            "utility": "San Diego Gas & Electric"
        }, {
            "tariffID": "SDGE-EV-TOU2",
            "description": "San Diego Gas & Electric - EV-TOU2",
            "utility": "San Diego Gas & Electric"
        }, {
            "tariffID": "SDGE-EV-TOU5",
            "description": "San Diego Gas & Electric - EV-TOU5",
            "utility": "San Diego Gas & Electric"
        }, {
            "tariffID": "SDGE-TOU-DR",
            "description": "San Diego Gas & Electric - TOU-DR",
            "utility": "San Diego Gas & Electric"
        }, {
            "tariffID": "SDGE-TOU-DR1",
            "description": "San Diego Gas & Electric - TOU-DR1",
            "utility": "San Diego Gas & Electric"
        }, {
            "tariffID": "SDGE-TOU-DR2",
            "description": "San Diego Gas & Electric - TOU-DR2",
            "utility": "San Diego Gas & Electric"
        }, {
            "tariffID": "SVCE-E-TOU-A",
            "description": "Silicon Valley Clean Energy - E-TOU-A",
            "utility": "Silicon Valley Clean Energy"
        }, {
            "tariffID": "SVCE-E-TOU-B",
            "description": "Silicon Valley Clean Energy - E-TOU-B",
            "utility": "Silicon Valley Clean Energy"
        }, {
            "tariffID": "SVCE-E-TOU-C",
            "description": "Silicon Valley Clean Energy - E-TOU-C",
            "utility": "Silicon Valley Clean Energy"
        }, {
            "tariffID": "SVCE-EV2-A",
            "description": "Silicon Valley Clean Energy - EV2-A",
            "utility": "Silicon Valley Clean Energy"
        }
    ],
    "count": 36
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

