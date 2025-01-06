# Assignment-2.14

1. Does SNS guarantee exactly once delivery to subscribers?
2. What is the purpose of the Dead-letter Queue (DLQ)? This a feature available to SQS/SNS/EventBridge.
3. How would you enable a notification to your email when messages are added to the DLQ?

# Answers

1. SNS does not guarantee once delivery to subscribers. SNS provides at least once delivery meaning message can be delivered multiple times.

2. A Dead-letter Queue is used to handle messages that cannot be successfully processed after a specific number of attempts. The purpose is to isolate problematic messages so that the main process flow can continue. The messages that failed to process are captured so that we can troubleshoot the reasons for failure without losing any messages. We can also retry to run the logic in the DLC Queue after addressing any issues found.

3. We can do this by using Simple Notification Service to our email address along with Lambda and CloudWatch.
