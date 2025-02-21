/**
 * @name Nexus Evolution
 * @description A smooth, Discord theme with futuristic elements 2024
 * @author CrimZenEdits
 * @version 1.2.2
 * @invite jQeKgHmjhu
 */

/* IMPORTANT: make sure to enable dark mode in Discord settings for the theme to apply properly!!! */
@import url('https://pastebin.com/raw/5Kdukqpj');
@import url('https://pastebin.com/raw/z6rRbCqJ');
/* Customize things here */
:root {
    /*settings modal root*/
    --themelightsettingsmodalbackground: rgb(223, 223, 223);
    --themedarksettingsmodalbackground: rgb(51, 49, 53);
    --settingsmodalwidth: 960px;
    --settingsmodalheight: 80vh;
    --streaming-indicator: hsl(260, 60%, 60%); /* change to #593695 for default purple */

    /* COLOURS */
    --main-color: #2780e6;
    --hover-color: #1f66b8;
    --channel-color: #ccffff;
    --dnd-indicator: hsl(0, 91%, 41%);

    /* MISC */
    --background-brightness: 87%;
    --emoji-size: 50px;

    /* 3D Text Shadow */
    --text-shadow: 1px 1px 0 rgba(0, 0, 0, 0.3), 
                   2px 2px 0 rgba(0, 0, 0, 0.2), 
                   3px 3px 0 rgba(0, 0, 0, 0.1);

    .popout-menu .popout-menu-item:hover {
        background: rgba(123, 0, 255, 0.8) !important;
        color: #fff !important;
    }

    body {
        font-family: 'Bitter', serif;
        -webkit-font-smoothing: antialiased;
        text-rendering: optimizeLegibility;
        text-size-adjust: 100%;
    }

    /* Font */
    --font: 'Roboto', sans-serif;

    --corner-text: '᲼᲼᲼ v1.2.1᲼᲼᲼᲼᲼᲼᲼᲼᲼᲼ NEXUS Evolution';

    /* Accent colors */
    --accent-1: hsl(190, 70%, 55%);
    --accent-2: hsl(190, 70%, 45%);
    --accent-3: hsl(190, 74%, 38%);
    --accent-4: hsl(189, 81%, 37%);
    --accent-5: hsl(190, 70%, 15%);
    --mention-bg: hsl(190, 70%, 90%);
    --mention-text: hsl(190, 70%, 15%);

    /* Text colors */
    --text-color: #e9e9e9; /* Set a base text color */
    --text-0: var(--text-color);
    --text-1: var(--text-color);
    --text-2: hsl(220, 25%, 85%);
    --text-3: hsl(220, 15%, 75%);
    --text-4: hsl(220, 15%, 55%);
    --text-5: hsl(220, 15%, 45%);

    /* Background and dark colors */
    --bg-1: hsl(220, 15%, 25%);
    --bg-2: hsl(220, 15%, 20%);
    --hover: hsla(230, 20%, 50%, 0.15); /* Slightly increase the hover background opacity */
    --active: hsla(220, 20%, 50%, 0.3); /* Increase the active background opacity */
    --message-hover: hsla(220, 0%, 0%, 0.1);

    /* Spacing and padding */
    --spacing: 12px;

    /* Animations */
    --list-item-transition: 0.4s ease; /* Slowed down the list item transitions */
    --unread-bar-transition: 0.4s ease; /* Slowed down the unread bar transitions */
    --Nexus-spin-transition: 0.4s ease;
    --icon-spin-transition: 1s ease;
    --dropdown-transition: 0.4s ease; /* Slowed down the dropdown transitions */

    /* Shadow improvements */
    --shadow-default: 0 8px 30px rgba(0, 0, 0, 0.5); /* Deeper shadow for elements */
    --shadow-hover: 0 12px 40px rgba(0, 0, 0, 0.6); /* Deeper shadow on hover */

    /* Corner roundness */
    --roundness-l: 20px; /* Consistent roundness */
    --roundness-m: 16px; /* Consistent roundness */
    --roundness-s: 12px; /* Consistent roundness */
    --roundness-xs: 10px; /* Consistent roundness */
    --roundness-xxs: 8px; /* Consistent roundness */

    /* Icons */
    --discord-icon: none;
    --Nexus-icon: block;
    --Nexus-icon-url: url('https://i.postimg.cc/P5v8L9VB/Mvw-C1-Gq2-Tl-SFh-WNvi-SXgw-Q-033710.jpg');
    --Nexus-icon-size: 80px;

    /* Filters for uncolorable elements */
    --green-to-accent-3-filter: hue-rotate(56deg) saturate(1.43);
    --blurple-to-accent-3-filter: hue-rotate(304deg) saturate(0.84) brightness(1.2);
}

/* Dropdown styles */
#theme-options {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background: linear-gradient(145deg, rgba(25, 25, 25, 0.95), rgba(40, 40, 40, 0.85)); /* Gradient background for dropdown */
    border-radius: var(--roundness-m);
    padding: 20px;
    box-shadow: var(--shadow-default); /* Applied default shadow */
    z-index: 9999;
    display: none;
    color: var(--text-0);
    transition: all var(--dropdown-transition);
    width: 320px;
    backdrop-filter: blur(12px); /* Increased blur for more depth */
}

/* Heading and paragraph styles */
#theme-options h2 {
    margin: 0;
    font-size: 24px;
    color: var(--main-color);
    text-shadow: var(--text-shadow); /* Apply 3D shadow to heading */
}

#theme-options p {
    margin: 8px 0;
    font-size: 14px;
    text-shadow: var(--text-shadow); /* Apply 3D shadow to paragraphs */
}

/* Toggle button styles */
#toggle-options {
    position: fixed;
    top: 20px;
    right: 20px;
    cursor: pointer;
    color: var(--main-color);
    text-align: center;
    padding: 10px 15px;
    border: 2px solid var(--main-color);
    border-radius: var(--roundness-s);
    background-color: rgba(0, 0, 0, 0.7); /* Darkened background for toggle */
    box-shadow: var(--shadow-default); /* Applied default shadow */
    transition: background-color 0.4s ease, color 0.4s ease, box-shadow 0.4s ease; /* Smoother transitions */
    z-index: 10000;
    text-shadow: var(--text-shadow); /* Apply 3D shadow to the toggle button */
}

#toggle-options:hover {
    background-color: var(--hover-color);
    color: #fff;
    box-shadow: var(--shadow-hover); /* Apply hover shadow */
}

/* Show dropdown on theme load */
#theme-options.show {
    display: block;
}

/* Additional Info Section */
#theme-additional-info {
    margin-top: 12px;
    font-size: 12px;
    color: var(--text-1);
    text-shadow: var(--text-shadow); /* Apply 3D shadow */
}

/* Additional settings dropdown styles */
#settings-options {
    margin-top: 10px;
    color: var(--text-1);
    font-size: 14px;
}

#settings-options h3 {
    color: var(--main-color);
    margin-bottom: 5px;
    text-shadow: var(--text-shadow); /* Apply 3D shadow to settings heading */
}

#settings-options input[type="color"] {
    margin-right: 5px;
    border: none;
    border-radius: var(--roundness-xs);
    cursor: pointer;
}

/* New dropdown for Keyboard Shortcuts */
#shortcuts-options {
    margin-top: 10px;
    color: var(--text-1);
}

#shortcuts-options h3 {
    color: var(--main-color);
    margin-bottom: 5px;
    text-shadow: var(--text-shadow); /* Apply 3D shadow to shortcuts heading */
}

#shortcuts-options p {
    margin: 0;
    font-size: 12px;
    text-shadow: var(--text-shadow); /* Apply 3D shadow to shortcuts paragraph */
}

/* Specific input styles */
input {
    border: 1px solid var(--text-4);
    border-radius: var(--roundness-xs); /* Keeping the same roundness */
    background: var(--bg-2);
    color: var(--text-1);
    padding: 8px;
    text-shadow: var(--text-shadow); /* Apply 3D shadow to input text */
}

/* Adjusted colors for specific elements */
.select {
    background: var(--bg-2);
    color: var(--text-1);
    border-radius: var(--roundness-xs); /* Keeping the same roundness */
    text-shadow: var(--text-shadow); /* Apply 3D shadow to select text */
}

.select:hover {
    background: var(--hover-color);
    color: var(--text-0);
}

/* Scrolling element styling */
::-webkit-scrollbar {
    width: 8px;
}

::-webkit-scrollbar-track {
    background: var(--bg-1);
}

::-webkit-scrollbar-thumb {
    background: var(--main-color);
    border-radius: var(--roundness-xs); /* Keeping the same roundness */
}

::-webkit-scrollbar-thumb:hover {
    background: var(--hover-color);
}

/* Important styles for the overall interface */
body, .app, .chat, .channel, .navbar, .message, .user-card, .popover, .popout-menu, .tooltip {
    background: var(--bg-1) !important;
    color: var(--text-0) !important;
}

input, select, textarea {
    border: 1px solid var(--text-4);
    background: var(--bg-2);
    color: var(--text-1);
    border-radius: var(--roundness-xs); /* Keeping the same roundness */
    text-shadow: var(--text-shadow); /* Apply 3D shadow to input, select, and textarea text */
}

input:focus, select:focus, textarea:focus {
    border-color: var(--main-color);
}

/* Update the hover and active styles */
a:hover {
    color: var(--hover-color);
    text-decoration: underline;
}

/* Keep text on the user menu hover */
.user-menu {
    transition: all var(--list-item-transition);
}

/* Adjusted color for the user menu */
.user-menu-item {
    color: var(--text-0) !important;
    border-radius: var(--roundness-xs); /* Keeping the same roundness */
    text-shadow: var(--text-shadow); /* Apply 3D shadow to user menu text */
}

.user-menu-item:hover {
    background: var(--hover);
}

/* Adjusted color for the messages */
.message {
    background: var(--bg-2);
    border-radius: var(--roundness-m); /* Keeping the same roundness */
    margin-bottom: var(--spacing);
    transition: background-color var(--list-item-transition);
    text-shadow: var(--text-shadow); /* Apply 3D shadow to message text */
}

.message:hover {
    background: var(--message-hover);
}

/* Misc styles for links */
a {
    color: var(--main-color);
    text-shadow: var(--text-shadow); /* Apply 3D shadow to links */
}

a:hover {
    color: var(--hover-color);
}

/* Global styles for buttons */
button {
    background: var(--main-color);
    color: #fff;
    border: none;
    border-radius: var(--roundness-s); /* Keeping the same roundness */
    padding: 10px 15px;
    cursor: pointer;
    transition: background-color 0.3s ease, transform 0.2s ease, box-shadow 0.4s ease; /* Added box-shadow to transitions */
    text-shadow: var(--text-shadow); /* Apply 3D shadow to button text */
    font-weight: bold; /* Bold text for more impact */
    font-size: 16px; /* Slightly larger font size for prominence */
}

button:hover {
    background: var(--hover-color);
    box-shadow: 0 0 10px var(--main-color), 0 0 25px var(--main-color); /* Glowing effect */
}

/* Add styling for tooltips */
.tooltip {
    background: rgba(0, 0, 0, 0.8);
    color: #fff;
    border-radius: var(--roundness-xs); /* Keeping the same roundness */
    text-shadow: var(--text-shadow); /* Apply 3D shadow to tooltip text */
}

/* Adjust the transitions for smoother effects */
.channel {
    transition: background-color var(--list-item-transition), color var(--list-item-transition);
}

.channel:hover {
    background: var(--hover);
}

/* Add other general styles */
h1, h2, h3, h4, h5, h6 {
    color: var(--text-1);
    text-shadow: var(--text-shadow); /* Apply 3D shadow to all headings */
}

blockquote {
    border-left: 4px solid var(--main-color);
    padding-left: 10px;
    color: var(--text-3);
    font-style: italic;
    text-shadow: var(--text-shadow); /* Apply 3D shadow to blockquote text */
}

.theme-dark .sidebar_a4d4d9 .content_eed6a8:after {
    content: 'Theme Author: CrimZenEdits   discord.gg/5RVMJGQwQR';
    font-size: 13px;
    color: rgba(255, 255, 255, 0.062);
    text-align: center;
    text-shadow: var(--text-shadow); /* Apply 3D shadow to the author text */
    margin-top: 50px;
    height: 340px;
    display: flex; /* Use flexbox for centering */
    justify-content: center; /* Center horizontally */
    align-items: center; /* Center vertically */
    flex-direction: column; /* Stack items vertically */
}
