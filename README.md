# technology-radar

Describing all of Checkatrade technology in one place, based on the work from ThoughtWorks. To understand how to use 
this repository, please read the [original article](https://www.thoughtworks.com/radar/how-to).

## Releases

All new technology that is added to the radar should have passed the Architecture Review Board (ARB) and be in the state 
of being used in production. The radar is updated every 6 months, or at the occurrence of major technology shifts in the
engineering department. New versions should be generating a new radar URL and update the DNS CNAME record to point to the
new version.  
[BYOR](https://radar.thoughtworks.com/)

## JSON structure

You need to follow this JSON structure to ensure the radar is generated correctly.  

```json
  {
    "name": "Name of the technology",
    "ring": "adopt/hold/assess/trial",
    "quadrant": "platforms/tools/languages & frameworks/techniques",
    "isNew": "TRUE/FALSE",
    "description": "Short description of the technology"
  }
```

## Running locally

To run the radar locally you will have to run the following commands:

```bash
make build
make run
```

Then when you open your browser at `http://localhost:8080` and paste in the json file you wish to test out. The files should
be located at http://localhost:8080/files/version/version.json or http://localhost:8080/files/latest.json.