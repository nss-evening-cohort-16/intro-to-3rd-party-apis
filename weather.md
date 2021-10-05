# Weather API

- Go to [Open Weather](https://openweathermap.org/api) and create an account
- Create an API Key (NOTE: it will take an hour or so to allow the key to process, so during that time, you can review the docs)
- Make sure you save your key in your `.env` file so that it is not available all over the place.
- [Check out the wireframe](https://www.figma.com/file/oqMAbpsQjJfoX5QkbHKTcD/Open-Weather?node-id=0%3A1)
- Get the Sample 5 Day Weather Call in Postman
    - In Postman, select "Import" > "Link"
    - Copy/Paste this link into the input: `https://www.getpostman.com/collections/1b9c951eb7db4a94475f`
    - Click "Import"
- HINT: To get the ICON from the response, use the following: `http://openweathermap.org/img/wn/{INSERT_WEATHER_ICON}@2x.png`

## CHALLENGE
- Allow a user to login to the app using Firebase Auth with Google
- Allow the user to save their locations in Firebase so that when the app loads, all the weather for the locations they submitted give the current weather.

This is a sample response (Take note of the shape of the object):

```json
{
    "cod": "200",
    "message": 0,
    "cnt": 40,
    "list": [
        {
            "dt": 1616468400,
            "main": {
                "temp": 289.05,
                "feels_like": 286.95,
                "temp_min": 286.89,
                "temp_max": 289.05,
                "pressure": 1016,
                "sea_level": 1016,
                "grnd_level": 1000,
                "humidity": 56,
                "temp_kf": 2.16
            },
            "weather": [
                {
                    "id": 802,
                    "main": "Clouds",
                    "description": "scattered clouds",
                    "icon": "03n"
                }
            ],
            "clouds": {
                "all": 49
            },
            "wind": {
                "speed": 2.04,
                "deg": 108
            },
            "visibility": 10000,
            "pop": 0,
            "sys": {
                "pod": "n"
            },
            "dt_txt": "2021-03-23 03:00:00"
        },
        {
            "dt": 1616598000,
            "main": {
                "temp": 289.15,
                "feels_like": 287.61,
                "temp_min": 289.15,
                "temp_max": 289.15,
                "pressure": 1014,
                "sea_level": 1014,
                "grnd_level": 997,
                "humidity": 91,
                "temp_kf": 0
            },
            "weather": [
                {
                    "id": 500,
                    "main": "Rain",
                    "description": "light rain",
                    "icon": "10d"
                }
            ],
            "clouds": {
                "all": 99
            },
            "wind": {
                "speed": 4.27,
                "deg": 187
            },
            "visibility": 10000,
            "pop": 0.21,
            "rain": {
                "3h": 0.14
            },
            "sys": {
                "pod": "d"
            },
            "dt_txt": "2021-03-24 15:00:00"
        }
    ],
    "city": {
        "id": 4644585,
        "name": "Nashville",
        "coord": {
            "lat": 36.1659,
            "lon": -86.7844
        },
        "country": "US",
        "population": 530852,
        "timezone": -18000,
        "sunrise": 1616413644,
        "sunset": 1616457620
    }
}
```


