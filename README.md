# Day-2-task---FSWD
JavaScript - Day -2: Datatypes - Task 2 in FSWD

Contents:
   1.HTML Browser view - Debugger, Inspect
   2.Browser js vs Node js
   3.Data types
   4.Copy by value and Copy by reference
   5.Window & document object

1.HTML Browser view - Debugger, Inspect :- in Microsoft(I'm using)
  Step1 - Open the webpage on the edge to inspect.
  Step2 - Right click or ctrl+shift+I on the respective web page and choose the inspection option.
  Step3 - After clicking on the inspection option, A slidebar will appear that contains all the necessary options to inspect, edit & debug HTML and CSS with the Elements tools.


2.Browser js vs Node js :-
   a)Difference in Environment
   b)User Interface
   c)Different in their usage
   d)Architecture difference

      a) Difference in Environment
         •	Browser executes JavaScript within the Host Environment, on the client side. Browsers provide a Document Object Model (DOM) which represents the structure of web pages.	
         •	Node.js provides a runtime environment that allows JavaScript to run on a server, outside the browser. Also, it does not have a DOM like web browsers.
         
      b) User Interface
         •	Browser in Browsers Host environment execute JavaScript and render the HTML, CSS, and JavaScript and also provide a graphical user interface (GUI) to interact with web pages, since users interact with the web pages so it is essential to use GUI.	
         •	Node.js uses a command line interface (CLI) because it has no interaction with the users and it is used for server-side development to build web servers and APIs.

      c) Different in their Usage
         •	Browser is used for the Client-side and executes JavaScript inside the browser’s Host environment and here developers use JavaScript to make the web Content dynamic.
         •	Node.js which is a runtime environment for the execution of JavaScript is used for server-side development to create web servers and APIs so JavaScript is most used for logic-building and algorithmic parts here.
         
      d) Architecture Difference
         •	Browsers are used for browsing web content, its architecture is much more complex than the node.js architecture, and it has a JavaScript engine inside a rendering engine that executes the JavaScript within the client-side environment.	
         •	Node.js runtime architecture consists of a V8 engine, event-driven I/O, Libuv library, and C++ addons and JavaScript Modules which will provide an amazing runtime environment for JavaScript execution.
         

3.Data types :-
  ^ In computer programming, JavaScript provides different data types to hold different types of values.
  ^ JavaScript has two categories in which data types are segregated as,
    1) Primitive Data Type :- 
        ^ Primitive data are only single values and have no special capabilities. 
        ^ Two types of primitive data type are as a) Numeric and 
                                                  b) Non-Numeric Data types.
            a) Numeric Type :- 
                ^ Numeric data type refers to data expressed in numbers.
                ^ It is always collected in number form and can store both integers and decimal values with high precision.
                ^ Two types are as i) Integer 
                                  ii) Floating point
                  i) Integer :-
                      ^ Integer Data Type can stores whole numbers without decimals.
                      ^ Four types are as i} Byte
                                         ii} Short
                                        iii} Int
                                         iv} Long
                        i} Byte :- 
                            ^ The byte data type is an 8-bit signed two’s complement integer.
                            ^ 1 byte = 8 bits
                       ii} Short :-
                            ^ The short data type is a 16-bit signed two’s complement integer.
                            ^ 2 bytes = 16 bits
                      iii} Int :-
                            ^ Int data type is a 32-bit signed two’s complement integer.
                            ^ 4 bytes = 32 bits
                       iv} Long :- 
                            ^ Long data type is a 64-bit signed two’s complement integer.
                            ^ 8 bytes = 64 bits
                  ii) Floating point :-
                       i} Float :- 
                           ^ The float data type is a single-precision 32-bit IEEE 754 floating-point.
                           ^ 4 bytes = 32 bits
                      ii} Double :-
                           ^ The double data type is a double-precision 64-bit IEEE 754 floating-point. 
                           ^ 8 bytes = 64 bits
           b) Non-Numeric Type :-
               ^ Non-Numeric data type refers to data not expressed in numbers.
               ^ Two types of Non-Numeric data types are as i) Boolean 
                                                           ii) Char
               i) Boolean :- 
                   ^ The boolean data type represents a logical value that can be either true or false.
               ii) Char(Character) :- 
                   ^ The char data type is a single 16-bit Unicode character with the size of 2 bytes (16 bits).
     2) Non-Primitive Data Type :-
         ^ Non-Primitive (Reference) Data types are used to store multiple values and can call methods to perform certain operations
         ^ Five types of Non-primitive data types are as a) String
                                                         b) Class
                                                         c) Object
                                                         d) Interface
                                                         e) Array
                                                         f) Function
            a) String :-
                 ^ Strings are defined as an array of characters.
            b) Class :-
                 ^ A Class is a user-defined blueprint or prototype from which objects are created. 
                 ^ Five types of class are as i) Modifiers
                                             ii) Class Name
                                            iii) Superclass (if any)
                                             iv) Interfaces (if any)
                                              v) Body
            C) Object :-
                 ^ An Object is a basic unit of Object-Oriented Programming and represents real-life entities.
                 ^ Three types of Object Data types are as i) State
                                                          ii) Behavior
                                                         iii) Identity
            d) Interface:- 
                 ^ Like a class, an interface can have methods and variables, but the methods declared in an interface are by default abstract (only method signature, no body).
            e) Array:- 
                 ^ An Array is a group of like-typed variables that are referred to by a common name. 
                 ^ Arrays in Java work differently than they do in C/C++. 
            f) Function :-
                 ^ A block of code designed to perform a particular task.

 4.Copy by value and Copy by reference.
 
   Copy by value :-
    ^ In this type, the value is copy to many variables.
    ^ For example :-
       - Person A has a red shirt.
       - Person B buying same red shirt as Person A.
       - If Person B has damage in the shirt, Person A has no damage.
       - Because they have separate shirt, so damage will not occur.
    ^ By coding..
        Input :-
          let num = 10
          let temp = num
          console.log(num,temp)
          num = 20
          console.log(num,temp)
        output :- (10,10)
          (20,10)
        - So this Copy by value.

   Copy by reference :-
    ^ In this type, the value is copied according to the refernce.
    ^ For example :-
       - Person A has a red shirt in Locker box.
       - Person B asking the shirt of Person A,
       - Person A giving permission to Person B to wear the shirt.
       - In this case, both are use the same shirt when they need.
       - If Person B is made damage in the shirt,
       - so same shirt is kept in the locker room.
       - And Person A used same shirt, the damage is occur.
       - So here the value is shirt, reference is locker room.
       - This is copy by reference.
    ^ By coding..
        Input :-
           Let num = [10,20,30,40]
           let temp = num
           console.log(num,temp)
           num.push(50)
           console.log(num,temp)
         Output :-
           [10,20,30,40],[10,20,30,40]
           [10,20,30,40,50],[10,20,30,40,50]
        - So this copy by refernce [].

 5. Window & document object :-
    1. Window object in JavaScript :-
         A) Definition :-
              ^ The Window object in JavaScript represents the browser window that contains a Document Object Model (DOM) document.
              ^ It is a global object that provides various properties and methods to interact with the browser environment, manipulate the document, handle events, manage timers, display dialog boxes, and more.
            
         B) Key Properties of the Window Object as
              a) window.document :-
                   ^ Refers to the Document object representing the HTML document shown in the window.
              b) window.console :-
                   ^ Returns the window’s Console object.
              c) window.location :-
                   ^ Provides information about the current URL.
              d) window.innerHeight and window.innerWidth :-
                   ^ Describe the height and width of the browser window's content area, excluding toolbars and scrollbars.
              e) window.localStorage :-
                   ^ Allows storing key/value pairs in a web browser with no expiration date.
              f) window.sessionStorage :-
                   ^ Similar to localStorage but stores data for one session only.
              g) window.history :-
                   ^ Retrieves the window’s History object.
              h) window.navigator :-
                   ^ Represents the browser and its capabilities
       
         C) Common Methods of the Window Object :-
              a) window.alert() :-
                   ^ Displays an alert message to the user.
              b) window.confirm() :-
                   ^ Displays a confirm message to the user and waits for their response.
              c) window.prompt() :-
                   ^ Displays a prompt message to the user and waits for their input.
              d) window.open() :-
                   ^ Opens a new browser window or tab.
              e) window.close() :-
                   ^ Closes the current window or tab.
              f) window.setInterval() :-
                   ^ Calls a function or evaluates an expression at specified intervals (in milliseconds).
              g) window.setTimeout() :-
                   ^ Calls a function or evaluates an expression after a specified number of milliseconds.
       
          D) Conclusion :-
              ^ The Window object in JavaScript is essential for interacting with the browser window or frame.
              ^ It offers numerous properties like innerHeight, innerWidth, and screen, as well as methods like alert(), confirm(), and open(), enabling developers to control and manipulate the window and document effectively.
  
    2. Document object in JavaScript :-
         A) Definitions :-
             ^ The document object in JavaScript represents the web page loaded in the browser and serves as an entry point into the web page's content, which is the DOM (Document Object Model) tree.
             ^ The DOM tree includes elements such as <body> and <table>, among many others.
             ^ It provides functionality globally to the document, like how to obtain the page's URL and create new elements in the document.
       
         B) Key Properties and Methods :-
              a) Finding HTML Elements :-
                  # The document object provides several methods to find HTML elements :-
                       ^ document.getElementById(id): Finds an element by its ID.
                       ^ document.getElementsByTagName(name): Finds elements by their tag name.
                       ^ document.getElementsByClassName(name): Finds elements by their class name. 
              b) Changing HTML Elements :-
                  # You can change HTML elements using properties and methods of the document object :-
                       ^ element.innerHTML = new HTML content: Changes the inner HTML of an element.
                       ^ element.setAttribute(attribute, value): Changes the attribute value of an HTML element.
              c) Adding and Deleting Elements :-
                  # The document object allows you to create, remove, and manipulate HTML elements :-
                       ^ document.createElement(element) :-
                            ~ Creates an HTML element.
                       ^ document.removeChild(element) :-
                            ~ Removes an HTML element.
                       ^ document.appendChild(element) :-
                            ~ Adds an HTML element.
                       ^ document.replaceChild(new, old) :-
                            ~ Replaces an HTML element.
               d) Writing to the Document :-
                   # You can write directly to the HTML output stream using :-
                       ^ document.write(text) :-
                            ~ Writes text in a document.
                       ^ document.writeln(text) :-
                            ~ Writes a line of text in a document.
               e) Event Handling :-
                    # The document object also supports adding event handlers :-
                       ^ document.getElementById(id).onclick = function() { code } :-
                            ~ Adds an event handler to an element's onclick event.
       
          C) Conclusion :-
               ^ The document object is a powerful tool in JavaScript for interacting with and manipulating the content of a web page.
               ^ It provides a wide range of methods and properties to access, modify, and interact with HTML elements, making it essential for dynamic web development.


          




     
   
  
