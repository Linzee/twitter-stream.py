# twitter-stream.py
[![v2](https://img.shields.io/endpoint?url=https%3A%2F%2Ftwbadges.glitch.me%2Fbadges%2Fv2)](https://developer.twitter.com/en/docs/twitter-api)

# Sampled Stream
![](assets/SampledStream.png)

# Filtered Stream

![](assets/quickstart.png)

### Bearer Token
```
~$ export BEARER_TOKEN=BEARER TOKEN
```
### Adding Rules
```python
>>> import json
>>> from twitter_stream import FilteredStream

>>> stream = FilteredStream()
>>> rules = {"add": [{'value': 'from: twitivitydev'}]}
>>> print(json.dumps(stream.add_rule(data=rules), indent=4))
```

### Deleting Rules
```python
>>> import json
>>> from twitter_stream import FilteredStream

>>> stream = FilteredStream()
>>> response = stream.delete_rule({"delete": {"ids": ['1331486534579589120']}})
>>> print(response)
```

### Get Rules
```python
>>> import json
>>> from twitter_stream import FilteredStream

>>> stream = FilteredStream()
>>> print(json.dumps(stream.get_rules(), indent=4, sort_keys=True))
```

### Stream
```python
>>> import json
>>> from twitter_stream import FilteredStream

>>> stream = FilteredStream()
>>> for tweet in stream.connect():
       print(json.dumps(tweet, indent=4))
```

## Installation
```bash
~$ pip3 install twitter-stream.py
```

# Documentation
Read the documentation at [twitivity.dev/docs](https://twitivity.dev/docs/twitter-stream.py/)
