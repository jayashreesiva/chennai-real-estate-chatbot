# Chennai Real Estate AI - Demo v3

A modern frontend prototype for an AI-powered Chennai real estate assistant.

This project demonstrates the user interface and interaction flow for a future RAG-based real estate chatbot with property search, conversation, voice input/output, location search, property details, nearby facilities, and broker information.

## ✨ Features

### 💬 Chatbot Conversation

The chatbot supports normal conversations such as:

- Hi
- Hello
- Good morning
- Good afternoon
- Good evening
- Thank you

Example:

User:
> Hi

Bot:
> Hi! How can I help you with Chennai properties today?

User:
> Thank you

Bot:
> You're welcome! I'm happy to help.

---

### 🏡 Property Search

Users can search for properties using natural-language queries.

Examples:

```text
Show me 3 BHK properties in Velachery
I need a 3 BHK property in Anna Nagar
Show me properties in Ambattur

The system displays matching properties based on the requested Chennai area.
This version keeps the approved design and makes the requested interaction changes.



                       🏠 HOME
                            │
                            ↓
                 ┌────────────────────┐
                 │ Text / Voice Query │
                 └─────────┬──────────┘
                           ↓
                  Language Processing
                           ↓
                  Query Understanding
                           ↓
                  Conversation Memory
                           ↓
                    FAISS Retrieval
                           ↓
                 ┌─────────┴─────────┐
                 ↓                   ↓
           Properties            Nearby Data
                 │                   │
                 └─────────┬─────────┘
                           ↓
                     RAG Context
                           ↓
                         Gemini
                           ↓
                    AI Response
                           ↓
                    4–5 Results
                           ↓
              ┌────────────┼────────────┐
              ↓            ↓            ↓
           Property 1   Property 2   Property 3
              │            │            │
          [ VIEW ]      [ VIEW ]      [ VIEW ]
              │            │            │
              ↓            ↓            ↓
          Details      Details      Details
              │
       ┌──────┼──────────────┐
       ↓      ↓      ↓       ↓
     Images  Nearby  Broker  Location

     🌐 Language access[multiple languages]

English
தமிழ்
हिन्दी
...

Property Cards

Each search result displays:

Property name
Property ID
Property image
Price
BHK
Area
Bathrooms
Location
Property status

Nearby Facilities

The property detail page displays nearby facilities related to the selected property.

Examples:

Nearby Schools
- DAV Public School
- Velammal Main School
Nearby College
- Loyola College
Nearby Hospital
- Apollo Hospitals
Nearby Supermarket
- Reliance SMART
Local Transport
- Velachery MRTS Station

Property Location

Each property has an area-level location.

The application provides:

Open this location in Google Maps

Clicking this opens Google Maps for the property's area.

Example:

Velachery, Chennai

Voice Input

The prototype includes a microphone button.

Click:

🎙️ Speak

Then speak your query.

Example:

Show me three BHK properties in Velachery

The speech is converted into text and placed into the chatbot input.

The chatbot then processes the query.

Microphone permission must be allowed in Google Chrome.

Voice Output

Bot responses include a:

🔊 Listen

button.

Clicking it reads the chatbot response aloud.

The selected language controls the speech language when the browser supports it.
Hallucination Control

The final RAG system should avoid creating information that does not exist in the knowledge base.

For example, if the database does not contain swimming-pool information:

User:
Does this property have a swimming pool?

The chatbot should respond with something like:

Swimming-pool information is not available
in the current knowledge base.

It should not invent an amenity.

<img width="1762" height="797" alt="Screenshot 2026-09-24 212430" src="https://github.com/user-attachments/assets/18406acb-d2ca-4379-8bdb-2acfffaf94d1" />
<img width="1737" height="972" alt="Screenshot 2026-09-24 213729" src="https://github.com/user-attachments/assets/79bd1f53-e607-4733-aed3-b09b2d5896bb" />
<img width="1830" height="886" alt="Screenshot 2026-09-24 213858" src="https://github.com/user-attachments/assets/f469d731-7a4f-49ec-8c4c-8335d25d20aa" />
<img width="1730" height="886" alt="Screenshot 2026-09-24 213915" src="https://github.com/user-attachments/assets/968bf432-a381-41f0-a0b4-4b5732c743cb" />
<img width="1790" height="876" alt="Screenshot 2026-09-24 213931" src="https://github.com/user-attachments/assets/2a893d08-39ce-45fb-a07f-d233163cd9a2" />

### Updated
- Natural greetings: Hi, Hello, Good morning/evening
- Thank you -> You're welcome
- Emoji are NOT sent to speech synthesis, so voice does not read out emoji descriptions
- Search response for a property query is only: "I found 4 matching properties."
- Four separate property cards
- Each View Property button opens that property's own details
- Nearby schools, college, hospital, supermarket and local transport are shown
- Google Maps opens the relevant area for each demo property
- Broker name, ID and clearly labelled DEMO contact number are shown
- Search/Ask controls stay at the bottom of the chat box
- User question stays above its answer in the conversation
- Removed suggestion/example chips
- Removed extra text below the main project content
- Green/light-green visual style retained

### Important
The property records, nearby facility associations and broker phone numbers in this prototype are sample/demo data. They are intentionally labelled as demo information where appropriate. The final project should replace them with verified project datasets.

### Run
Extract the ZIP and open `index.html` in Google Chrome. Allow microphone permission for voice input.
