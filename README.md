
# **CoolMapRoutePath**

A Python utility for calculating route paths, estimated travel times, and distances using Mapbox API.


## **Installation**

Install the package using pip:

```bash
pip install coolmaproutepath
```


## **What is it?**

`CoolMapRoutePath` is a utility module that supports:
- Generating route paths (coordinates) between two locations.
- Calculating estimated travel distances.
- Calculating estimated travel times.

The calculations are based on the latitude and longitude of the pick-up and delivery locations, powered by the Mapbox API.


## **Usage/Examples**

### **Basic Usage**
To use `CoolMapRoutePath`, instantiate the class with the following parameters:
- **`from_lat_log`**: The starting latitude and longitude.
- **`to_lat_log`**: The destination latitude and longitude.
- **`map_box_api_key`**: Your Mapbox API key.

```python
from coolmaproutepath import CoolmapRoutePath

# Example initialization
cool_obj = CoolmapRoutePath("38.24265,-76.56296", "39.2262,-76.81595", "<your_map_box_api_key>")
```


### **Methods**

#### **1. Get Estimated Time**

Retrieve the estimated travel time between locations in various units:
- **`s`**: Seconds
- **`m`**: Minutes
- **`h`**: Hours

```python
# Example: Get estimated time in seconds
time_in_seconds = cool_obj.estimated_time(required_unit='s')
print(time_in_seconds)  # Output: '6656.05 Seconds'
```


#### **2. Get Estimated Distance**

Retrieve the estimated travel distance between locations in various units:
- **`m`**: Miles
- **`k`**: Kilometers
- **`n`**: Nautical Miles
- **`t`**: Meters

```python
# Example: Get estimated distance in meters
distance_in_meters = cool_obj.estimated_distance(required_unit='t')
print(distance_in_meters)  # Output: '144062.0 Meters'
```


#### **3. Get Route Path**

Retrieve the route path as a series of coordinates.

```python
# Example: Get the route path
route_path = cool_obj.get_path()
print(route_path)  # Output: '38.242287,-76.56314400000001;38.242289,-76.563149;...'
```


## **Features**
- **Simple API** for route, distance, and time estimation.
- **Customizable Units** for time and distance.
- Powered by **Mapbox API** for accurate route information.


## **Requirements**
- Python 3.6+
- Mapbox API Key (sign up at [Mapbox](https://www.mapbox.com/))


## **Installation Dependencies**
Make sure to install the required dependencies listed in the `requirements.txt` file. These are automatically installed with the package.


## **Contributing**
We welcome contributions! Feel free to fork the repository and submit a pull request for additional features or improvements.


## **License**
This project is licensed under the MIT License. See the `LICENSE` file for details.
