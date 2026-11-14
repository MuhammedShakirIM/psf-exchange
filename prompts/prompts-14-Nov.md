1. This is not a production grade project. 
2. This is a learning project where I want you to give me - simple PoC code  using plain python libraries and required SDK from claude that would help to make token based API Calls to Claude Sonnet 5.5 model. Demonstrate the API call with a simple request and show the response on the console / terminal. 
3. Scaffold a new uv based python project and do the needful.

---- 


## Prompt for Groq

1. Now create the PoC for Groq. I have set the API key in the .env as GROQ_API_KEY
2. Use the following snippet as the reference
3. Add the required dependency and also install it

from groq import Groq

client = Groq()
completion = client.chat.completions.create(
    model="openai/gpt-oss-120b",
    messages=[
      {
        "role": "user",
        "content": ""
      }
    ],
    temperature=1,
    max_completion_tokens=2048,
    top_p=1,
    reasoning_effort="medium",
    stream=True,
    stop=None
)

for chunk in completion:
    print(chunk.choices[0].delta.content or "", end="")




# Project Structure

1. I am not happy with the struture of the project
2. I want you to restructure the project such that ./psf-ai-engineering is the root of the project with all the root files of the project like pyproject.tolm file
3. Run any poc code must be from the root project folder like : uv run claude_poc/<< the exact poc implementation file>> Do not implement the logic in  __init__.py   Likewise for all the PoCs in future




## PoC with Claude Subscription Adapter

1. Refer to the /Users/shakir/claude-subscription-adapter/README.md
2. Create new PoC called claude_subscription_poc in this project. note that I have already started the server.


