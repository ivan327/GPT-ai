# GPT-ai
@ivanm696's untitled project
Short description
Router/action
README
@ivanm696's untitled project
Short description
Router/action
README
Let everyone know what this project is about, how to use it and link to important resources.
Status updates
@ivanm696
ivanm696
1 minute ago
Status:

On track
title: gpt-oss-120b · Cloudflare Workers AI docs
description: OpenAI’s open-weight models designed for powerful reasoning,
agentic tasks, and versatile developer use cases – gpt-oss-120b is for
production, general purpose, high reasoning use-cases.
chatbotDeprioritize: false
source_url:
html: https://developers.cloudflare.com/workers-ai/models/gpt-oss-120b/
md: https://developers.cloudflare.com/workers-ai/models/gpt-oss-120b/index.md
OpenAI logo

gpt-oss-120b
Text Generation • OpenAI

@cf/openai/gpt-oss-120b

OpenAI’s open-weight models designed for powerful reasoning, agentic tasks, and versatile developer use cases – gpt-oss-120b is for production, general purpose, high reasoning use-cases.

Model Info
Context Window 128,000 tokens
Unit Pricing $0.35 per M input tokens, $0.75 per M output tokens
Usage
Worker

export default {
async fetch(request, env): Promise {
const response = await env.AI.run('@cf/openai/gpt-oss-120b', {
instructions: 'You are a concise assistant.',
input: 'What is the origin of the phrase Hello, World?',
});

return Response.json(response);
},
} satisfies ExportedHandler;
Python

import os
import requests

ACCOUNT_ID = os.environ.get("CLOUDFLARE_ACCOUNT_ID")
AUTH_TOKEN = os.environ.get("CLOUDFLARE_AUTH_TOKEN")

prompt = "Tell me all about PEP-8"
response = requests.post(
f"https://api.cloudflare.com/client/v4/accounts/{ACCOUNT_ID}/ai/v1/responses",
headers={"Authorization": f"Bearer {AUTH_TOKEN}"},
json={
"model": "@cf/openai/gpt-oss-120b",
"input": "Tell me all about PEP-8"
}
)
result = response.json()
print(result)
curl

curl https://api.cloudflare.com/client/v4/accounts/$CLOUDFLARE_ACCOUNT_ID/ai/v1/responses -H "Content-Type: application/json" -H "Authorization: Bearer $CLOUDFLARE_AUTH_TOKEN" -d '{
"model": "@cf/openai/gpt-oss-120b",
"input": "What are the benefits of open-source models?"
}'
Parameters

indicates a required field
Input
0 object

input required

0 string

Responses API Input messages. Refer to OpenAI Responses API docs to learn more about supported content types

1 array

Responses API Input messages. Refer to OpenAI Responses API docs to learn more about supported content types

reasoning object

effort string

Constrains effort on reasoning for reasoning models. Currently supported values are low, medium, and high. Reducing reasoning effort can result in faster responses and fewer tokens used on reasoning in a response.

summary string

A summary of the reasoning performed by the model. This can be useful for debugging and understanding the model's reasoning process. One of auto, concise, or detailed.

1 object

requests array required

items object

input required

0 string

Responses API Input messages. Refer to OpenAI Responses API docs to learn more about supported content types

1 array

Responses API Input messages. Refer to OpenAI Responses API docs to learn more about supported content types

reasoning object

effort string

Constrains effort on reasoning for reasoning models. Currently supported values are low, medium, and high. Reducing reasoning effort can result in faster responses and fewer tokens used on reasoning in a response.

summary string

A summary of the reasoning performed by the model. This can be useful for debugging and understanding the model's reasoning process. One of auto, concise, or detailed.

Output
0 object

1 string

API Schemas
The following schemas are based on JSON Schema

Input

{
"oneOf": [
{
"type": "object",
"title": "Responses",
"properties": {
"input": {
"anyOf": [
{
"type": "string"
},
{
"items": {},
"type": "array"
}
],
"description": "Responses API Input messages. Refer to OpenAI Responses API docs to learn more about supported content types"
},
"reasoning": {
"type": "object",
"properties": {
"effort": {
"type": "string",
"description": "Constrains effort on reasoning for reasoning models. Currently supported values are low, medium, and high. Reducing reasoning effort can result in faster responses and fewer tokens used on reasoning in a response.",
"enum": [
"low",
"medium",
"high"
]
},
"summary": {
"type": "string",
"description": "A summary of the reasoning performed by the model. This can be useful for debugging and understanding the model's reasoning process. One of auto, concise, or detailed.",
"enum": [
"auto",
"concise",
"detailed"
]
}
}
}
},
"required": [
"input"
]
},
{
"type": "object",
"title": "Async Request",
"properties": {
"requests": {
"type": "array",
"items": {
"type": "object",
"properties": {
"input": {
"anyOf": [
{
"type": "string"
},
{
"items": {},
"type": "array"
}
],
"description": "Responses API Input messages. Refer to OpenAI Responses API docs to learn more about supported content types"
},
"reasoning": {
"type": "object",
"properties": {
"effort": {
"type": "string",
"description": "Constrains effort on reasoning for reasoning models. Currently supported values are low, medium, and high. Reducing reasoning effort can result in faster responses and fewer tokens used on reasoning in a response.",
"enum": [
"low",
"medium",
"high"
]
},
"summary": {
"type": "string",
"description": "A summary of the reasoning performed by the model. This can be useful for debugging and understanding the model's reasoning process. One of auto, concise, or detailed.",
"enum": [
"auto",
"concise",
"detailed"
]
}
}
}
},
"required": [
"input"
]
}
}
},
"required": [
"requests"
]
}
]
}
Output

{
"oneOf": [
{
"type": "object",
"contentType": "application/json"
},
{
"type": "string",
"contentType": "text/event-stream",
"format": "binary"
}
]
}
@ivanm696
ivanm696
on Nov 11
Status:

On track
🖥

@ivanm696
ivanm696
on Nov 11
Status:

On track
Skip to content
Navigation Menu
@ivanm696's untitled project

@ivanm696's untitled project
View 1
Filter
status:Todo
Create azure-webapps-node.yml
#2
You can use control
Control
+
space
Space
to add an item
List updated, Focused item: Inactive, not selected, 1 of 5

Status updates
@ivanm696
ivanm696
1 minute ago
Status:

On track
@ivanm696
ivanm696
2 minutes ago
Status:

On track
title: gpt-oss-120b · Cloudflare Workers AI docs
description: OpenAI’s open-weight models designed for powerful reasoning,
agentic tasks, and versatile developer use cases – gpt-oss-120b is for
production, general purpose, high reasoning use-cases.
chatbotDeprioritize: false
source_url:
html: https://developers.cloudflare.com/workers-ai/models/gpt-oss-120b/
md: https://developers.cloudflare.com/workers-ai/models/gpt-oss-120b/index.md
OpenAI logo

gpt-oss-120b
Text Generation • OpenAI

@cf/openai/gpt-oss-120b

OpenAI’s open-weight models designed for powerful reasoning, agentic tasks, and versatile developer use cases – gpt-oss-120b is for production, general purpose, high reasoning use-cases.

Model Info	
Context Window	128,000 tokens
Unit Pricing	$0.35 per M input tokens, $0.75 per M output tokens
Usage
Worker

export default {
  async fetch(request, env): Promise<Response> {
    const response = await env.AI.run('@cf/openai/gpt-oss-120b', {
      instructions: 'You are a concise assistant.',
      input: 'What is the origin of the phrase Hello, World?',
    });


    return Response.json(response);
  },
} satisfies ExportedHandler<Env>;
Python

import os
import requests


ACCOUNT_ID = os.environ.get("CLOUDFLARE_ACCOUNT_ID")
AUTH_TOKEN = os.environ.get("CLOUDFLARE_AUTH_TOKEN")


prompt = "Tell me all about PEP-8"
response = requests.post(
  f"https://api.cloudflare.com/client/v4/accounts/{ACCOUNT_ID}/ai/v1/responses",
    headers={"Authorization": f"Bearer {AUTH_TOKEN}"},
    json={
      "model": "@cf/openai/gpt-oss-120b",
      "input": "Tell me all about PEP-8"
    }
)
result = response.json()
print(result)
curl

curl https://api.cloudflare.com/client/v4/accounts/$CLOUDFLARE_ACCOUNT_ID/ai/v1/responses   -H "Content-Type: application/json"   -H "Authorization: Bearer $CLOUDFLARE_AUTH_TOKEN"   -d '{
    "model": "@cf/openai/gpt-oss-120b",
    "input": "What are the benefits of open-source models?"
  }'
Parameters
* indicates a required field

Input
0 object

input required

0 string

Responses API Input messages. Refer to OpenAI Responses API docs to learn more about supported content types

1 array

Responses API Input messages. Refer to OpenAI Responses API docs to learn more about supported content types

reasoning object

effort string

Constrains effort on reasoning for reasoning models. Currently supported values are low, medium, and high. Reducing reasoning effort can result in faster responses and fewer tokens used on reasoning in a response.

summary string

A summary of the reasoning performed by the model. This can be useful for debugging and understanding the model's reasoning process. One of auto, concise, or detailed.

1 object

requests array required

items object

input required

0 string

Responses API Input messages. Refer to OpenAI Responses API docs to learn more about supported content types

1 array

Responses API Input messages. Refer to OpenAI Responses API docs to learn more about supported content types

reasoning object

effort string

Constrains effort on reasoning for reasoning models. Currently supported values are low, medium, and high. Reducing reasoning effort can result in faster responses and fewer tokens used on reasoning in a response.

summary string

A summary of the reasoning performed by the model. This can be useful for debugging and understanding the model's reasoning process. One of auto, concise, or detailed.

Output
0 object

1 string

API Schemas
The following schemas are based on JSON Schema

Input

{
    "oneOf": [
        {
            "type": "object",
            "title": "Responses",
            "properties": {
                "input": {
                    "anyOf": [
                        {
                            "type": "string"
                        },
                        {
                            "items": {},
                            "type": "array"
                        }
                    ],
                    "description": "Responses API Input messages. Refer to OpenAI Responses API docs to learn more about supported content types"
                },
                "reasoning": {
                    "type": "object",
                    "properties": {
                        "effort": {
                            "type": "string",
                            "description": "Constrains effort on reasoning for reasoning models. Currently supported values are low, medium, and high. Reducing reasoning effort can result in faster responses and fewer tokens used on reasoning in a response.",
                            "enum": [
                                "low",
                                "medium",
                                "high"
                            ]
                        },
                        "summary": {
                            "type": "string",
                            "description": "A summary of the reasoning performed by the model. This can be useful for debugging and understanding the model's reasoning process. One of auto, concise, or detailed.",
                            "enum": [
                                "auto",
                                "concise",
                                "detailed"
                            ]
                        }
                    }
                }
            },
            "required": [
                "input"
            ]
        },
        {
            "type": "object",
            "title": "Async Request",
            "properties": {
                "requests": {
                    "type": "array",
                    "items": {
                        "type": "object",
                        "properties": {
                            "input": {
                                "anyOf": [
                                    {
                                        "type": "string"
                                    },
                                    {
                                        "items": {},
                                        "type": "array"
                                    }
                                ],
                                "description": "Responses API Input messages. Refer to OpenAI Responses API docs to learn more about supported content types"
                            },
                            "reasoning": {
                                "type": "object",
                                "properties": {
                                    "effort": {
                                        "type": "string",
                                        "description": "Constrains effort on reasoning for reasoning models. Currently supported values are low, medium, and high. Reducing reasoning effort can result in faster responses and fewer tokens used on reasoning in a response.",
                                        "enum": [
                                            "low",
                                            "medium",
                                            "high"
                                        ]
                                    },
                                    "summary": {
                                        "type": "string",
                                        "description": "A summary of the reasoning performed by the model. This can be useful for debugging and understanding the model's reasoning process. One of auto, concise, or detailed.",
                                        "enum": [
                                            "auto",
                                            "concise",
                                            "detailed"
                                        ]
                                    }
                                }
                            }
                        },
                        "required": [
                            "input"
                        ]
                    }
                }
            },
            "required": [
                "requests"
            ]
        }
    ]
}
Output

{
    "oneOf": [
        {
            "type": "object",
            "contentType": "application/json"
        },
        {
            "type": "string",
            "contentType": "text/event-stream",
            "format": "binary"
        }
    ]
}
@ivanm696
ivanm696
on Nov 11
Status:

On track
🖥

@ivanm696
ivanm696
on Nov 11
Status:

On track
Skip to content
