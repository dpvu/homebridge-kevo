
# Kevo Plugin

You MUST have a Kevo Plus for this plugin to work!

Example config.json:

    {
      "accessories": [
        {
            "accessory": "Kevo",
            "name": "Front Door",
            "username": "test@example.com",
            "password": "<your kevo password>",
            "lock_id": "<your lock id>",
            "serialNumber": "<RANDOM STRING HERE>"
        },
        {
            "accessory": "Kevo",
            "name": "Back Door",
            "username": "test@example.com",
            "password": "<your kevo password>",
            "lock_id": "<your lock id>",
            "serialNumber": "<RANDOM STRING HERE>"
        },
      ]
    }

Kevo now provides the lock IDs from the web portal or app within the lock detail information. If using multiple locks it is recommended to use different My Kevo accounts for both. This can easily done with Gmail by adding a "+something" to the email to create a second account that will go to the same email (e.g. myemail@gmail.com for the first account and myemail+kevo@gmail.com for the second). 

Use a random serial number for each lock so that when importing to Home Assistant all locks come across instead of just one. 

NOTE: When commanding groups of locks, there will be a 15 second delay between each lock command firing because Kevo does not support rapid API requests. This causes Siri to usually say "Sorry x, I didn't hear back" as a result.
