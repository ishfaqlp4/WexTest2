
# Salesforce Einstein Chat Bot Coupon Code Capture




## Overview
This project facilitates the integration of Salesforce Einstein Chat Bot to capture coupon codes from website cookies. It utilizes JavaScript and Salesforce Live Agent for seamless communication.
## Implementation
The key functionalities include:
- Integration with Einstein Chat Bot
- Retrieval of all cookies from the website
- Processing and extraction of specific cookie values (`wex_cc_persistent` and `wex_cc_session`)
- Configuration of pre-chat form details with the extracted cookie value
- LiveAgent setup for real-time communication
## Usage

1. Include the provided JavaScript code in your website.
2. Ensure the necessary Salesforce Einstein Chat Bot configurations are in place.
3. Ensure a custom field in Salesforce Object LiveChatTranscript is created to store the coupon code value. It must be the same as the field name in the code ""transcriptFields" : ["Coupon_Code__c"]"
4. The system will automatically capture and transmit relevant coupon code information during chat sessions.


## Code Structure
- Einstein Chat Bot Integration: Configuration of Einstein Chat Bot for seamless interaction.
- Cookie Capture: JavaScript code to retrieve, process, and extract coupon code information from website cookies. The code first searches for copon code in wex_cc_session, if empty, it searches wex_cc_persistent.
- LiveAgent Setup: Configuration for real-time communication using Salesforce LiveAgent.

## Dependencies
- Salesforce Einstein Chat Bot
- Salesforce LiveAgent
- Custom Field in LiveChatTranscript
## Setup
1. Include the provided JavaScript code on your website.
2. Configure Einstein Chat Bot and LiveAgent settings in accordance with your Salesforce instance.
## Authors

- Mohammed Khan, Sr Software Developer | Cognizant

