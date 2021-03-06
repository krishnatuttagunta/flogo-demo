



# Directory Poller
This triggers provides your flogo application the ability to poll a directory continuosly and notify whenever anything changes inside that directory.


## Installation

```bash
flogo add activity github.com/anshu2185/flogo-demo/dirpoll
```

## Schema
Inputs and Outputs:

```json
{
  "settings":[
    {
      "name": "dirName",
      "type": "string",
      "value": "default"
    }
  ],
  "outputs": [
    {
      "name": "filename",
      "type": "string"
    }
  ],
  "handler": {
    "settings": [
      {
        "name": "dirName",
        "type": "string"
      }
    ]
}
```
## Settings
| Setting     | Description    |
|:------------|:---------------|
| dirName   | Full file path of the directory to be polled |         

## Configuration


### Flow Configuration
Configure a task in flow to perform Fast Fourier Transform

```json
{
  "triggers": [
    {
      "name": "Directory Poller",
      "ref": "github.com/anshu2185/flogo-demo/dirpoll",
      "description": "Simple Directory Poller",
      "settings": {
        "dirName": "/Users/anshu/Downloads/files"
      },
      "id": "directory_poller",
      "handlers": [
        {
          "settings": {
            "dirName": "/Users/anshu/Downloads/files"
          },
        }
      ]
    }
  ]
}
```
