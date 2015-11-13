# user: findMeetingTimes


### Prerequisites
The following **scopes** are required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http


```
### Request headers
| Name       | Type | Description|
|:---------------|:--------|:----------|
| X-Sample-Header  | string  | Sample HTTP header. Update accordingly or remove if not needed|

### Request body
In the request body, provide a JSON object with the following parameters.

| Parameter	   | Type	|Description|
|:---------------|:--------|:----------|
|attendees|attendeeBase||
|locationConstraint|locationConstraint||
|timeConstraint|timeConstraint||
|meetingDuration|duration||
|maxCandidates|int32||
|isOrganizerOptional|boolean||

### Response
If successful, this method returns `200, OK` response code and [meetingTimeCandidate](../resources/meetingtimecandidate.md) object in the response body.

### Example
Here is an example of how to call this API.
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "user_findmeetingtimes"
}-->
```http

Content-type: application/json
Content-length: 1166

{
  "attendees": [
    {
      "type": {
      }
    }
  ],
  "locationConstraint": {
    "isRequired": true,
    "suggestLocation": true,
    "locations": [
      {
        "displayName": "displayName-value",
        "locationEmailAddress": "locationEmailAddress-value",
        "address": {
          "street": "street-value",
          "city": "city-value",
          "state": "state-value",
          "countryOrRegion": "countryOrRegion-value",
          "postalCode": "postalCode-value"
        },
        "coordinates": {
          "altitude": 99,
          "latitude": 99,
          "longitude": 99,
          "accuracy": 99,
          "altitudeAccuracy": 99
        }
      }
    ]
  },
  "timeConstraint": {
    "activityDomain": {
    },
    "timeslots": [
      {
        "start": {
          "date": "datetime-value",
          "time": "datetime-value",
          "timeZone": "timeZone-value"
        },
        "end": {
          "date": "datetime-value",
          "time": "datetime-value",
          "timeZone": "timeZone-value"
        }
      }
    ]
  },
  "meetingDuration": "datetime-value",
  "maxCandidates": 99,
  "isOrganizerOptional": true
}
```

##### Response
Here is an example of the response. Note: The response object may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.meetingtimecandidate"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 984

{
  "meetingTimeSlot": {
    "start": {
      "date": "datetime-value",
      "time": "datetime-value",
      "timeZone": "timeZone-value"
    },
    "end": {
      "date": "datetime-value",
      "time": "datetime-value",
      "timeZone": "timeZone-value"
    }
  },
  "confidence": 99,
  "score": 99,
  "organizerAvailability": {
  },
  "attendeeAvailability": [
    {
      "attendee": {
        "type": {
        }
      },
      "availability": {
      }
    }
  ],
  "locations": [
    {
      "displayName": "displayName-value",
      "locationEmailAddress": "locationEmailAddress-value",
      "address": {
        "street": "street-value",
        "city": "city-value",
        "state": "state-value",
        "countryOrRegion": "countryOrRegion-value",
        "postalCode": "postalCode-value"
      },
      "coordinates": {
        "altitude": 99,
        "latitude": 99,
        "longitude": 99,
        "accuracy": 99,
        "altitudeAccuracy": 99
      }
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: findMeetingTimes",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->