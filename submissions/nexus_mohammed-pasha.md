---

# Nexus

---

## Attendee/Team Details

**Name:** Mohammed Pasha
**GitHub Username:** Pasha2308
**LinkedIn Profile:** https://www.linkedin.com/in/mohammed-pasha
**GitHub Project Repository:** https://github.com/Pasha2308/Nexus

---

## Problem Statement Selected

Track B - Build an Application

---

## Project Description

Nexus is a Founder's Network & Context Engine. It acts as a Personal CRM and long-term memory layer for LLMs. Founders can quickly input meeting notes, which Nexus parses and stores. When chatting with the AI, the app automatically injects the founder's profile and relevant network connections into the context, eliminating the need to repeatedly prompt the LLM and preventing "LLM amnesia".

* What is the project about? A smart, personalized CRM and Chat interface.
* Who is it for? Founders and operators managing complex networks.
* What problem does it solve? Losing track of valuable connections and having to manually pass context to LLMs.
* How does it help the user? By automatically leveraging past context, the AI can draft perfectly tailored outreach or recall network details seamlessly.

---

## Approach

* **Understanding the problem:** I noticed I was constantly explaining my business and network to LLMs for drafting emails or brainstorming. 
* **User flow:** The user inputs a "Brain Dump" (e.g., "Met Alex, does marketing"). The app stores it. When querying the AI later ("Who do I know in marketing?"), it uses the stored context automatically.
* **AI usage:** Breeth AI powers the intelligence, extracting structured data from messy notes and answering user queries.
* **Valkey:** Used as a highly efficient Context Manager & Semantic Cache (using Hashes and Lists) to store session history, profiles, and connection metadata.

---

## Tech Stack and Tools Used

**Frontend:** React, Next.js, Tailwind CSS
**Backend:** Next.js API Routes, Node.js
**Database:** Valkey (Context & Memory Cache)
**AI Tools/API:** Breeth AI
**Cloud/Deployment:** Google Cloud Platform (Cloud Run, Memorystore for Valkey migration later)
**Other Tools:** Docker

---

## Key Features

1. Instant Brain Dump Parser (extracts CRM data from raw notes).
2. "Zero-Prompt" Context Injection (LLM automatically knows who you are and who you know).
3. Network Graph & Connection Tracker.

---

## What is Working?

The foundational architecture is set up, defining the Context injection pipeline using Valkey for caching and Next.js for the UI.

---

## What is Still in Progress?

Integrating the live Breeth AI endpoints and finalizing the React dashboard UI.

---

## Screenshots or Demo

**Deployed Link:** TBD
**Demo Video Link:** TBD
**Screenshots:** TBD

---

## Challenges Faced

Structuring the dynamic context window efficiently using Valkey's Hashes and Lists to ensure the LLM gets the most relevant memory without overflowing the token limit.

---

## Learnings

Gaining deep experience using Valkey as an ultra-fast semantic memory store rather than just a simple cache, and mastering Next.js API routes for edge AI streaming.

---

## Future Improvements

Implementing true Valkey Vector Search to semantically search through thousands of network connections, and migrating the entire stack to Google Cloud Platform for scale.

---

## Final Note

Nexus aims to be the ultimate second brain for busy founders, built specifically to leverage the speed of Valkey and the intelligence of Breeth AI.
