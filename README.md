
# WSD_ RestAPI_Technical_project

This is a RestApi that returns Betting data about horse racing events, Using the betfair api.



### Prerequisites
This README.md provides a step-by-step guide on how to download, install, and set up the WSD Technical task project from Github.

In order to test this application, the user must have their own X-Application (app key) and X-Authentication (session Token). To obtain these, follow these steps:

1). Create a Betfair account by following this [link](https://register.betfair.com/account/registration).

2). Create an Application Key by following the instructions found [here](https://docs.developer.betfair.com/display/1smk3cen4v3lu3yomq5qye0ni/Application+Keys).

3). Obtain a session key by following the instructions found [here](https://developer.betfair.com/exchange-api/accounts-api-demo/). Note that session tokens need to be updated every 12 hours as they expire.

Once you have obtained your X-Application (app key) and X-Authentication (session Token), you can proceed to download or clone the WSD Technical task project from Github.

### Installation

Follow these instructions to install the WSD Technical task project:


1). Change into the project directory by running the following command: cd WSD Techical task

2). Install the dependencies by running the following command: npm install

3). Start the project by running the following command: npm run dev. This command starts the project with the help of the nodedemon script, which automatically restarts the project whenever changes are made.

### API Setup

The API setup involves adding your X-Application (app key) and X-Authentication (session Token) to the api client file. To do this, follow these steps:

1). Open the api client file in your chosen editor.

2). Add your X-Application (app key) to the appKey field in the header of the api client file.

3). Add your X-Authentication (session Token) to the sessionToken field in the header of the api client file.


![apiclient File](https://github.com/JosephBatchelor/WSD_Technical_Test/blob/main/RDME_Images/apiclient.png)

Note: Remember to update your sessionToken every 12 hours, as it expires.



### Postgres Setup

he database connector is located in the model/HorseDetails.js file. To set up the database, follow these steps:

1). Open the model/HorseDetails.js file in your chosen editor.

2). Add the corresponding details from your database setup to the appropriate fields in the model/HorseDetails.js file.

![HorseDetails File](https://github.com/JosephBatchelor/WSD_Technical_Test/blob/main/RDME_Images/db%20setup.png)

That's it! You have successfully installed and set up the WSD Technical task project.

If you have any problems during the installation and setup process, please don't hesitate to reach out to me for assistance.
## API Reference


### Get all events types

```http
  GET /event-types
```
This will provide a list of event-types (i.e. football, tennis horse racing).

![event-types](https://github.com/JosephBatchelor/WSD_Technical_Test/blob/main/RDME_Images/event-types.png)



### Get all events with id

```http
  GET /events/:id
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `integer` | **Required**. Id of the event to fetch |

This will provide the details of spsefic events based its id. The id can be obtained from "/event-types".

![events](https://github.com/JosephBatchelor/WSD_Technical_Test/blob/main/RDME_Images/events.png)

### Get all market-book data

```http
  GET /market-book
```
This will provde all market book details for all events.

![Market-book](https://github.com/JosephBatchelor/WSD_Technical_Test/blob/main/RDME_Images/market-book.png)




### Get all market-book data for spesific event

```http
  GET /market-book/:eventid
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `eventid`      | `integer` | **Required**. Id of the event to fetch market data for |

This will provde all market book details for spesific events.

![Market-book/eventid](https://github.com/JosephBatchelor/WSD_Technical_Test/blob/main/RDME_Images/market-book_event.png)



### Get all market-book data for Runner in a spesific event

```http
  GET /market-book/:eventid/:selectionId
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `eventid`      | `integer` | **Required**. Id of the event  |
| `selectionId`      | `integer` | **Required**. Id of the runner   |


This will provde all market book details for spesific runners in spesific events.() 

![Market-book/eventid/runnerid](https://github.com/JosephBatchelor/WSD_Technical_Test/blob/main/RDME_Images/market-book_event_runner.png)
