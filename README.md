# Focus Oasis: A Micro Productivity Hub
Focus Oasis is a lightweight, single-page web application designed to help you organize daily tasks and manage focus sessions using a custom Pomodoro-style timer. Built purely with semantic HTML5, modern CSS variables, and native vanilla JavaScript, it functions as a modular two-page dashboard without relying on heavy frameworks.

 Features
 Dual-Page Architecture: A smooth, tabbed navbar lets you instantly flip between the productivity Dashboard and your historical Analytics data.

 Configurable Pomodoro Timer: Start, pause, and reset your workflow sessions. Dynamic UI updates show active states with context-aware color switching.

 Interactive Task Manager: Dynamic creation and injection of HTML components (<li>, <span>, <button>) with localized completion event tracking.

 Live Theme Swapping: Switch seamlessly between Light Mode and Dark Mode via dynamic CSS variable manipulation.

 Configuration Pop-up: An overlaid settings modal for setting customized timer limits and configuration options.

 Live Stats Engine: Tracks your completed tasks and focus milestones automatically, reporting live figures to your analytics view.

 Built With
HTML5: Semantic elements (<main>, <nav>, <section>, <header>) for clean layout and accessibility.

CSS3: Custom properties (CSS variables) for immediate theme changes, flexbox arrangements, and keyframe animations (fadeIn, slideIn).

Vanilla JavaScript (ES6+): Centralized state management, real-time DOM manipulation, and contextual event handlers.

 How to Run the Project
Since this entire app is bundled neatly inside a single file, setup takes less than 10 seconds:

Download/Copy the code into a file named index.html (or focus_oasis.html).

Double-click the file to open it directly inside any modern web browser (Chrome, Firefox, Edge, Safari, etc.).

No servers, bundlers, terminal installations, or internet connections are required!

 Code Architecture Highlights
This project serves as an excellent sandbox for understanding fundamental web development concepts:

1. State Management
An appState object acts as the single source of truth for the app, storing session totals, active timer values, and toggle statuses:

JavaScript
let appState = {
    sessionsCompleted: 0,
    tasksCompleted: 0,
    timerMinutes: 25,
    timerSeconds: 0,
    // ...
};
2. Advanced Event Handlers
The project showcases multiple JavaScript event listeners working harmoniously:

click: For button toggles, tab navigation, and modal closures.

change: Listens to settings modifications to adjust internal math algorithms instantly.

keypress: Intercepts the Enter key inside inputs so users can save tasks quickly without using a mouse.

3. Dynamic DOM Manipulation
Rather than simply revealing hidden text, the app creates, styles, and attaches localized events directly onto new HTML elements whenever you write a quest:

JavaScript
const li = document.createElement('li');
const completeBtn = document.createElement('button');
// Event handler is attached safely directly to the new element
completeBtn.addEventListener('click', () => { ... });
📄 License
This project is open-source and free to modify, break, or scale up for your own educational journeys! Enjoy focusing!
