--How the Web works--

    1-What is HTTP?

        -HTTP (Hypertext Transfer Protocol) is basically the system that makes websites work. When you type a web address into your browser and hit Enter, your browser sends a message (called a request) to the website's server asking for the page. That message uses HTTP.
        It works on what's called the Application Layer, which is just a fancy way of saying it's one of the top layers in how data travels across networks — kind of like the final layer where everything gets wrapped up and sent to you
        
        
        - The difference between HTTP and HTTPS?
            HTTPS is basically HTTP, but secure. The extra S stands for Secure.
            The key difference: HTTPS uses encryption (TLS/SSL) to protect the data that travels between your browser and the website. This means:(Your data is encrypted — not sent in plain text)


        -Status Codes:HTTP status codes are short 3-digit numbers that tell you what happened when your browser tried to reach a website. They basically let you know if things went well or if there was a problem.
        These codes are grouped into 5 main categories:
        1xx – Just letting you know something is happening (informational).
        2xx – Everything is good! (success).
        3xx – The page moved somewhere else (redirection).
        4xx – You made a mistake (like typing the wrong address).
        5xx – The website/server has a problem.

    Examples:
        200:This means everything good(success).Your browser asked for a page, and the server gave it back successfully.
        404:This means You made a mistake .Your browser asked for something, but the server couldn’t find it. Maybe the link is broken, or you typed the URL wrong
        500:This means the problem is on the website’s side/server has a problem not yours.The server tried to load the page but something broke inside (maybe a bug or crash).

    -------------------------

    2- what is the DNS?

        The Domain Name System (DNS) is like the Internet’s phonebook.
        When you want to visit a website, you type something easy like www.google.com.
        But your computer doesn’t understand names- it understands IP addresses (like 192.168.1.1 (in IPv4)).So DNS helps by translating the domain name into the correct IP address, so your browser knows where to go.

        -why we need DNS?
            When you want to visit a website, you type an easy name like: www.google.com.But computers don’t understand names-they understand IP addresses like: 192.168.1.1.That’s where DNS comes in.DNS takes the name you typed and translates it into the correct IP address, so your browser knows exactly where to go and can open the right website for you.

        -How the DNS work?
        Here's what happens when you type a domain in the browser:

            1. You type "www.google.com" and hit Enter.
            2. Your browser asks the DNS Resolver (usually provided by your internet provider): “Do you know this domain?”
            3. If the Resolver has it in cache, it returns the IP immediately.
            4. If not, it asks:
            - Root Server "Ask the .com TLD server"
            - TLD Server "Ask the Authoritative server for google.com"
            - Authoritative Server "Here’s the IP: '192.168.1.1'"
            5. Resolver sends the IP back to the browser.
            6. Browser uses the IP to talk to the website’s server and load the page.

        -Domain vs IP Address
            This is the name you type in your browser, like: youtube.com
            It's made for humans easy to read and remember instead of memorizing long numbers
            IP Address:This is a unique number for each website or server, like:
            192.168.10.1 Computers use these numbers to find and connect to the correct website behind the scenes.

        -Example
            What happens when you type www.google.com in your browser?
            You type www.google.com and hit Enter.
            Your browser asks: "DNS, what’s the IP address for google.com?"
            The DNS starts searching:It asks the Root Server which says: “Go ask the .com server.”Then it asks the TLD Server for .com  which says: “Ask the server responsible for google.com.”
            Then it asks the Authoritative Server → which replies with an IP address, like 192.168.10.1.
            The browser takes that IP address and connects to Google.
            The Google server responds with the webpage.
            Your browser shows the page in front of you 

    --------------------------

    3-What happens when you type a URL in the browser?
        1. You type the link:You open your browser and type something like www.google.com and hit Enter
        2. DNS Resolution Finding the IP
        Your browser asks: "DNS, what’s the IP address for google.com?"
        The DNS starts searching:It asks the Root Server which says: “Go ask the .com server.”Then it asks the TLD Server for .com which says: “Ask the server responsible for google.com.”Then it asks the Authoritative Server which replies with an IP address, like 192.168.10.1.
        3. Sending the HTTP Request
        Now the browser knows where to go. It sends a message (HTTP request) to the Google server like
        4. Getting the Response
        The server receives the request, prepares the data,and sends it back.
        5. Rendering the Page
        Your browser takes that data and starts building the page visually(text, images, buttons) everything you see.

    -------------------------------
    4. Frontend vs Backend
        In web development, the terms frontend and backend are essential for understanding how websites and web applications work.

        -Frontend The User Interface (UI):This is the part of a website or app that users directly interact with. So, anything you see on the screen is part of the frontend, like:(The page layout ,Colors ,Buttons, Images, Menus, Animations and effects)The main goal of frontend development is to make the user experience smooth, attractive, and easy to use.

        -Backend The Behind the Scenes Part:This is the part of a website or app that runs in the background you don’t see it, but it powers everything that happens on the site:(It works with databases, Handles user requests, Stores and retrieves data, Manages security and data protection, Takes care of login/logout, file uploads, and more)


        -Frontend Frameworks: (HTML, CSS, JavaScript ,React, Angular, Vue.js, Tailwind CSS,Bootstrap)

        -Backend Frameworks:(Node.js, Django (Python),Laravel (PHP),Express.js (JavaScript), Spring Boot (Java) ,Ruby on Rails (Ruby))

    --------------------------------

        5-Web Servers vs Browsers
            The Web Browser and Web Server are two essential components of the World Wide Web that work together to deliver web pages to users.

            - Web Browser : A web browser is the software we use to access the internet and browse websites — like Google Chrome or Firefox and Edge.

            - Web Server : A web server is a computer (or software) that stores websites and delivers them over the internet. It’s the one that sends the web pages to you when you request them. 

            -How does each one work?

                -Web Browser:The user types a website link (like: www.google.com).The browser sends an HTTP request to the server saying: “Give me this page.”
                Once the server replies, the browser takes the data and displays it nicely with text, images, buttons, videos, and more.

                -Web Server: It’s always ready to receive requests from browsers.When a request comes in, it checks which page or file is being asked for.Then it sends the correct file back to the browser so the user can see it.

    -------------------------------

    6-Client vs Server

        -Client : A Client is a device or a software that the user uses to request services from a server like : (Web browsers (like Google Chrome, Firefox),Mobile application).The user interacts with the client to ask for something like opening a webpage, logging in and then the client sends that request to the server.

        -Server : A Server is a computer or a program that works in the background. It receives requests from clients, processes them, and then sends back the needed data.like: Web Server , Database Server.

        - Who Sends the Request and Who Responds?
            client: sends the request 
            Server: responds to the request

        - What runs on the user's device (Client side)?
            The Frontend(user interface),The Browser or App directly
        - What runs on the server?
            Processing requests, Databases , Website files , Operations like login, data analysis, and sending responses

    ----------------------------------

    7-What is an API (Application Programming Interface)?
        An API is like a messenger that allows two different software programs to talk to each other. You can also define it as  is a set of rules that allow different software applications to communicate with each other.

        -How are APIs used in the Web?
            On the web, APIs help connect the frontend (what you see) with the backend (the server and data).
        -What is JSON?
            JSON stands for JavaScript Object Notation. It's a simple format used by APIs to send and receive data.JSON is easy to read and write, and it's used by most web APIs because it's lightweight and fast.

        -Example:
           -How a Weather Website Uses an API
            You open a weather website and type "Cairo".
            The site sends a request to a weather API.
            The API responds with JSON data.
            The website takes that data and shows it to you 

    ---------------------------------

    8-Request Methods (GET vs POST)
        When a browser or an app wants to talk to a server to send or receive data, it uses something called HTTP request methods. Two of the most common ones are: GET and POST.

        -What's the difference between (GET vs POST)?
            -GET: is a method we use when we want to request data from the server without changing anything.
            It's a fast and simple method, but it’s not secure for sensitive data, because the information is sent in the URL, and anyone can see it.

            -POST:This method is used when we want to send data to the server — for example, when you log in, fill out a form, or upload a file.
            POST is more secure than GET because the data is sent inside the body of the request and not shown in the URL.

        -When to use each one?
            -Use GET When you just want to read or fetch data from the server.
            
            -Use POST When you need to send data or do something that changes data on the server (like saving, updating, or logging in).

