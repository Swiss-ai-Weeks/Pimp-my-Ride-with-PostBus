# Data for the Challenge "Pimp my Ride with PostBus"
This respository is part of the Zurich hackathon of [Swiss {ai} Week](https://swiss-ai-weeks.ch/) happening on 26/27 September 2025.

By accessing or using the data provided, you agree to the following terms and conditions.

## Terms and Conditions
> The data is provided solely for the purpose of participating in the hackathon event held in Zurich, Switzerland, and for developing solutions directly related to the specific challenge you have selected. You are strictly prohibited from using the Data for any other purpose, including but not limited to:
> - Commercial use.
> - Research or development outside the scope of this hackathon challenge.
> - Personal use or any other unauthorized activities.
> 
> The data is provided "as is" without any warranties, express or implied, including but not limited to, warranties of merchantability, fitness for a particular purpose, or non-infringement. The hackathon organizers do not guarantee the accuracy, completeness, or reliability of the data.
>
> Immediately following the conclusion of the hackathon event, you are obligated to permanently and securely delete all copies of the data, including any derived or processed data, from all your devices, storage media, and systems. 

## Source of Data
The data of this respository has been provided by [Swiss Post](https://www.post.ch/) submitting the challenge.

## Documentation
For all the postauto trips a hash of their route is calculated to group the data into folders. In the folder for a trip hash the individual trips are grouped into folders by date. All these trips took the exact same planned timetable route, just at different times.

The individual trip files are CSV files with the following columns:
- `time`: The timestamp of the GPS point in ISO 8601 format (e.g., `2023-09-01T12:34:56Z`).
- `latitude`: The latitude of the GPS point in decimal degrees.
- `longitude`: The longitude of the GPS point in decimal degrees.
- `velocity`: The velocity of the vehicle at the GPS point in meters per second (m/s).

In one file all the recorded positions of a single trip are stored. The files are named with a trip-id (excluding the file ending .csv) that can be resolved with the [Viadi Routing Services](https://www.viadi-mobility-services.ch/routing-service.html). For the hackathon you can use the INT API of the Viadi Routing Services. The corresponding API key and documentation is provided upon request.