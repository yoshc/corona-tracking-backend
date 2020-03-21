# corona-tracking-backend
Backend of the Corona Tracking App, developed in the context of the #WirVsVirus Hackathon by the german government. See https://wirvsvirushackathon.org/

# Dependencies
- Python 3.7
- websockets
- psycopg2-binary
- pyjwt

# Setup
- To install all packages, run "pip3 install -r requirements.txt"

# Starting the server
- Enter "python3 server.py" in the terminal

# REST API Documentation
- Content-Type must be application/json
- Use Unix Timestamps
- All responses are in the following format:
```
{
    "success": True,
    "messages": "Contains message if something went wrong"
    "payload": {
        // request payload here
    }
}
```
## Test
```
GET /test
```
Just for testing

## Register User
```
POST /register
```

## Upload tracking data
```
POST /track
```

**Request body:**
```
{
  [
    {
        timestamp: 123456
        contactId0: 123456
        contactId1: 123456
    }
    ...
  ]
}
```