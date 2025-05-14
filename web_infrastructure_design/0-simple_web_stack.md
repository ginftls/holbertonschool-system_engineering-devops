Task 0: Simple Web Stack - Whiteboard Exercise
This a comprehensive whiteboard diagram and explanation for a simple web stack infrastructure. 

<svg viewBox="0 0 800 600" xmlns="http://www.w3.org/2000/svg">
  <!-- Title -->
  <text x="400" y="30" text-anchor="middle" font-size="24" font-weight="bold">Simple Web Stack - www.foobar.com</text>
  
  <!-- User Computer -->
  <rect x="30" y="80" width="120" height="80" fill="#E3F2FD" stroke="#2196F3" stroke-width="2" rx="5"/>
  <text x="90" y="105" text-anchor="middle" font-size="14" font-weight="bold">User</text>
  <text x="90" y="125" text-anchor="middle" font-size="12">Computer</text>
  <text x="90" y="145" text-anchor="middle" font-size="12">Browser</text>
  
  <!-- Internet Cloud -->
  <ellipse cx="300" cy="120" rx="80" ry="50" fill="#F5F5F5" stroke="#757575" stroke-width="2"/>
  <text x="300" y="110" text-anchor="middle" font-size="14" font-weight="bold">Internet</text>
  <text x="300" y="130" text-anchor="middle" font-size="12">HTTP/HTTPS</text>
  <text x="300" y="150" text-anchor="middle" font-size="12">(TCP/IP)</text>
  
  <!-- Domain Name -->
  <rect x="450" y="50" width="140" height="60" fill="#F0F4F8" stroke="#4A5568" stroke-width="2" rx="5"/>
  <text x="520" y="75" text-anchor="middle" font-size="12" font-weight="bold">Domain Name</text>
  <text x="520" y="95" text-anchor="middle" font-size="11">foobar.com</text>
  
  <!-- DNS Record -->
  <rect x="630" y="60" width="120" height="40" fill="#E8F5E9" stroke="#4CAF50" stroke-width="2" rx="5"/>
  <text x="690" y="80" text-anchor="middle" font-size="12" font-weight="bold">DNS Record</text>
  <text x="690" y="95" text-anchor="middle" font-size="11">www → 8.8.8.8</text>
  
  <!-- Server Box -->
  <rect x="380" y="200" width="280" height="320" fill="#FFF3E0" stroke="#F57C00" stroke-width="3" rx="10"/>
  <text x="520" y="225" text-anchor="middle" font-size="16" font-weight="bold">Single Server</text>
  <text x="520" y="245" text-anchor="middle" font-size="14">(IP: 8.8.8.8)</text>
  
  <!-- Web Server -->
  <rect x="410" y="270" width="220" height="50" fill="#E1F5FE" stroke="#0288D1" stroke-width="2" rx="5"/>
  <text x="520" y="290" text-anchor="middle" font-size="14" font-weight="bold">Web Server</text>
  <text x="520" y="308" text-anchor="middle" font-size="12">(Nginx)</text>
  
  <!-- Application Server -->
  <rect x="410" y="340" width="220" height="50" fill="#F3E5F5" stroke="#7B1FA2" stroke-width="2" rx="5"/>
  <text x="520" y="360" text-anchor="middle" font-size="14" font-weight="bold">Application Server</text>
  <text x="520" y="378" text-anchor="middle" font-size="12">(Node.js, Python, PHP, etc.)</text>
  
  <!-- Application Files -->
  <rect x="410" y="410" width="105" height="50" fill="#FFF9C4" stroke="#F9A825" stroke-width="2" rx="5"/>
  <text x="462" y="430" text-anchor="middle" font-size="12" font-weight="bold">Application</text>
  <text x="462" y="448" text-anchor="middle" font-size="11">Files/Code</text>
  
  <!-- Database -->
  <rect x="525" y="410" width="105" height="50" fill="#FFEBEE" stroke="#C62828" stroke-width="2" rx="5"/>
  <text x="577" y="430" text-anchor="middle" font-size="12" font-weight="bold">Database</text>
  <text x="577" y="448" text-anchor="middle" font-size="11">(MySQL)</text>
  
  <!-- Arrows -->
  <defs>
    <marker id="arrowhead" markerWidth="10" markerHeight="10" refX="9" refY="3" orient="auto" markerUnits="strokeWidth">
      <polygon points="0 0, 10 3, 0 6" fill="#424242"/>
    </marker>
  </defs>
  
  <!-- User to Internet -->
  <line x1="150" y1="120" x2="220" y2="120" stroke="#424242" stroke-width="2" marker-end="url(#arrowhead)"/>
  <text x="185" y="110" text-anchor="middle" font-size="11">Request</text>
  
  <!-- Internet to Domain -->
  <line x1="380" y1="120" x2="450" y2="80" stroke="#424242" stroke-width="2" marker-end="url(#arrowhead)"/>
  <text x="415" y="95" text-anchor="middle" font-size="11">Domain Query</text>
  
  <!-- Domain to DNS -->
  <line x1="590" y1="80" x2="630" y2="80" stroke="#424242" stroke-width="2" marker-end="url(#arrowhead)"/>
  
  <!-- Internet to Server -->
  <line x1="340" y1="155" x2="500" y2="200" stroke="#424242" stroke-width="2" marker-end="url(#arrowhead)"/>
  <text x="420" y="175" text-anchor="middle" font-size="11">HTTP Request</text>
  
  <!-- Internal Server Flow -->
  <!-- Web to App -->
  <line x1="520" y1="320" x2="520" y2="340" stroke="#616161" stroke-width="2" marker-end="url(#arrowhead)"/>
  
  <!-- App to Files -->
  <line x1="490" y1="390" x2="475" y2="410" stroke="#616161" stroke-width="2" marker-end="url(#arrowhead)"/>
  
  <!-- App to DB -->
  <line x1="550" y1="390" x2="565" y2="410" stroke="#616161" stroke-width="2" marker-end="url(#arrowhead)"/>
  
  <!-- Issues Section -->
  <rect x="30" y="280" width="300" height="200" fill="#FFEBEE" stroke="#D32F2F" stroke-width="2" rx="5"/>
  <text x="180" y="305" text-anchor="middle" font-size="16" font-weight="bold" fill="#D32F2F">Infrastructure Issues</text>
  
  <text x="40" y="330" font-size="14" font-weight="bold" fill="#D32F2F">SPOF (Single Point of Failure):</text>
  <text x="40" y="350" font-size="12">• Entire server is a single point</text>
  <text x="40" y="368" font-size="12">• No redundancy or failover</text>
  
  <text x="40" y="395" font-size="14" font-weight="bold" fill="#D32F2F">Maintenance Downtime:</text>
  <text x="40" y="415" font-size="12">• Server restart required for updates</text>
  <text x="40" y="433" font-size="12">• Website unavailable during maintenance</text>
  
  <text x="40" y="460" font-size="14" font-weight="bold" fill="#D32F2F">Scalability Issues:</text>
  <text x="40" y="478" font-size="12">• Cannot handle traffic spikes</text>
  
  <!-- Labels for explanations -->
  <text x="30" y="550" font-size="14" font-weight="bold">Key Components:</text>
  <text x="30" y="570" font-size="12">1. Server: Physical/virtual machine hosting all services</text>
  <text x="30" y="588" font-size="12">2. Domain: Human-readable address mapping to IP</text>
  <text x="400" y="570" font-size="12">3. Web Server: Handles HTTP requests/responses</text>
  <text x="400" y="588" font-size="12">4. App Server: Executes business logic</text>
</svg>



Whiteboard Explanation - Simple Web Stack
User Access Flow:

User types www.foobar.com in their browser
DNS Resolution: Browser queries DNS to resolve www.foobar.com to IP address 8.8.8.8
HTTP Request: Browser sends HTTP/HTTPS request over the internet to server at 8.8.8.8
Web Server (Nginx): Receives the request and forwards it to the application server
Application Server: Processes the request, executes business logic
Database/Files Access: Application retrieves data from MySQL database and/or application files
Response Generation: Application generates HTML/JSON response
Response Delivery: Response travels back through web server → internet → user's browser

Component Definitions:
1. What is a server?

A physical or virtual computer that provides services to other computers
In this case, it hosts all the components needed to serve the website
Has its own IP address (8.8.8.8)

2. Role of the domain name (foobar.com)

Human-readable address that maps to the server's IP address
Easier to remember than numerical IP addresses
Provides a consistent access point even if server IP changes

3. DNS Record Type - www

"www" is a subdomain configured with an A record
A record (Address record) maps the hostname to IPv4 address
Points www.foobar.com → 8.8.8.8

4. Role of the web server (Nginx)

Handles incoming HTTP/HTTPS requests
Serves static content (images, CSS, JavaScript)
Acts as reverse proxy to application server
Manages SSL/TLS encryption
Load balancing (in more complex setups)

5. Role of the application server

Executes dynamic application logic
Processes business rules
Handles user sessions
Generates dynamic content
Communicates with database

6. Role of the database (MySQL)

Persistent data storage
Structured data management
Query processing
Data integrity and transactions
User data, content, configurations

7. Server-User Communication

Uses HTTP/HTTPS protocol
Built on top of TCP/IP
Port 80 for HTTP, Port 443 for HTTPS
Request-response model

Infrastructure Issues:
1. SPOF (Single Point of Failure)

Everything runs on one server
If server fails, entire website is down
No redundancy for any component
Single network connection

2. Maintenance Downtime

Deploying new code requires server restart
System updates need downtime
No way to perform maintenance without affecting users
Database maintenance affects entire system

3. Scalability Limitations

Cannot handle traffic spikes
Limited by single server resources (CPU, RAM, bandwidth)
No horizontal scaling capability
Database becomes bottleneck with increased load