# Environmental Awareness Dashboard

## How to Setup ?
- Step 1: Clone Server Code from https://github.com/Arka90/Environmental-Awareness-Dashboard-server.git
- Step 2: Clone Client Code from https://github.com/Arka90/Environmental-Awareness-Dashboard-Client.git
- Step 3: Open Server Code folder in any terminal and run ``` npm install ``` this will install the dependencies.

Note: Currently for simplicity I am not ignoring the **.env** file in case if you don't have the file create a **.env** file on root level and paste the following content

```
PORT=9000

MONGO_URL=mongodb+srv://arkas:gxmZ5o5Z3sdRyDAs@graphql-todo.uqv1bgd.mongodb.net/environmental_awareness_dashboard

OPEN_WEATHER_API_KEY=ffd2f88a623ef8dcc5b13c926ed82099
```

- Step 4: Now to run the server run this command ``` npm run start ```. If every thing went well you will see these message in console "Server is running on port 9000
DB Successfully Connected 🟢"  
- Step 5: Now to Start the client go into the client folder and run this command ```npm install``` this will again download all the dependencies for the client
- Step 6: To start the client code run this command ```npm run dev```. You will get a local hosted link for the app click that to open on the browser

## Schema Definition

Here we are using only one schema to store weather data

### Model name Weather
```
name: {
type:  String,
required: [true, "A weather must belongs to some Place"],
},
date: [],
temperature: [],
pressure: [],
humidity: [],
```

## API endpoints

### For getting live data | Method : GET
```
http://localhost:9000/weather/getLiveData/latitude/longitude
```

### For getting history data | Method : GET
```
http://localhost:9000/weather/getHistory/latitude/longitude
```

### For getting all weather | Method : GET
```
http://localhost:9000/weather/getAllWeather
```

### For getting a weather by Name | Method: GET
```
http://localhost:9000/weather/getWeatherByName?city=cityName
```

**NOTE :  The port number might be different in your case if you have changed it in .env file**
