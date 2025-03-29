# Spidertrap
(Antisyphon training lab from Cyber Deception/Active Defense)
## Spidertrap
- In a terminal, obtain your IP and cd into  ```cd /opt/spidertrap```
- Start spidertrap
<pre>python3 spidertrap.py</pre>
- Visit ```http://{YOUR LINUX IP}:8000```
- This shows random links that lead to more links in an infinite loop, but right now it all looks like gibberish. <br><br>
<img width="500" alt="Screenshot 2025-03-29 at 3 48 15 PM" src="https://github.com/user-attachments/assets/177b977b-ce72-4d86-9a8d-e50cfe95e702" /> <br><br>
## Feeding a directory list
- Let's make this more realistic by adding a directory list. This file contains a large list of common directory names, file names, and paths that web crawlers typically try to access on a website:
<pre>python3 spidertrap.py directory-list-2.3-big.txt</pre>
- Refresh the page <br>
<img src="https://github.com/user-attachments/assets/8d7da576-a6c0-4ed1-aa36-8194aef1012c" width="500" height="auto" /><br><br>
- We're going to mirror the website locally with this command:
<pre>sudo wget -m http://127.0.0.1:8000</pre>
- Spidertrap will start crawling through the mirrored website and make HTTP requests to different paths from the directory list file until it crashes <br><br>
<img src="https://github.com/user-attachments/assets/664dd48c-350f-4123-bc3b-5db997dc7ea1" width="1000" height="auto" />



