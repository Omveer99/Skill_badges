# Get Started with Pub/Sub: Challenge Lab

## Run in cloud Shell 

```bash
export TOPIC_NAME=
```


```bash
export SUBSCRIPTION_NAME=
```

```bash
export JOB_NAME=
```

```bash
export MESSAGE_BODY=
```

```bash
export REGION=
```

```bash
gcloud pubsub topics create $TOPIC_NAME
```

```bash
gcloud pubsub subscriptions create $SUBSCRIPTION_NAME --topic=$TOPIC_NAME
```

```bash
gcloud services enable cloudscheduler.googleapis.com
```


```bash
gcloud scheduler jobs create pubsub $JOB_NAME --schedule="* * * * *" --topic=$TOPIC_NAME --message-body="$MESSAGE_BODY" --time-zone="Etc/UTC" --description="subscribe to quicklab" --project=$DEVSHELL_PROJECT_ID --location=$REGION
```
