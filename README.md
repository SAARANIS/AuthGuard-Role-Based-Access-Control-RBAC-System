# SecureRBAC: Access Control System

A Lightweight, CLI-Based Access Control System in Python
Tired of bulky authentication systems? AccessVault is your minimalist solution for managing users, permissions, and resources—all from the command line. Perfect for small-scale apps or prototyping security layers!

🚀 Why AccessVault?
No databases, no fuss: Stores data in simple files (thanks, pickle!).

Human-friendly commands: Type python auth.py AddUser bob 1234 instead of wrestling with GUIs.

RBAC made simple: Assign users to domains, tag objects with types, and control access like a pro.

Instant checks: CanAccess("delete", "bob", "report.xlsx") gives you a yes/no in seconds.

💻 Quick Start
Add a user:

bash
Copy
python auth.py AddUser alice p@ssw0rd  
Grant permissions:

bash
Copy
python auth.py AddAccess "edit" "admin" "document"  
Check access:

bash
Copy
python auth.py CanAccess "edit" "alice" "budget.xlsx"  
(Output: Success or Error: access denied)

🛠 Features at a Glance
Command	What It Does	Example
AddUser	Registers a new user	AddUser bob 1234
Authenticate	Validates credentials	Authenticate bob 1234
SetDomain	Groups users (e.g., "admin", "guest")	SetDomain bob admin
AddAccess	Defines who can do what (e.g., "edit documents")	AddAccess "view" "guest" "logfile"

This project is strictly for educational purposes and demonstrates cybersecurity principles through ethical white-hat practices. Any unauthorized or malicious use of this code is expressly prohibited. Violators may be subject to legal consequences under applicable cybercrime laws. By using this software, you agree to employ it solely for legitimate security research and learning objectives.
