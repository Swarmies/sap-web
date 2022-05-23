# Calendar View

## What is an API End points

An API endpoint is a point at which an API (the code that allows two software programs to communicate with each other) connects with the software program. APIs work by sending *requests* 
for information from a web application or web server and receiving a *response*.

### **How API endpoints work**

One side sends the information to the API and is called the [server](https://www.techtarget.com/searchnetworking/definition/client-server). The other side, the client, makes the requests and manipulates the API. The server side that provides the requested information, or resources, is the API endpoint.  

![Screen Shot 2022-05-09 at 4.18.32 PM.png](https://user-images.githubusercontent.com/32272045/169191178-d3ab7f24-f66b-4b76-bab9-7023e46b0fd2.png)

In our case the client is going to be **Student, Mentor and Admin** as seen in the class diagram.

### API connection:

After creating the API locally, it will be hosted on an api hosting platform. Swagger is not only good for documenting the API but also has features for running and testing the API. The API should be able to respond to requests as seen below. 

When making GET request to the link, the API responds with the following JSON data

- GET:    https://sapapi.com/calendar

```cpp
// Response
{         name:"Dinaol Tadesse",
					courses:{"csc 118","calculus"},
					calendar: { { {"Tuesday","Thursday"},
												startTime:"00:12:00",
												endTime:"00:13:00"},
											{ {"Monday","Wednesday"},
												startTime:"00:07:00",
												endTime:"00:09:00"}
}
```

- POST: https://sapapi.com/user/addmentor

When making a post request to the API for adding a mentor, the API has to authenticate and respond with the following JSON. The API can either use a token or username and password for authentication.

```cpp
{authorization: {username,password}
	{
		Body: {name:"Dinaol Tadesse",
					courses:{"csc 118","calculus"},
					calendar: { { {"Tuesday","Thursday"},
												startTime:"00:12:00",
												endTime:"00:13:00"},
											{ {"Monday","Wednesday"},
												startTime:"00:07:00",
												endTime:"00:09:00"}
	

}
```

### Calendar UI

For displaying the calendar on our application, there are different react calendar libraries. We can use the [React Big Calendar library](https://github.com/jquense/react-big-calendar). A small demo of how the calendar looks like can be found [here](https://jquense.github.io/react-big-calendar/examples/index.html?path=/story/about-big-calendar--page).

![Screen Shot 2022-05-18 at 9.21.24 PM.png](https://user-images.githubusercontent.com/32272045/169191267-b8572369-bd86-4794-ae0f-6da53c1bf57c.png)

### Resources:

**OpenAPI** - standard way to describe an API

**Swagger API -** [https://swagger.io/specification/](https://swagger.io/specification/)

**Amazon API gateway**

**Requestbin**: [https://pipedream.com/workflows](https://pipedream.com/workflows)

**Tech Target:** [https://www.techtarget.com/searchapparchitecture/definition/API-endpoint#:~:text=An API endpoint is a,server and receiving a response](https://www.techtarget.com/searchapparchitecture/definition/API-endpoint#:~:text=An%20API%20endpoint%20is%20a,server%20and%20receiving%20a%20response).

**API Creation:** [https://blog.stoplight.io/how-to-create-an-api-in-three-steps](https://blog.stoplight.io/how-to-create-an-api-in-three-steps)