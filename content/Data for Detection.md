
Data for detection can be broadly categorized into response data, response paradata, and response metadata. 

**Response data** have to do with the content of the responses themselves, such as the selected option in a multiple-choice item or the string of characters in an open-ended item, and derived metrics like total scores or subscores. Most psychometric methods focus on response data as the only source of information. For example, the Rasch model (a.k.a. the 1PL IRT model) uses only the total score to estimate respondent abilities. For the purpose of AI response detection, response data remain a critical source of information, especially for open-ended items. 

**Response paradata** have to do with the response process (e.g. response times, mouse movements, or keystrokes). Response paradata are typically collected in process/log files, while contain long sequences of time-stamped events. Events include various types of user interactions and system changes, such as clicking on answer choices, switching tabs, or using copy/paste. For the purpose of AI response detection, response paradata is a critical source of information as various forms of genuine, AI-assisted, and AI-agent responding are expected to differ in the way they navigate online platforms. 

**Response metadata** include additional information about the response beyond the content of the response or the response process, such as network, software, or hardware information. Response metadata is not as central to AI response detection, but response metadata can be helpful for identifying potential fraud, such as when multiple responses share the same IP address or have suspiciously similar process features. 

---
Next [[Response Data]]
Next [[Response Paradata]]
Next [[Response Metadata]]

