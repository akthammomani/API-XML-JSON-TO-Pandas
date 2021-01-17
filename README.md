# APIs (Application Programming Interfaces):

An API is a set of protocols and routines for building and interacting with software applications. 
Another way to think of it is that an API is a bunch of code that allows two software programs to communicate with each other. 
For example:
 * If we wanted to stream twitter data by writing some Python code, we would use the Twitter API.
 * If we wanted to automate pulling and processing information
 
 ## Getting Started With Python Requests:
 
In many web apps, it’s normal to connect to various third-party services by using APIs. When we use these APIs we can get access to data like weather information, sports scores, movie listings, tweets, search engine results, and pictures. we can also use APIs to add functionality to your app. Examples of these are payments, scheduling, emails, translations, maps, and file transfers. If we were to create any of those on your own it would take a ton of time, but with APIs, it can take only minutes to connect to one and access its features and data.

**Python Requests library:** which allows you to send HTTP requests in Python.
And since using an API is simply sending HTTP requests and receiving responses, Requests allows you to use APIs in Python.

## Install Python Requests
Before we can do anything, we need to install the library. So let’s go ahead and install requests using pip: 

  * pip install requests

## Our First Request
  * import requests
  * response = requests.get('url')
  * print(response)

So all this code is doing is sending a GET request to url (API). This is the same type of request our browser sent to view this page, but the only difference is that Requests can’t actually render the HTML, so instead we will just get the raw HTML and the other response information.

## Status Codes
The first thing we can do is check the status code. HTTP codes range from the 1XX to 5XX. Common status codes that you have probably seen are 200, 404, and 500.
Here’s a quick overview of what each status code means:
  * 1XX - Information
  * 2XX - Success
  * 3XX - Redirect
  * 4XX - Client Error (you messed up)
  * 5XX - Server Error (they messed up)
Generally, what you’re looking for when you perform your own requests are status codes in the 200s.
Requests recognizes that 4XX and 5XX status codes are errors, so if those status codes get returned, the response object from the request evaluates to False.

## Headers
Another thing we can get from the response are the headers. We can take a look at them by using the headers dictionary on the response object.

  * response.headers
  
## Response Text
And finally, if we take a look at response.text (this works for textual data, like a HTML page like we are viewing) we can see all the HTML needed to build the home page of a specific website. It won’t be rendered, but we see that it looks like it belongs to a specific website. If we saved this to a file and opened it, you would see something that resembled the a specific website. In a real situation, multiple requests are made for a single web page to load things like images, scripts and stylesheets, so if we save only the HTML to a file, it won’t look anything like what the a specific website page looks like in your browser because only a single request was performed to get the HTML data.
  
  * response.text 
  
  

 

