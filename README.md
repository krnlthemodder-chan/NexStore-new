<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>NexStore v2 - Dashboard</title>
    
    <link rel="stylesheet" href="https://rsms.me/inter/inter.css">

    <style>
        /* Premium iOS System Color Design Tokens */
        :root {
            --bg-system: #f2f2f7;
            --bg-secondary: #ffffff;
            --text-primary: #000000;
            --text-muted: #8e8e93;
            --nav-blur-bg: rgba(255, 255, 255, 0.75);
            --border-separator: rgba(60, 60, 67, 0.12);
            --overlay-bg: rgba(0, 0, 0, 0.15);
            
            /* Native Apple Accents */
            --ios-blue: #007aff;
            --ios-green: #34c759;
            --ios-purple: #af52de;
            --ios-indigo: #5856d6;
            --ios-orange: #ff9500;
        }

        [data-theme="dark"] {
            --bg-system: #1c1c1e;
            --bg-secondary: #2c2c2e;
            --text-primary: #ffffff;
            --text-muted: #aeaeae;
            --nav-blur-bg: rgba(28, 28, 30, 0.75);
            --border-separator: rgba(84, 84, 88, 0.36);
            --overlay-bg: rgba(0, 0, 0, 0.4);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
            -webkit-tap-highlight-color: transparent;
        }

        body {
            background-color: var(--bg-system);
            color: var(--text-primary);
            transition: background-color 0.4s ease, color 0.4s ease;
            overflow-x: hidden;
            padding-top: 50px;
        }

        /* Translucent iOS Top Bar */
        .ios-navbar {
            position: fixed;
            top: 0;
            width: 100%;
            height: 50px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 16px;
            background-color: var(--nav-blur-bg);
            backdrop-filter: blur(25px);
            -webkit-backdrop-filter: blur(25px);
            border-bottom: 0.5px solid var(--border-separator);
            z-index: 100;
        }

        .nav-title {
            font-weight: 600;
            font-size: 17px;
            letter-spacing: -0.4px;
        }

        .nav-btn {
            background: none;
            border: none;
            color: var(--ios-blue);
            cursor: pointer;
            display: flex;
