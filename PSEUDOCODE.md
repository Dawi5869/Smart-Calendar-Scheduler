START PROGRAM

AUTHENTICATE with Google Calendar API
  IF token.json exists:
    LOAD credentials
  ELSE:
    RUN OAuth flow with credentials.json
    SAVE token.json for future use

DISPLAY main options:
  1. Add new event(s) and reorganize
  2. Reorganize existing events
  3. Summarize events for a custom time slot

PROMPT user for a scheduling end date
CONVERT date into datetime format with timezone

IF user selects:
  OPTION 1: ADD + REORGANIZE
    - Prompt user for number of events to add
    - For each event:
        - Get title, estimated duration, due date, priority, and description
        - Store metadata in a temporary dictionary
    - Retrieve events from Google Calendar up to the given end date
    - Categorize into:
        - Movable (based on metadata in event description)
        - Fixed (default or non-movable)
    - Add fixed events to unavailable time slots
    - Sort movable events by due date and priority
    - For each movable event:
        - Search for the earliest available slot
        - If found, schedule the event in Google Calendar
        - If not, skip and log a message

  OPTION 2: REORGANIZE EXISTING EVENTS
    - Retrieve all events up to the given end date
    - Categorize into movable/fixed as described above
    - Add fixed events to unavailable time slots
    - Sort and reschedule movable events as described above

  OPTION 3: SUMMARIZE A TIME RANGE
    - Ask user for start and end dates
    - Fetch events within that range from Google Calendar
    - Convert events into a readable summary format
    - Send summary and user’s custom question to Gemini AI
    - Display Gemini's response to the user

END PROGRAM
