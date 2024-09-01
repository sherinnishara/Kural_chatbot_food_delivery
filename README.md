# Kural_tamil_food_delivery_chatbot

It is the entry level project "Kural- The Tamil Food Delivery Chatbot", built with Dialogflow Essential and it integrates text-to-speech (TTS) and speech-to-text (STT) technologies, helps Tamil-speaking users order foods easily. It supports both text and voice commands in tamil(also local tamil and thanglish) for a smooth ordering experience

Installations:\
1)Dialogflow Essential: For NLP agent creation.\
2)Database: mysql workbench 8.0 CE\
3)Mapping (Http to Https): Ngrok(version based on your OS)\
4)Text Editor: PyCharm 2024.1.6\
5)API integration(for webhook calls): FastAPI\

Requirements:\
---> pip install mysql-connector\
---> pip install "fastapi[all]"

FastAPI initialization:

Create a file main.py with:\
from typing import Union\
from fastapi import FastAPI\
app = FastAPI()\
@app.get("/")\
def read_root():\
    return {"Hello": "World"}\
@app.get("/items/{item_id}")\
def read_item(item_id: int, q: Union[str, None] = None):\
    return {"item_id": item_id, "q": q}

to start or restart FastAPI backend server:\
-->  Run this command: uvicorn main:app --reload\
[ensure your ngrok or https server doesn't time_out]\
if timeout clear cmd and restart ngrok

to start and restart ngrok\
----> Run this command: ngrok http 8000\
(your_localhost_address --> 8000)
_____________________________________________________________
My first project
[**if any problem in this repository please give me pull request**]
thank_you :)
