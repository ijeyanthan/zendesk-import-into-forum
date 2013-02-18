import-into-zendesk-forum
=========================

A Python Script to import bunch of offline HTML files into Zendesk Forum creating Topics in a Forum under Categories

To know more, visit http://developer.zendesk.com/documentation/rest_api/forums.html for the list of possible JSON requests available in Zendesk.

Example request that I tweaked is using curl.

curl https://yoursubdomain.zendesk.com/api/v2/topics.json \
 -H "Content-Type: application/json" -v -u email:password -X POST \
 -d '{"topic": {"forum_id": 79161, "title": "My Topic", "body":"<code>This is some code</code>", "topic_type": "articles", "access": "logged in users" }'`
