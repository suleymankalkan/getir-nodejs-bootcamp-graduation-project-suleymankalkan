# Getir NodeJS Bootcamp Graduation Project
Getir&Patika.dev NodeJS Bootcamp Graduation Project

Demo link: https://getir-graduation-project.herokuapp.com/

## Installation

Install my-project with npm

After cloning the project, go to project folder and execute the commands below for install.
```bash
  npm install
  cp env-example .env
```
Make sure to fill your .env file. 

### Start
After everything is installed and configured, we can simply start out project with:
```bash
  npm run dev
```

### Tests
To run integration tests, simply execute:
```bash
  npm test
```
## API Reference

#### List the filtered records

```http
  POST /records
```
Request body should be in json format and should contain the fiels below as described.
| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `startDate` | `string` | Should be in ISO Date format |
| `endDate` | `string` | Should be in ISO Date format |
| `minCount` | `number` | min value for totalCount |
| `maxCount` | `number` | max value for totalCount |

#### Example request

```http
  POST /records
```

| Payload | 
| :-------- | 

```javascript
{
    "startDate": "2016-01-23",
    "endDate": "2017-01-26",
    "minCount": 1000,
    "maxCount": 5000
}
```
| Response | 
| :-------- | 

```javascript
{
    "code": 0,
    "msg": "Success",
    "records": [
        {
            "key": "PVLFLSNw",
            "createdAt": "2016-12-30T04:51:57.295Z",
            "totalCount": 4184
        },
        {
            "key": "QLBWiXWS",
            "createdAt": "2016-12-30T04:37:04.145Z",
            "totalCount": 3976
        },
        ...
    ]
}
```



## Environment Variables

To run this project, you will need to add the following environment variables to your .env file

`SERV_PORT` : The port that http server will use to serve.

`DB_URL`: MongoDB connection string

