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
