# Share-It-
Share it is social media like threads. The idea of Share it is to share your opinion with others. People can like your post, comment on your post, like other peoples comments. You can send friend requests to others and accept friend requests. You can chat with your friends wiht live connection. When someone does something on your post you get notification about it. You can change your profile settings. You can see peoples profile and you can see all of their posts there. Overall share it acts as small normal social media.
Project architecture - 
The app is divided into modules. Each module is lazy loaded and each module corresponds to different page. The modules(pages) are chat, friends, general, notifications, profile and shared. The navigation module is not lazy loaded. All of the modules keep components and functionalities which are mandatory for the page of the module. Each module has one component which is an wrapper and other components which are used inside the wrapper. There are 3 services, one for user requests, one for post requests and one for authentications. The api is kept inside the environment-vars.ts file. All of the interfaces are kept inside the interface folder from which almost all components get their interfaces for vars. The shared module holds the post UI and its comment UI which is used in multiple places and because of that it accepts many variables as states and results from functions. The chat page uses websocket (Subject) which fires when the page is open. There is also an authguard file which guards for unauthorized access. Guests of the site can access the / page and they can login or register, Registered users can access everything except login and register. The registered users can do all of the CRUD operaions.
