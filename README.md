Hangouts.json Parser
===

## Introduction
I tried using every `Hangouts.json` parser I could find but they were all browser based and crashed when I tried parsing my 500MB+ payload. This CLI based parser doesnt.

## Usage
```
./parse path/to/Hangouts.json
```

## Behavior
This tool will export a simplified JSON file for each conversation under the `exports/` directory. It will be named after the internal conversation ID which is pretty useless but at least unique.

The content of the file will be as follows:
```
{
  "users": [
    "John Smith",
    "Jane Smith"
    ...
  ],
  "conversation": [
    {
      "timestamp": 946684800000,
      "friendly_timestamp": "1999-12-31 19:00:00 -0500",
      "user": "John Smith",
      "content": "Wow the Hangouts export sure is bloated!"
    },
    ...
  ]
}
```
