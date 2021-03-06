# PI Web Control
**Raspberry PI web lighting control with React and NodeJS**


This project was created to allow web based control of IOT hubs such as the HUE.  
Initial support for HUE with a plan for other hubs in future.  
The server was intended to run on Raspberry PI to allow access to PI peripherals as
well as local control via sensors and schedules. 

## Getting Started

These instructions will get the project up and running on your Raspberry PI for
testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

Nodejs


### Installing

Install NodeJS on your PI

```
curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -
sudo apt install -y nodejs

```
Test node installation

```
node --version
```
Install the app

```
git clone https://github.com/gwyncm/PIWebControl.git
```
Move to project directory

```
cd PIWebControl
```

Install libraries

```
npm install
```
Build the app

```
npm run build
```

Obtain a username/key here 

[HUE getting started](https://developers.meethue.com/develop/get-started-2/)

Create a file with the following format called config.hue in the project directory.

```
{ "user" : "<your username>", "host" : "<bridge ip address>" }
```

Run the app with logging

```
node piserv.js --log
```

Connect

### browse to your PI app ###

```
http://<your pi address>/piweb
```

Enjoy!


## Running the tests

npm test

### You can also access the server via http

```
http://<your pi address>:8075/api/lights

<json result>

```

## Deployment

npm build

## Built With

[Create React App](https://github.com/facebook/create-react-app)  - The web framework used - See READMECRA.md

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* [Huejay] (https://github.com/sqmk/huejay) - Excellent HUE control library


