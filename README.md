# TalentScout AI-Powered Candidate Screener

This project is an AI-powered candidate screener built with Python, Gradio, OpenAI, and FPDF.  
It offers both a conversational chatbot interface and a classic form, allowing users to complete the screening process in the style they prefer.  
At the end, users can download a summary PDF including their responses and AI-generated technical questions.

---

## Features

- **Chatbot Mode:** Conversational, one-question-at-a-time AI interview.
- **Regular Form Mode:** Classic form, all fields visible, submit at once.
- **OpenAI Integration:** Generates technical interview questions based on the candidate's tech stack.
- **PDF Summary:** Downloadable candidate summary with all answers, detected frameworks, and AI-generated questions.
- **Internationalization:** Supports all major country codes.
- **Robust Validation:** Per-field validation for each input, user-friendly error messages.

---

## Installation

pip install gradio openai fpdf

## Usage

1. **Set your OpenAI API key**  
   Open the Python file and replace the placeholder with your OpenAI API key:

   openai.api_key = "YOUR_OPENAI_API_KEY_HERE"

2. **Run the App**
   python your_script_name.py

3. **Open the Interface**
- The Gradio app will launch in your browser.
- Use either the **Chatbot** tab for a conversational experience, or the **Regular Form** tab to fill out all fields at once.

4. **Download PDF**
- After completion, click the **Download PDF** button to save your candidate summary.

---

## Fields Collected

- Full Name
- Email Address
- Country Code (dropdown, all international codes)
- Phone Number (10 digits, no country code)
- Years of Experience
- Roles Worked
- Project Descriptions (with optional links)
- Position(s) Applied For
- Current Location
- Tech Stack (e.g., Python, Django, React, C++, Node.js, C#)

---

## Validation Rules

- **Name:** Only alphabets and spaces.
- **Email:** Must be valid and end with `.com`.
- **Country Code:** Must be selected from the dropdown.
- **Phone:** Exactly 10 digits, no country code.
- **Experience:** Numeric, in years.
- **Roles, Projects:** Cannot be blank.
- **Position, Location:** Only alphabets and spaces.
- **Tech Stack:** Cannot be empty or multiline.

---

## AI/LLM Usage

- The app uses OpenAI's GPT-3.5-turbo to generate technical interview questions based on the tech stack provided by the candidate.

---

## PDF Output

- The summary PDF includes all answers, detected frameworks/libraries (if any), and the generated technical questions.

---

## Customization

- You can modify the questions, validation, or PDF formatting by editing the corresponding sections in the Python script.

---

## Troubleshooting

- **OpenAI errors:** Verify your API key and network connection.
- **Validation errors:** Ensure all fields meet the specified requirements.
- **PDF download issues:** Check your browser's download settings.

---

## License

MIT License

---

## Credits

Built with [Gradio](https://gradio.app/), [OpenAI](https://platform.openai.com/), and [FPDF](https://pyfpdf.github.io/).

---
