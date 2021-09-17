<h1>Checkpoint Export</h1>
<h2>What this is</h2>
This is a collection of scripts and postman collections for:

- querrying a checkpoint fw management server for information (objects, rules, etc)
- manipulating checkpoint data exported via any means possible (e.g. csv exports via dashboard or other means)

<h2>The readrules script</h2>
The actions->export part of the dashboard can produce a csv file that you can download in your PC from the Smart Dashboard console. That csv file is ugly and doesn't translate well with the text-to-columns tool in excel. Also we always spend more time formating columns and alligmnent every time we get the data to look like we want them to. 
This script does all those in seconds provided you run it with the csv filename as an argument.
Have fun with your exports!

Install openpyxl before you run the script. You should probably use a dedicated virtual environment for it.
Install with pip install openpyxl

<h2>Postman Collections</h2>
I can't remember if I have found an original version of those anywhere or I built them myself. If you find part of them anywhere please let me know so I can give proper credit.
I am pretty certain I have built this myself sometime during the COVID-19 period.

The Checkpoint Community site has a big list of collections and the v.1.5 API collection is a lot bigger and different from this one, so this doesn't come from there.
I was requested to share this so I am posting fast.
You can always look up more in the following links:
- https://community.checkpoint.com/t5/API-CLI-Discussion/Postman-Collections-links-to-all-available-and-the-basics/m-p/40923
- https://community.checkpoint.com/t5/API-CLI-Discussion/postman-collection-R80-30/m-p/53935#M3495
- https://rawcode7.medium.com/how-to-use-check-point-api-with-postman-8dd34bf7e2a

You can find information on the Checkpoint Mgmt API here (v.1.5):
https://sc1.checkpoint.com/documents/latest/APIs/index.html#web/show-services-tcp~v1.5%20

Let me know if you find more.

To make this work, you need to import the collection and the environment and modify the environment values. Then you run the get in request to get back your sid. Select the sid in the response, right-click with your mouse over it and select the set-to option to set it to the X-chkp-sid variable. Then you can perform the rest of the requests at will. Pay attention that the variables are sometimes set inside quotes. That means that the expected value from the API is a string. If the quotes are already there, you don't need to put them in the environment variable values. Play a bit with that and you will get the hang of it.

<h2>API querrying</h2>
I will work eventually on querrying the Checkpoint Mgmt API with Python (check above for https link) and publish what I can here, once I get it sanitized from sensitive information.

Feel free to look me up on twitter under @mythryll if you have questions related to this or automation/programmability in general.
