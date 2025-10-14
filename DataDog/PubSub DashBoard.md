# [Google Cloud Pubsub](https://docs.datadoghq.com/integrations/google_cloud_pubsub/#data-collected)

## DashBoard >> GCP: Pub/Sub Summary
1. Sends per second (project:*) : Number of publish message operations.
2. Oldest unack'ed message (project:*) : Age of the oldest unacknowledged message in a subscription.
3. Messages sent (project:*) : Cumulative count of messages sent by Cloud Pub/Sub to subscriber clients.
4. Messages ack'ed (project:*) : Cumulative count of messages acknowledged by Acknowledge requests, grouped by delivery type.
5. Bytes in backlog (project:*) : Approximate size of the message backlog in a subscription.
6. Expired ack deadlines (project_id:*) : Cumulative count of messages whose ack deadline expired while the messages was outstanding to a subscriber client.
7. Pending messages (project_id:*) : Messages pending to be delivered.

## DashBoard >> logged-data-cache pubsub
1. gcp.pubsub.topic.send_request_count : Number of message send requests.
2. gcp.pubsub.topic.send_message_operation_count : Number of publish message operations.
3. gcp.pubsub.subscription.ack_message_count : Cumulative count of messages acknowledged by Acknowledge requests, grouped by delivery type.
4. gcp.pubsub.subscription.sent_message_count : Cumulative count of messages sent by Cloud Pub/Sub to subscriber clients.
5. gcp.pubsub.subscription.streaming_pull_message_operation_count : Cumulative count of streaming pull message operations, grouped by result.

## DashBoard >> Google Cloud PubSub
1. Bytes used by subscriptions : Cost of operations per subscription measured.
2. Bytes used by topics : Byte cost of operations per topic.
- Topic
3. Publish message operations by response code : Number of publish message operations.
4. Message send requests by response code : Number of message send requests.
5. Average message size : Average of publish message sizes.
6. Configuration changes by operation type : Number of configuration changes for topics.
- Subscription
7. Oldest unacknowledged message : Age of the oldest unacknowledged message in a subscription.
8. Number of unacknowledged messages : Messages delivered but not yet acknowledged.
9. Undelivered messages by subscription : Messages pending to be delivered.
10. Pull request count by response code : Number of message pull requests.
11. Push request count by response class : Number of message push attempts.
