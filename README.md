# manhattan-inspection-tracker
Work files 
<!DOCTYPE html>
<html>
<head>
    <title>Manhattan Inspection Tracker</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <link rel="stylesheet" href="style.css">

    <link rel="stylesheet" href="https://unpkg.com/leaflet/dist/leaflet.css"/>
</head>

<body>

<div id="header">
    <h1>Manhattan Inspection Tracker</h1>

    <div class="stats">
        🟢 Completed: <span id="completeCount">0</span>
        |
        🟡 Needs Work: <span id="yellowCount">0</span>
        |
        🔴 Remaining: <span id="remainingCount">0</span>
    </div>
</div>


<div id="map"></div>


<div id="menu" class="hidden">

    <h2>Block Status</h2>

    <button onclick="setStatus('green')">
        🟢 Completed
    </button>

    <button onclick="setStatus('yellow')">
        🟡 Needs Work
    </button>

    <button onclick="setStatus('red')">
        🔴 Not Inspected
    </button>

</div>


<script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>

<script src="app.js"></script>

</body>
</html>
style.css
body {
    margin: 0;
    font-family: Arial, sans-serif;
    background: #f5f5f5;
}

#header {
    background: #222;
    color: white;
    padding: 12px;
    text-align: center;
}

#header h1 {
    margin: 0 0 10px 0;
    font-size: 20px;
}

.stats {
    font-size: 14px;
}

#map {
    height: calc(100vh - 120px);
    width: 100%;
}

#menu {
    position: fixed;
    bottom: 20px;
    left: 10%;
    width: 80%;
    background: white;
    padding: 20px;
    border-radius: 12px;
    box-shadow: 0 5px 20px rgba(0,0,0,.3);
    z-index: 1000;
    text-align: center;
}

#menu button {
    display: block;
    width: 100%;
    padding: 12px;
    margin: 8px 0;
    font-size: 16px;
    border-radius: 8px;
    border: none;
}

.hidden {
    display: none;
}
