# FOIL-DOH
Open-source system for generating high-precision, compliance-aligned FOIL requests to NYS agencies—optimized to reduce denials and increase meaningful disclosure
FOIL-DOH: Precision Civic Transparency Engine

FOIL-DOH is an open-source civic-tech toolkit designed to generate, submit, and track Freedom of Information Law (FOIL) requests specifically optimized for the New York State Department of Health (health.ny.gov).

Government transparency shouldn't require a law degree. This system uses natural language processing and statutory state-machine tracking to help citizens draft requests that are legally sound, narrowly tailored, and highly likely to be fulfilled.

🎯 Core Principles

• Precision over Volume: We do not spam agencies. The engine forces users to narrow their scope to reasonably described records to respect the time of Records Access Officers and reduce denial rates.

• Compliance-First: Built around NYS Public Officers Law, Article 6.

• Accountability: Automated tracking of the 5-day acknowledgment and 20-day fulfillment statutory deadlines.

🚀 MVP Features (Phase 1)

• [x] FOIL Intelligence Engine: Translates plain English into legally structured requests.

• [x] DOH Templates: Pre-configured routing for NYS DOH capital projects and Certificate of Need (CON) data.

• [x] Export: Generates portal-ready text or email payloads.

• [x] Local Tracking: SQLite/JSON backed state machine for deadline monitoring.

🛠️ Installation & Setup

1. Clone the repository:

[bash]
git clone [https://github.com/SignalArchitectDM/FOIL-DOH.git](https://github.com/SignalArchitectDM/FOIL-DOH.git)
cd FOIL-DOH


2. Create a virtual environment and install dependencies:

[bash]
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
pip install -r requirements.txt


3. Set your environment variables (create a .env file):

[env]
LLM_API_KEY=your_key_here
DATABASE_URL=sqlite:///./foil_tracker.db


4. Run the API:

[bash]
uvicorn api.main:app --reload


⚖️ Ethical Usage & Rate Limiting

This tool is strictly for targeted, legitimate civic inquiry.

• Anti-Spam: The system enforces rate-limiting on generation.

• No Harassment: Requests targeting specific lower-level state employees by name for non-administrative records are flagged and rejected by the engine.

📝 Disclaimer

This repository is a technological tool, not a law firm. The creators and contributors are not your attorneys. Use of this software does not constitute legal advice.
