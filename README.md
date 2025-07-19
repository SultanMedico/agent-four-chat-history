# agent-four-chat-history


✅ Yes, you can absolutely create a separate chat history file!

This means your conversation will be saved outside the code — in a .txt, .json, or .csv file — so you can:

View it later

Reload it next time the app runs

Or even use it in another tool

✅ Recommended: Use a .json file
It’s easy to read, edit, and works well with your existing chat_history = [{"role": ..., "content": ...}] format.

🔧 Let's Modify Your Code to Use chat_history.json
📄 Step 1: Create a file called chat_history.json
(You don’t need to create it manually — the code will do it.)

✏️ Step 2: Update main.py
Here’s the modified version that:

Loads chat history from chat_history.json (if it exists)

Saves history to the file after each message

💬 Example:
python
Copy
Edit
handle_query("What is the capital of France?")
handle_query("How old is that city?")
handle_query("What is it famous for?")
Even though the second and third questions don’t mention "Paris", the AI knows you’re still talking about Paris, because it's looking at the full conversation history like this:

vbnet
Copy
Edit
User: What is the capital of France?
Assistant: Paris is the capital of France.
User: How old is that city?
Assistant: Paris is over 2,000 years old...
User: What is it famous for?
Assistant: Paris is famous for the Eiffel Tower, art, fashion...
🔁 Why this works:
You’re passing the whole chat history into each prompt via:

python
Copy
Edit
full_prompt = build_prompt_from_history(chat_history)
So the AI "reads" the conversation before answering, just like a person would.




uv init . 
uv venv 
source .venv/bin/activate
uv add openai-agents
uv add python-dotenv
uv run main.py
uv run app.py


