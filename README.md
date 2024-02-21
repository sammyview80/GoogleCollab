Text Summarization: curl -s -XPOST "https://samanshrestha.ap-south-1.modelbit.com/v1/summarize_thread/latest" -d '{"data": [text, num_of_words]}' | json_pp
Text Classification: curl -s -XPOST "https://samanshrestha.ap-south-1.modelbit.com/v1/classifer_text/latest" -d '{"data": data}' | json_pp
