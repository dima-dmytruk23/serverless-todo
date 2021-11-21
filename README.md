## Setup

```bash
npm install -g serverless
```

## Deploy

In order to deploy the endpoint simply run

```bash
serverless deploy
```

## Usage

You can create, retrieve, update, or delete todos with the following commands:

### Create a Todo

```bash
curl -X POST https://w81p72wbq8.execute-api.us-west-1.amazonaws.com/dev/todos --data '{ "text": "Learn Serverless" }'
```

No output

### List all Todos

```bash
curl https://w81p72wbq8.execute-api.us-west-1.amazonaws.com/dev/todos
```

Example output:
```bash
[{"text":"Deploy my first service","id":"ac90feaa11e6-9ede-afdfa051af86","checked":true,"updatedAt":1479139961304},{"text":"Learn Serverless","id":"206793aa11e6-9ede-afdfa051af86","createdAt":1479139943241,"checked":false,"updatedAt":1479139943241}]%
```

### Get one Todo

```bash
# Replace the <id> part with a real id from your todos table
curl https://w81p72wbq8.execute-api.us-west-1.amazonaws.com/dev/todos/<id>
```

Example Result:
```bash
{"text":"Learn Serverless","id":"ee6490d0-aa11e6-9ede-afdfa051af86","createdAt":1479138570824,"checked":false,"updatedAt":1479138570824}%
```

### Update a Todo

```bash
# Replace the <id> part with a real id from your todos table
curl -X PUT https://w81p72wbq8.execute-api.us-west-1.amazonaws.com/dev/todos/<id> --data '{ "text": "Learn Serverless", "checked": true }'
```

Example Result:
```bash
{"text":"Learn Serverless","id":"ee6490d0-aa11e6-9ede-afdfa051af86","createdAt":1479138570824,"checked":true,"updatedAt":1479138570824}%
```

### Delete a Todo

```bash
# Replace the <id> part with a real id from your todos table
curl -X DELETE https://w81p72wbq8.execute-api.us-west-1.amazonaws.com/dev/todos/<id>
```
