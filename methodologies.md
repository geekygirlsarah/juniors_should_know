State
  - Advice: "Never break links."
    - Lesson: "If you changed the URL for a page, always re-direct the old URL to the new one."
    - URL Redirection
      - TODO
  - Advice: "Keep URLs Meaningful."
    - Lesson: "Use pushState to change URL in Rich web apps. Your users should be able to copy an URL from their browser and be able to share it with their friends."
      - pushState
          - TODO
  - Advice: "Avoid hashbangs!".
    - hashbang
        - TODO

Sessions
  - Cookies
      - TODO (What are cookies?)
      - Advice: "Cookies are not for storage. Your cookies shouldn't be larger than 4096 bytes."
      - Security
        - HttpOnly = true
        - Secure = true
        - TODO (Aditional cookies security).
  - LocalStorage
    - TODO (What is LocalStorage?)
    - Advice: "Use it."

Security
  - OWASP TOP 10
    - https://www.owasp.org/index.php/Category:OWASP_Top_Ten_Project
    - List of Top 10 current security vulnerabilities
  - XSS
    - Cross Site Scripting: being tricked into executing external Javascript
    - can lead to an attacker being able to do anything a victim can do through their browser
    - OWASP XSS Prevention Cheatsheat: https://www.owasp.org/index.php/XSS_%28Cross_Site_Scripting%29_Prevention_Cheat_Sheet
  - Cross Site Request Forgery
      - Victim has an active session and has been authenticated on another web site, such as a bank website
      - Victim visits another website and is tricked into submitting an HTTP request to the valid website
      - Victim thinks they are submitting a form to enter a contest, but are actually submitting a form to transfer all their money to China
      - Can be prevented with input validation, specifically by using Regex
      - OWASP CSRF Prevention Cheatsheat: https://www.owasp.org/index.php/Cross-Site_Request_Forgery_%28CSRF%29_Prevention_Cheat_Sheet
  - SQL Injections
    - When user input goes directly into a database query, attackers can make malicious queries
    - Attacker inputs a SQL query into a form
    - Can be used to query the database for all user passwords or drop database tables
    - Do not trust user input
    - Prevention: Avoid dynamic DB queries or use Stored Procedures (developer defines query, users only supply the parameters)
    - OWASP SQL Injection Prevention: https://www.owasp.org/index.php/SQL_Injection_Prevention_Cheat_Sheet
  - Other Types of Injection
    - Command Injection: User-supplied input is passed to the system shell, allowing attacker to execute commands
    - Code Injection: Attacker executes code in the application without accessing the shell
    - Prevention: input validation
    - Advice: "eval() is evil."
    - OWASP Command Injection Prevention: https://www.owasp.org/index.php/Command_Injection
  - Insecure Direct Object Reference
    - Developer exposes access to an internal implementation object, such as a file, directory or database key
    - Developer intends user to have access to a harmles file: www.example.com/images/my_image
    - Attacker can reach sensitive files by climbing up the directory: www.example.com/images/../../../my_secret.key
    - OWASP Insecure Direct Object References: https://www.owasp.org/index.php/Top_10_2013-A4-Insecure_Direct_Object_References
  - See The OWASP Top 10 List for Other Common Vulnerabilities
  - Authentication
    - Identification
      - User states who they are
      - User can claim to be someone they are not
      - ex. Entering your name or username
    - Authentication
      - Computer validates user identity
      - ex. entering a password, showing a Drivers License
    - Authorization
      - Determining what a person is allowed to do in a system
      - Assumes user has already been identified and authenticated
      - Advice: "Don't do Authority via Identity" i.e. Everyone can edit cookies.
    - Identification vs. Authentication vs. Authorization: https://danielmiessler.com/blog/security-identification-authentication-and-authorization/
  - Salting and hashing passwords
    - Salting: Adding randomness to your encryption so that an attacker cannot reverse-engineer the passwords on your site
    - Without salting, an attacker can try a common password with different encryption methods until one works: he now knows your encyption method
    - When the attacker knows your encryption method, he can decrypt everyone's password
    - Hashing: Using an algorithm, a password is converted to a long sequence of numbers and letters
    - Example hash: 8743b52063cd84097a65d1633f5c74f5
    - Advice: "Use bcrypt."

Debugging and Testing
  - Advice: "Don't be superstitious."
    - Lesson: TODO
  - Advice: "Be Explorative."
    - Lesson: "Use your language's Read Eval Print Loop (console) to test out everything you don't quite understand."
  - Error Messages
    - Advice: "'Oops!' is not an error message"
  - Source Maps
    - TODO

Coding Antipatterns
  - Globals
    - Advice: TODO
  - God Objects
    - Advice: TODO
  - Giant Function Signatures
    - Advice: TODO
  - Variable Names
    - Advice: "You're not charged by the character."
      - Lesson: "Most editors have autocomplete. A long explicit variable name is better than a short, confusing one."
  - Advice: "Stop being clever."
    - Lesson: "You're coding for the next programmer that's going to read your code 2 years later when you're out in vacactions. Using obscure patterns and hard to read, yet clever, code requires a much higher investment of time to understand."
  - Advice: "Be Boring."
    - Lesson: "Use what works. Don't re-invent the wheel. Not everything is special."

Code Readability
  - Advice: "Pretend the person that's going to read your code 6 months from now has your address and a gun."
    - Lesson: "Before commiting, try to read your code from scratch and see if it's readable enough for the next person to understand. Change structure when necessary, try to eliminate confusion (or code line hopping) by being extra explicit. Your coding style shouldn't be unique and representative of yourself, but something understood and consumeable by everyone."

Tips
  - Javascript
    - Advice: "Who cares if it is tabs or spaces"
  - Git
    - Advice: "Know the ins and out of Git. Don't be afraid of rebasing"
    - Git Rebase
      - TODO
    - Git Merge Conflicts
      - TODO
  - Deployment
    - Automate Deployment
      - TODO
  - Architecture Patterns
    - MVC
      - TODO
    - MVP
      - TODO
    - SOA
      - TODO
    - Event-driven
      - TODO
    - P2P
      - TODO