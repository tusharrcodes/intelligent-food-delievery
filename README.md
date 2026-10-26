# Intelligent Food Delivery Agent

You can view the live, working website here:
https://tusharrcodes.github.io/intelligent-food-delivery/

This repository contains the core HTML code for the intelligent food delivery agent I built:

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Intelligent Food Delivery Agent</title>

<style>
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: Arial, Helvetica, sans-serif;
    background: #f3f7fb;
    color: #172033;
}

/* HEADER */

header {
    background: linear-gradient(135deg, #172554, #2563eb);
    color: white;
    padding: 30px 6%;
    text-align: center;
}

header h1 {
    font-size: 32px;
    margin-bottom: 8px;
}

header p {
    color: #dbeafe;
}


/* NAVIGATION */

nav {
    background: #0f172a;
    padding: 12px 6%;
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
}

nav button {
    background: transparent;
    color: white;
    border: 1px solid #475569;
    padding: 10px 16px;
    border-radius: 7px;
    cursor: pointer;
}

nav button:hover {
    background: #2563eb;
}


/* CONTAINER */

.container {
    width: 92%;
    max-width: 1200px;
    margin: 25px auto;
}


/* SECTIONS */

.section {
    display: none;
}

.section.active {
    display: block;
}


/* CARDS */

.cards {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 15px;
}

.card {
    background: white;
    border-radius: 14px;
    padding: 22px;
    margin-bottom: 20px;
    box-shadow: 0 5px 18px rgba(0,0,0,0.08);
}

.stat-card {
    border-top: 5px solid #2563eb;
}

.stat-title {
    color: #64748b;
    font-size: 14px;
}

.stat-value {
    font-size: 27px;
    font-weight: bold;
    margin-top: 8px;
}


/* HEADINGS */

h2 {
    margin-bottom: 15px;
    color: #172554;
}


/* FORM */

.form-grid {
    display: grid;
    grid-template-columns: repeat(2,1fr);
    gap: 15px;
}

label {
    display: block;
    font-weight: bold;
    margin-bottom: 6px;
}

input,
select {
    width: 100%;
    padding: 11px;
    border: 1px solid #cbd5e1;
    border-radius: 8px;
    font-size: 15px;
}


/* BUTTONS */

button {
    border: none;
    padding: 11px 17px;
    border-radius: 8px;
    cursor: pointer;
    font-weight: bold;
}

.primary {
    background: #2563eb;
    color: white;
}

.green {
    background: #16a34a;
    color: white;
}

.orange {
    background: #f59e0b;
    color: white;
}

.red {
    background: #dc2626;
    color: white;
}

button:hover {
    opacity: 0.9;
}


/* TABLE */

table {
    width: 100%;
    border-collapse: collapse;
}

th,
td {
    padding: 11px;
    border-bottom: 1px solid #e2e8f0;
    text-align: center;
}

th {
    background: #eff6ff;
    color: #172554;
}


/* PRIORITY TAGS */

.tag {
    display: inline-block;
    padding: 5px 9px;
    border-radius: 20px;
    font-size: 12px;
    font-weight: bold;
}

.low {
    background: #dcfce7;
    color: #166534;
}

.normal {
    background: #fef3c7;
    color: #92400e;
}

.high {
    background: #ffedd5;
    color: #9a3412;
}

.emergency {
    background: #fee2e2;
    color: #991b1b;
}


/* CAMPUS MAP */

.map {
    position: relative;
    height: 430px;
    background: #eaf3fb;
    border: 2px solid #bfdbfe;
    border-radius: 15px;
    overflow: hidden;
}

.road-h {
    position: absolute;
    height: 9px;
    background: #cbd5e1;
    border-radius: 10px;
}

.road-v {
    position: absolute;
    width: 9px;
    background: #cbd5e1;
    border-radius: 10px;
}

.location {
    position: absolute;
    width: 135px;
    text-align: center;
    padding: 12px;
    background: white;
    border: 3px solid #475569;
    border-radius: 12px;
    font-weight: bold;
    z-index: 5;
}

.location small {
    display: block;
    color: #64748b;
    font-weight: normal;
    margin-top: 4px;
}

.active-location {
    border-color: #16a34a !important;
    box-shadow: 0 0 15px rgba(22,163,74,.45);
}


/* AI RESULT */

.result {
    margin-top: 18px;
    padding: 20px;
    background: #0f172a;
    color: white;
    border-radius: 12px;
    line-height: 1.8;
}

.result-title {
    color: #60a5fa;
    font-size: 19px;
    margin-bottom: 8px;
}

.success-text {
    color: #4ade80;
    font-weight: bold;
}


/* ALGORITHMS */

.algorithm-grid {
    display: grid;
    grid-template-columns: repeat(3,1fr);
    gap: 15px;
}

.algorithm {
    padding: 20px;
    border-radius: 12px;
    background: #f8fafc;
    border: 2px solid #cbd5e1;
}

.bfs {
    border-color: #22c55e;
}

.dfs {
    border-color: #f59e0b;
}

.astar {
    border-color: #2563eb;
}


/* WORKFLOW */

.flow {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 10px;
    flex-wrap: wrap;
}

.flow-box {
    flex: 1;
    min-width: 140px;
    padding: 18px;
    border-radius: 10px;
    background: #eff6ff;
    border: 2px solid #60a5fa;
    text-align: center;
    font-weight: bold;
}

.arrow {
    font-size: 25px;
    color: #16a34a;
}


/* FOOTER */

footer {
    margin-top: 30px;
    padding: 25px;
    background: #0f172a;
    color: white;
    text-align: center;
}


/* MOBILE */

@media(max-width:850px) {

    .cards,
    .form-grid,
    .algorithm-grid {
        grid-template-columns: 1fr;
    }

    .flow {
        flex-direction: column;
    }

    .arrow {
        transform: rotate(90deg);
    }
}
</style>
</head>

<body>


<header>

    <h1>🤖 Intelligent Food Delivery Agent</h1>

    <p>
        B.Tech CSE Project | Intelligent Agents • BFS • DFS • A* • Optimization
    </p>

</header>


<nav>

    <button onclick="showSection('dashboard')">
        Dashboard
    </button>

    <button onclick="showSection('orders')">
        Orders
    </button>

    <button onclick="showSection('mapSection')">
        Campus Map
    </button>

    <button onclick="showSection('algorithms')">
        AI Algorithms
    </button>

    <button onclick="showSection('about')">
        About Project
    </button>

</nav>


<div class="container">


<!-- ================= DASHBOARD ================= -->

<section id="dashboard" class="section active">


    <div class="cards">


        <div class="card stat-card">

            <div class="stat-title">
                🔋 Battery
            </div>

            <div class="stat-value" id="battery">
                100%
            </div>

        </div>


        <div class="card stat-card">

            <div class="stat-title">
                📦 Robot Capacity
            </div>

            <div class="stat-value" id="capacity">
                5 / 5
            </div>

        </div>


        <div class="card stat-card">

            <div class="stat-title">
                📍 Robot Location
            </div>

            <div class="stat-value" id="robotLocation">
                Cafeteria
            </div>

        </div>


        <div class="card stat-card">

            <div class="stat-title">
                📋 Pending Orders
            </div>

            <div class="stat-value" id="pendingCount">
                0
            </div>

        </div>

    </div>


    <!-- ORDER FORM -->

    <div class="card">

        <h2>🍔 Customer Order Management</h2>


        <div class="form-grid">


            <div>

                <label>
                    Student / Department
                </label>

                <input
                    id="customer"
                    placeholder="Enter name"
                >

            </div>


            <div>

                <label>
                    Food Item
                </label>

                <select id="food">

                    <option>Burger</option>
                    <option>Pizza</option>
                    <option>Sandwich</option>
                    <option>Thali</option>
                    <option>Cold Drink</option>

                </select>

            </div>


            <div>

                <label>
                    Quantity
                </label>

                <input
                    id="quantity"
                    type="number"
                    value="1"
                    min="1"
                >

            </div>


            <div>

                <label>
                    Delivery Location
                </label>

                <select id="location">

                    <option>Library</option>
                    <option>CSE</option>
                    <option>Hostel</option>
                    <option>Sports</option>

                </select>

            </div>


            <div>

                <label>
                    Order Priority
                </label>

                <select id="priority">

                    <option value="1">
                        Low
                    </option>

                    <option value="2">
                        Normal
                    </option>

                    <option value="3">
                        High
                    </option>

                    <option value="4">
                        Emergency
                    </option>

                </select>

            </div>

        </div>


        <br>


        <button
            class="primary"
            onclick="addOrder()">

            ➕ Add Order

        </button>

    </div>


    <!-- AI AGENT -->

    <div class="card">

        <h2>
            🧠 Intelligent Agent
        </h2>

        <p>
            The agent selects an order according to
            priority, route cost, battery and carrying capacity.
        </p>


        <br>


        <button
            class="green"
            onclick="runAgent()">

            🤖 Run Intelligent Agent

        </button>


        <button
            class="orange"
            onclick="compareAlgorithms()">

            🔎 Compare BFS / DFS / A*

        </button>


        <button
            class="red"
            onclick="resetRobot()">

            🔄 Reset Robot

        </button>


        <div
            class="result"
            id="result">

            <div class="result-title">
                AI Result
            </div>

            Waiting for an order...

        </div>

    </div>

</section>


<!-- ================= ORDERS ================= -->

<section
    id="orders"
    class="section">

    <div class="card">

        <h2>
            📋 Order Management
        </h2>


        <table>

            <thead>

                <tr>

                    <th>ID</th>
                    <th>Customer</th>
                    <th>Food</th>
                    <th>Qty</th>
                    <th>Location</th>
                    <th>Priority</th>
                    <th>Status</th>

                </tr>

            </thead>


            <tbody id="orderTable"></tbody>

        </table>

    </div>

</section>


<!-- ================= MAP ================= -->

<section
    id="mapSection"
    class="section">


    <div class="card">

        <h2>
            🗺️ Campus Map
        </h2>

        <p>
            Campus locations are represented as graph nodes
            and roads represent graph edges.
        </p>


        <br>


        <div class="map">


            <div
                class="road-h"
                style="
                    left:10%;
                    top:52%;
                    width:80%;
                ">
            </div>


            <div
                class="road-h"
                style="
                    left:25%;
                    top:27%;
                    width:55%;
                ">
            </div>


            <div
                class="road-v"
                style="
                    left:51%;
                    top:15%;
                    height:65%;
                ">
            </div>


            <div
                class="road-v"
                style="
                    left:22%;
                    top:50%;
                    height:35%;
                ">
            </div>


            <div
                class="location"
                id="locCafeteria"
                style="
                    left:2%;
                    top:45%;
                ">

                🍔 Cafeteria

                <small>
                    Robot Start
                </small>

            </div>


            <div
                class="location"
                id="locGate"
                style="
                    left:43%;
                    top:45%;
                ">

                🚪 Main Gate

            </div>


            <div
                class="location"
                id="locLibrary"
                style="
                    left:43%;
                    top:7%;
                ">

                📚 Library

            </div>


            <div
                class="location"
                id="locCSE"
                style="
                    left:70%;
                    top:45%;
                ">

                💻 CSE

            </div>


            <div
                class="location"
                id="locHostel"
                style="
                    left:2%;
                    top:80%;
                ">

                🏠 Hostel

            </div>


            <div
                class="location"
                id="locSports"
                style="
                    left:66%;
                    top:80%;
                ">

                ⚽ Sports

            </div>

        </div>

    </div>

</section>


<!-- ================= ALGORITHMS ================= -->

<section
    id="algorithms"
    class="section">


    <div class="card">

        <h2>
            🔍 AI Algorithm Comparison
        </h2>


        <div class="algorithm-grid">


            <div class="algorithm bfs">

                <h3>
                    🟢 BFS
                </h3>

                <p>
                    Breadth First Search explores
                    nodes level by level.
                </p>

                <br>

                <b>
                    Used for:
                </b>

                Shortest path in unweighted graphs.

            </div>


            <div class="algorithm dfs">

                <h3>
                    🟠 DFS
                </h3>

                <p>
                    Depth First Search explores
                    one path deeply before backtracking.
                </p>

                <br>

                <b>
                    Used for:
                </b>

                Graph exploration.

            </div>


            <div class="algorithm astar">

                <h3>
                    🔵 A*
                </h3>

                <p>
                    A* combines actual cost
                    and heuristic cost.
                </p>

                <br>

                <b>
                    Formula:
                </b>

                f(n) = g(n) + h(n)

            </div>

        </div>


        <br>


        <button
            class="primary"
            onclick="compareAlgorithms()">

            Run Comparison

        </button>


        <div
            class="result"
            id="algorithmResult">

            Click Run Comparison.

        </div>

    </div>

</section>


<!-- ================= ABOUT ================= -->

<section
    id="about"
    class="section">


    <div class="card">

        <h2>
            📚 About the Project
        </h2>


        <h3>
            Objective
        </h3>

        <p>
            To create an autonomous agent that delivers
            food from the campus cafeteria to students
            or departments.
        </p>


        <br>


        <h3>
            AI Concepts
        </h3>

        <ul
            style="
                line-height:2;
                margin-left:20px;
            ">

            <li>
                Intelligent Agents
            </li>

            <li>
                Graph Search
            </li>

            <li>
                BFS and DFS
            </li>

            <li>
                A* Search
            </li>

            <li>
                Priority-Based Planning
            </li>

            <li>
                Optimization
            </li>

            <li>
                Battery and Capacity Constraints
            </li>

        </ul>

    </div>


    <div class="card">

        <h2>
            ⚙️ System Workflow
        </h2>


        <div class="flow">


            <div class="flow-box">

                ORDER

                <br>

                <small>
                    Customer request
                </small>

            </div>


            <div class="arrow">
                →
            </div>


            <div class="flow-box">

                PRIORITY

                <br>

                <small>
                    Classify order
                </small>

            </div>


            <div class="arrow">
                →
            </div>


            <div class="flow-box">

                ROUTE

                <br>

                <small>
                    BFS / DFS / A*
                </small>

            </div>


            <div class="arrow">
                →
            </div>


            <div class="flow-box">

                CHECK

                <br>

                <small>
                    Battery + Capacity
                </small>

            </div>


            <div class="arrow">
                →
            </div>


            <div class="flow-box">

                DELIVERY

                <br>

                <small>
                    Update robot
                </small>

            </div>

        </div>

    </div>

</section>


</div>


<footer>

    B.Tech CSE Project |
    Intelligent Food Delivery Agent

</footer>


<script>

/* ================= DATA ================= */

let orders = [];

let nextOrderId = 101;

let battery = 100;

let capacity = 5;

let robotLocation = "Cafeteria";


/* ================= ROUTES ================= */

const routeInfo = {

    Library: {

        bfs: [
            "Cafeteria",
            "Gate",
            "Library"
        ],

        dfs: [
            "Cafeteria",
            "Hostel",
            "Sports",
            "Library"
        ],

        astar: [
            "Cafeteria",
            "Gate",
            "Library"
        ],

        cost: 5
    },


    CSE: {

        bfs: [
            "Cafeteria",
            "Gate",
            "CSE"
        ],

        dfs: [
            "Cafeteria",
            "Hostel",
            "Sports",
            "Library",
            "CSE"
        ],

        astar: [
            "Cafeteria",
            "Gate",
            "CSE"
        ],

        cost: 6
    },


    Hostel: {

        bfs: [
            "Cafeteria",
            "Hostel"
        ],

        dfs: [
            "Cafeteria",
            "Hostel"
        ],

        astar: [
            "Cafeteria",
            "Hostel"
        ],

        cost: 4
    },


    Sports: {

        bfs: [
            "Cafeteria",
            "Hostel",
            "Sports"
        ],

        dfs: [
            "Cafeteria",
            "Hostel",
            "Sports"
        ],

        astar: [
            "Cafeteria",
            "Hostel",
            "Sports"
        ],

        cost: 6
    }

};


/* ================= ADD ORDER ================= */

function addOrder() {

    let customer =
        document.getElementById(
            "customer"
        ).value.trim();


    let food =
        document.getElementById(
            "food"
        ).value;


    let quantity =
        Number(
            document.getElementById(
                "quantity"
            ).value
        );


    let location =
        document.getElementById(
            "location"
        ).value;


    let priority =
        Number(
            document.getElementById(
                "priority"
            ).value
        );


    if(customer === "") {

        alert(
            "Please enter student name."
        );

        return;
    }


    if(quantity <= 0) {

        alert(
            "Quantity must be greater than zero."
        );

        return;
    }


    orders.push({

        id: nextOrderId++,

        customer: customer,

        food: food,

        quantity: quantity,

        location: location,

        priority: priority,

        status: "Pending"

    });


    document.getElementById(
        "customer"
    ).value = "";


    displayOrders();

    updatePendingCount();


    showResult(
        "✅ Order added successfully."
    );

}


/* ================= DISPLAY ORDERS ================= */

function displayOrders() {

    let table =
        document.getElementById(
            "orderTable"
        );


    if(orders.length === 0) {

        table.innerHTML = `
            <tr>
                <td colspan="7">
                    No orders yet.
                </td>
            </tr>
        `;

        return;
    }


    table.innerHTML = "";


    orders.forEach(order => {

        let name =
            getPriorityName(
                order.priority
            );


        let className =
            getPriorityClass(
                order.priority
            );


        table.innerHTML += `

            <tr>

                <td>
                    #${order.id}
                </td>

                <td>
                    ${order.customer}
                </td>

                <td>
                    ${order.food}
                </td>

                <td>
                    ${order.quantity}
                </td>

                <td>
                    ${order.location}
                </td>

                <td>

                    <span
                        class="tag ${className}">

                        ${name}

                    </span>

                </td>

                <td>
                    ${order.status}
                </td>

            </tr>

        `;

    });

}


/* ================= PRIORITY ================= */

function getPriorityName(priority) {

    if(priority === 4)
        return "Emergency";

    if(priority === 3)
        return "High";

    if(priority === 2)
        return "Normal";

    return "Low";

}


function getPriorityClass(priority) {

    if(priority === 4)
        return "emergency";

    if(priority === 3)
        return "high";

    if(priority === 2)
        return "normal";

    return "low";

}


/* ================= RUN AGENT ================= */

function runAgent() {

    let pending =
        orders.filter(
            order =>
                order.status === "Pending"
        );


    if(pending.length === 0) {

        alert(
            "No pending orders."
        );

        return;
    }


    pending.sort(
        (a,b) => {

            if(
                b.priority !==
                a.priority
            ) {

                return (
                    b.priority -
                    a.priority
                );

            }


            return (
                routeInfo[a.location].cost -
                routeInfo[b.location].cost
            );

        }
    );


    let selected =
        pending[0];


    let route =
        routeInfo[
            selected.location
        ];


    let batteryNeeded =
        route.cost * 5;


    if(
        selected.quantity >
        capacity
    ) {

        showResult(

            "❌ Delivery blocked.<br>" +

            "Robot capacity: " +
            capacity +

            "<br>Required: " +
            selected.quantity

        );

        return;
    }


    if(
        batteryNeeded >
        battery
    ) {

        showResult(

            "❌ Delivery blocked.<br>" +

            "Battery available: " +
            battery +
            "%" +

            "<br>Required: " +
            batteryNeeded +
            "%"

        );

        return;
    }


    battery -=
        batteryNeeded;


    capacity -=
        selected.quantity;


    robotLocation =
        selected.location;


    selected.status =
        "Delivered";


    document.getElementById(
        "battery"
    ).innerText =
        battery + "%";


    document.getElementById(
        "capacity"
    ).innerText =
        capacity + " / 5";


    document.getElementById(
        "robotLocation"
    ).innerText =
        robotLocation;


    displayOrders();

    updatePendingCount();

    highlightRoute(
        route.astar
    );


    showResult(

        `<div class="result-title">
            🤖 Intelligent Agent Decision
        </div>

        <b>Selected Order:</b>
        #${selected.id}

        <br>

        <b>Priority:</b>
        ${getPriorityName(
            selected.priority
        )}

        <br>

        <b>Destination:</b>
        ${selected.location}

        <br>

        <b>A* Route:</b>
        ${route.astar.join(" → ")}

        <br>

        <b>Distance:</b>
        ${route.cost} units

        <br>

        <b>Battery Used:</b>
        ${batteryNeeded}%

        <br><br>

        <span class="success-text">
            ✅ Order Delivered Successfully!
        </span>

        <br>

        Battery Remaining:
        ${battery}%

        <br>

        Capacity Remaining:
        ${capacity}/5`

    );

}


/* ================= COMPARE ================= */

function compareAlgorithms() {

    let pending =
        orders.find(
            order =>
                order.status === "Pending"
        );


    if(!pending) {

        alert(
            "Place an order first."
        );

        return;
    }


    let route =
        routeInfo[
            pending.location
        ];


    document.getElementById(
        "algorithmResult"
    ).innerHTML = `

        <div class="result-title">
            🔎 Algorithm Comparison
        </div>

        <b>Destination:</b>
        ${pending.location}

        <br><br>

        <b>BFS:</b>
        ${route.bfs.join(" → ")}

        <br><br>

        <b>DFS:</b>
        ${route.dfs.join(" → ")}

        <br><br>

        <b>A*:</b>
        ${route.astar.join(" → ")}

        <br><br>

        <b>A* Cost:</b>
        ${route.cost} units

        <br><br>

        <span class="success-text">
            ⭐ A* selected as the least-cost route.
        </span>
    `;


    highlightRoute(
        route.astar
    );

}


/* ================= RESULT ================= */

function showResult(message) {

    document.getElementById(
        "result"
    ).innerHTML =
        message;

}


/* ================= PENDING COUNT ================= */

function updatePendingCount() {

    let count =
        orders.filter(
            order =>
                order.status === "Pending"
        ).length;


    document.getElementById(
        "pendingCount"
    ).innerText =
        count;

}


/* ================= HIGHLIGHT ROUTE ================= */

function highlightRoute(path) {

    let mapping = {

        Cafeteria:
            "locCafeteria",

        Gate:
            "locGate",

        Library:
            "locLibrary",

        CSE:
            "locCSE",

        Hostel:
            "locHostel",

        Sports:
            "locSports"

    };


    document
        .querySelectorAll(
            ".location"
        )
        .forEach(
            element =>
                element.classList.remove(
                    "active-location"
                )
        );


    path.forEach(
        location => {

            let element =
                document.getElementById(
                    mapping[location]
                );


            if(element) {

                element.classList.add(
                    "active-location"
                );

            }

        }
    );

}


/* ================= RESET ================= */

function resetRobot() {

    battery = 100;

    capacity = 5;

    robotLocation =
        "Cafeteria";


    orders.forEach(
        order =>
            order.status =
                "Pending"
    );


    document.getElementById(
        "battery"
    ).innerText =
        "100%";


    document.getElementById(
        "capacity"
    ).innerText =
        "5 / 5";


    document.getElementById(
        "robotLocation"
    ).innerText =
        "Cafeteria";


    displayOrders();

    updatePendingCount();


    showResult(
        "🔄 Robot reset successfully."
    );

}


/* ================= NAVIGATION ================= */

function showSection(id) {

    document
        .querySelectorAll(
            ".section"
        )
        .forEach(
            section =>
                section.classList.remove(
                    "active"
                )
        );


    document
        .getElementById(id)
        .classList.add(
            "active"
        );


    window.scrollTo({
        top: 0,
        behavior: "smooth"
    });

}


/* ================= START ================= */

displayOrders();

updatePendingCount();

</script>

</body>
</html>
