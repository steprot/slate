--- 

title: Nucleus API 

language_tabs: 
   - shell 

toc_footers: 
   - <a href='#'>Sign Up for a Developer Key</a> 
   - <a href='https://github.com/lavkumarv'>Documentation Powered by lav</a> 

includes: 
   - errors 

search: true 

--- 

# Introduction 

Nucleus text analytics APIs from SumUp Analytics. Example and documentation: https://github.com/SumUpAnalytics/nucleus-sdk 

**Version:** v2.4.1 

# Authentication 

|apiKey|*API Key*|
|---|---| 

# /DATASETS
## ***GET*** 

**Description:** List the datasets owned by the user.

### HTTP Request 
`***GET*** /datasets` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| consumes | textHtml |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /DATASETS/APPEND_JSON_TO_DATASET
## ***POST*** 

**Description:** Add a document to a dataset, in JSON form.

### HTTP Request 
`***POST*** /datasets/append_json_to_dataset` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /DATASETS/BULK_INSERT_JSON
## ***POST*** 

**Description:** Add many document to a dataset, in JSON form. Bulk insertion is much faster than making one api call for each document.

### HTTP Request 
`***POST*** /datasets/bulk_insert_json` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /DATASETS/DATASET_INFO
## ***POST*** 

**Description:** Get information about a dataset.

### HTTP Request 
`***POST*** /datasets/dataset_info` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /DATASETS/DATASET_TAGGING
## ***POST*** 

**Description:** Tag documents containig specified entities within a dataset.

### HTTP Request 
`***POST*** /datasets/dataset_tagging` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /DATASETS/DELETE_DATASET
## ***POST*** 

**Description:** Delete an existing dataset from the user storage.

### HTTP Request 
`***POST*** /datasets/delete_dataset` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /DATASETS/DELETE_DOCUMENT
## ***POST*** 

**Description:** Delete documents from a dataset.

### HTTP Request 
`***POST*** /datasets/delete_document` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /DATASETS/IMPORT_FILE_FROM_URL
## ***POST*** 

### HTTP Request 
`***POST*** /datasets/import_file_from_url` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /DATASETS/RENAME_DATASET
## ***POST*** 

**Description:** Rename an existing dataset.

### HTTP Request 
`***POST*** /datasets/rename_dataset` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /DATASETS/UPLOAD_FILE
## ***POST*** 

### HTTP Request 
`***POST*** /datasets/upload_file` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| metadata | query | Optional json containing additional document metadata. Eg: {"time":"01/01/2001","author":"me"} | No | string |
| file | formData |  | Yes | file |
| dataset | query | Destination dataset where the file will be inserted. | Yes | string |
| filename | query | Specify the filename if you want to override the original filename (Nucleus guesses the file type from the file name extension) | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /DOCUMENTS/DOCUMENT_CLASSIFY
## ***POST*** 

**Description:** Document one-layer classifier on a chosen dataset.

### HTTP Request 
`***POST*** /documents/document_classify` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /DOCUMENTS/DOCUMENT_CONTRASTED_SUMMARY
## ***POST*** 

**Description:** Document contrasted summarization.

### HTTP Request 
`***POST*** /documents/document_contrasted_summary` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /DOCUMENTS/DOCUMENT_DISPLAY
## ***POST*** 

**Description:** Document display.

### HTTP Request 
`***POST*** /documents/document_display` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /DOCUMENTS/DOCUMENT_INFO
## ***POST*** 

**Description:** Retrieve metadata of documents matching the provided filter (limited to 10000 documents).

### HTTP Request 
`***POST*** /documents/document_info` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /DOCUMENTS/DOCUMENT_RECOMMEND
## ***POST*** 

**Description:** Recommendation of documents on given topics that have been extracted from a given dataset.

### HTTP Request 
`***POST*** /documents/document_recommend` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /DOCUMENTS/DOCUMENT_SENTIMENT
## ***POST*** 

**Description:** Document sentiment.

### HTTP Request 
`***POST*** /documents/document_sentiment` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /DOCUMENTS/DOCUMENT_SUMMARY
## ***POST*** 

**Description:** Document summarization.

### HTTP Request 
`***POST*** /documents/document_summary` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /FEEDS/AVAILABLE_SEC_FILINGS
## ***POST*** 

**Description:** Get information about the available sec filings. If no input is passed, returns the list of all available tickers. If tickers are passed, returns the list of available document types for these tickers. If documt types are also passed, returns the list of available secions for the selected tickers/filing types

### HTTP Request 
`***POST*** /feeds/available_sec_filings` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /FEEDS/CREATE_DATASET_FROM_SEC_FILINGS
## ***POST*** 

**Description:** Creates a new dataset and populates it with sec filings matching the specified tickers/form types.

### HTTP Request 
`***POST*** /feeds/create_dataset_from_sec_filings` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /FILTERS
## ***GET*** 

**Description:** List the filters owned by the user.

### HTTP Request 
`***GET*** /filters` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| consumes | textHtml |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /FILTERS/DELETE_FILTER
## ***POST*** 

**Description:** Delete a filter.

### HTTP Request 
`***POST*** /filters/delete_filter` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /FILTERS/SAVE_FILTER
## ***POST*** 

**Description:** Save a filter representing a subsect of a dataset (time range, query, metadata..).

### HTTP Request 
`***POST*** /filters/save_filter` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /JOBS
## ***GET*** 

**Description:** Use this API to check the progress and retrieve results of a job. Poll this endpoint repeatedly until result is not null.

### HTTP Request 
`***GET*** /jobs` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | query | ID of the job | Yes | string |
| consumes | textHtml |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /JOBS/START_EXAMPLE_JOB
## ***POST*** 

**Description:** Start an example background job

### HTTP Request 
`***POST*** /jobs/start_example_job` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| color | query | A color | Yes | string |
| wait_time | query | Seconds to wait before returning the result | Yes | integer |
| consumes | textHtml |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /LEGACY
## ***POST*** 

**Description:** Recommendation of documents on given topics that have been extracted from a given dataset.

### HTTP Request 
`***POST*** /legacy` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /TOPICS/AUTHOR_CONNECTIVITY
## ***POST*** 

**Description:** Get the network of similar authors to a reference author.

### HTTP Request 
`***POST*** /topics/author_connectivity` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /TOPICS/TOPIC_CONSENSUS
## ***POST*** 

**Description:** Get topic consensus for topics extracted from a given dataset.

### HTTP Request 
`***POST*** /topics/topic_consensus` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /TOPICS/TOPIC_CONSENSUS_TRANSFER
## ***POST*** 

**Description:** Get exposures of documents in a validation dataset to topics extracted from a reference dataset.

### HTTP Request 
`***POST*** /topics/topic_consensus_transfer` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /TOPICS/TOPIC_CONTRAST
## ***POST*** 

**Description:** Contrasting topic extraction on a chosen dataset.

### HTTP Request 
`***POST*** /topics/topic_contrast` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /TOPICS/TOPIC_DELTA
## ***POST*** 

**Description:** Get changes in exposure to key topics from documents in a dataset in between two dates.

### HTTP Request 
`***POST*** /topics/topic_delta` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /TOPICS/TOPIC_HISTORICAL
## ***POST*** 

**Description:** Get a historical analysis of topics extracted from a dataset.

### HTTP Request 
`***POST*** /topics/topic_historical` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /TOPICS/TOPIC_SENTIMENT
## ***POST*** 

**Description:** Get topic sentiment for topics extracted from a given dataset.

### HTTP Request 
`***POST*** /topics/topic_sentiment` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /TOPICS/TOPIC_SENTIMENT_TRANSFER
## ***POST*** 

**Description:** Get sentiment exposures of documents in a validation dataset to topics extracted from a reference dataset.

### HTTP Request 
`***POST*** /topics/topic_sentiment_transfer` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /TOPICS/TOPIC_SUMMARY
## ***POST*** 

**Description:** Get summaries of topics that have been extracted from a dataset.

### HTTP Request 
`***POST*** /topics/topic_summary` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /TOPICS/TOPIC_TRANSFER
## ***POST*** 

**Description:** Get exposures of documents in a validation dataset to topics extracted from a reference dataset.

### HTTP Request 
`***POST*** /topics/topic_transfer` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /TOPICS/TOPICS
## ***POST*** 

**Description:** Get key topics from a given dataset.

### HTTP Request 
`***POST*** /topics/topics` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Failed |

# /USERS
## ***POST*** 

**Description:** Use this API to register a new user. Email and password are required, all other fields optional.

### HTTP Request 
`***POST*** /users` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| payload | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

## ***GET*** 

**Description:** Use this API to authenticate. If the password is correct, returns the user details, including the user's api key.

### HTTP Request 
`***GET*** /users` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| user_email | query | Email of the user to authenticate.  | Yes | string |
| password | query | Plaintext password of the user to authenticate.  | Yes | string |
| consumes | textHtml |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
