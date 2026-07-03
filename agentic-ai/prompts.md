# AI Prompts

## Project

Auto-Reply to Incoming Emails using Relay.app

## Purpose

The AI model analyzes the content of incoming Gmail messages and classifies them into predefined categories. Based on the classification, the workflow performs different automation actions.

## Prompt 1 – Email Classification

### Objective

Determine the category of the received email.

### Prompt

```
Please classify the attached email as one of the following:
- personal email: if the email looks like personal
- professional email: if the email is professional
- Spam Email: if email looks like spam
- Leave request email: if the person asks for leave
-Linkedin Request: if email is from stephyannsending@gmail.com and asks to write a linkedin post
```

### Input

Email Subject

Email Body

### Expected Output

```
Personal Email
```

---

## Prompt 2 – Conditional Logic

If the AI returns:

```
Personal Email
```

The workflow sends a WhatsApp notification to the user.

---

## Example

### Email

Subject:
Dinner this Saturday?

Body:
Hey! Are you free this Saturday evening? Let's meet for dinner.

### AI Output

```
Personal Email
```

### Workflow Action

✅ Send WhatsApp notification.

### Prompt 3 : Professional email

If the AI returns:

```
You are helpful email drafting assistant to me:
Mt name : Stephy Ann Biju
My role: AI/ML Developer , RAG Developer

Read this email Body

Understand the Email
Write a professional reply to the Email

Output: 
{
Email Subject:
Email Body:
}
```

The workflow sends a mail to the sender.

### Prompt 4 : Spam email

If the AI returns:

```
Spam EMail
```

The workflow sends a mail to the sender.


### Prompt 5 : Leave Request email

If the AI returns:

```
Spam EMail
```

The workflow sends a mail to the sender as 'Please talk to HR dept. .'.


## Notes

- AI is used for semantic understanding rather than keyword matching.
- The workflow can easily be extended with additional categories.
- The prompt is designed to return only the category name, simplifying conditional logic.

---

## Future Improvements

- Add sentiment analysis.
- Detect urgency levels.
- Generate automatic email replies.
- Extract meeting dates and times.
- Support multiple languages.
