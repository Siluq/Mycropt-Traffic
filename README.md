
# Traffic Skill for Mycroft

This is a skill to query travel times to points of interest (POIs) for
[Mycroft](https://mycroft.ai). 

## Installation

Clone the repository into your `~/.mycroft/skills` directory. Then install the
dependencies inside your mycroft virtual environment:

```
cd ~/.mycroft/skills
git clone https://github.com/siluq TrafficSkill
```

## Configuration

Add a block to your `~/.mycroft/mycroft.conf` file like this:

```
"TrafficSkill": {
  "api_key": "REPLACETHISWITHKEYFROMGOOGLE",
  "pois": {
    "default": {
      "destinations": {
        "work": "Dorpsstraat 25, 3941 JK Doorn"
      },
      "origins": {
        "home": "Notengaard 18, 3941 LW Doorn"
      }
    }
  }
}
```
* Google API key can be obtained [HERE](https://developers.google.com/maps/documentation/directions/start#get-a-key)

## Usage

"Hey Mycroft, how long is my trip to work?". 
This will return your travel time, and if there is any traffic how much there is.


## Supported Phrases/Entities
Currently the phrases are:
* Hey Mycroft, how long is my trip to X? (Where X is a configured POI)



## TODO
* Include required start or arrival time
* Include alternatives for navigation other than Google Maps API
 > [MapQuest](https://developer.mapquest.com/documentation/directions-api/)
 
 > [Bing Maps](https://msdn.microsoft.com/en-us/library/ff701718.aspx)

## In Development
* Be able to query for non-configured locations. (i.e. "How close is the nearest bank?")


## Contributing

All contributions welcome:

* Fork
* Write code
* Submit pull request

