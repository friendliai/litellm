# FriendliAI
https://suite.friendli.ai/

**We support ALL FriendliAI models, just set `friendliai/` as a prefix when sending completion requests**

## API Key
```python
# env variable
os.environ['FRIENDLI_TOKEN']
```

## Sample Usage
```python
from litellm import completion
import os

os.environ['FRIENDLI_TOKEN'] = ""
response = completion(
    model="friendliai/mixtral-8x7b-instruct-v0-1", 
    messages=[
       {"role": "user", "content": "hello from litellm"}
   ],
)
print(response)
```

## Sample Usage - Streaming
```python
from litellm import completion
import os

os.environ['FRIENDLI_TOKEN'] = ""
response = completion(
    model="friendliai/mixtral-8x7b-instruct-v0-1", 
    messages=[
       {"role": "user", "content": "hello from litellm"}
   ],
    stream=True
)

for chunk in response:
    print(chunk)
```


## Supported Models - ALL FriendliAI Models Supported!
We support ALL FriendliAI AI models, just set `friendliai/` as a prefix when sending completion requests

| Model Name               | Function Call                                                                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mixtral-8x7b-instruct | `completion(model="friendliai/mixtral-8x7b-instruct-v0-1", messages)` | 
| meta-llama-3-8b-instruct | `completion(model="friendliai/meta-llama-3-8b-instruct", messages)` |
| meta-llama-3-70b-instruct | `completion(model="friendliai/meta-llama-3-70b-instruct", messages)` |  