# API Usage Examples

This section provides examples of how to interact with our APIs directly from the command line using `curl`. 

## Text Summarization API

To use the Text Summarization API, you can send a POST request with the text you want to summarize and specify the number of words for the summary. Here's an example command:

```bash
curl -s -XPOST "https://samanshrestha.ap-south-1.modelbit.com/v1/summarize_thread/latest" -d '{"data": ["Your text here", num_of_words]}' | json_pp

```

## Text Classification API

The Text Classification API allows you to classify a given text into predefined categories. Follow the example below to learn how to use this API with a `curl` command.

To classify your text, send a POST request with the data you want to classify. Below is a template of the `curl` command for sending your request:

```bash
curl -s -XPOST "https://samanshrestha.ap-south-1.modelbit.com/v1/classifer_text/latest" -d '{"data": "Your data here"}' | json_pp
```

### Python Code

```python
import json
import requests

# Change `ENTER_WORKSPACE_NAME` to your workspace name
response = requests.post(
    "https://samanshrestha.ap-south-1.modelbit.com/v1/classifer_text/latest",
    headers={"Content-Type": "application/json"},
    data=json.dumps(
        {
            "data": [
                "URGENT! You have won a 1 week FREE membership in our £100,000 Prize Jackpot! Txt the word: CLAIM",
            ]
        }
    ),
)

print(response.json())
