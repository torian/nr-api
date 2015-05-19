# Maintenance script for New Relic

## Requirements

  * python
  * python lib newrelic_api
  * python lib docopt

## Install

Once you've cloned the repo:

```
  $> sudo pip install -r requirements.txt
```

## Usage:

List servers and their metadata, in json format:
```
  $> nr-api server list --api-key <api_key> --json

```

Search servers that match a criteria
```
  $> nr-api server search --name ip-10-10 --api-key <api_key> 

```

Clean servers that are no longer reporting:
```
  $> nr-api server clean --api-key <api_key> 

```

Add servers to a given alert policy:
```
  $> nr-api server policy \
     --policy-name 'Production Server Policy' \
     --name ip-10-10
     --api-key <api_key> 

```

Keep in mind that the `--name` is a pattern, so using `ip-10-10` could
match `ip-10-10-123-1`, `ip-10-10-9-45`, etc.

## TODOs

  * Lots of this

