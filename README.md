<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bus Parking Management System</title>
    <style>
        /* CSS Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #f5f5f5;
            color: #333;
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        header {
            background-color: #2c3e50;
            color: white;
            padding: 20px 0;
            text-align: center;
            margin-bottom: 30px;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }

        .dashboard {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 20px;
            margin-bottom: 30px;
        }

        .controls {
            background-color: white;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        .parking-grid {
            background-color: white;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        h2 {
            margin-bottom: 20px;
            color: #2c3e50;
            border-bottom: 2px solid #eee;
            padding-bottom: 10px;
        }

        .form-group {
            margin-bottom: 15px;
        }

        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }

        input, select {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 16px;
        }

        button {
            background-color: #3498db;
            color: white;
            border: none;
            padding: 10px 15px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
            transition: background-color 0.3s;
        }

        button:hover {
            background-color: #2980b9;
        }

        .parking-slots {
            display: grid;
            grid-template-columns: repeat(5, 1fr);
            gap: 15px;
        }

        .slot {
            height: 100px;
            background-color: #ecf0f1;
            border-radius: 5px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            position: relative;
            transition: all 0.3s;
        }

        .slot.occupied {
            background-color: #e74c3c;
            color: white;
        }

        .slot.available {
            background-color: #2ecc71;
            color: white;
        }

        .slot.reserved {
            background-color: #f39c12;
            color: white;
        }

        .slot-number {
            font-weight: bold;
            font-size: 1.2rem;
        }

        .slot-info {
            font-size: 0.8rem;
            text-align: center;
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            margin-bottom: 30px;
        }

        .stat-card {
            background-color: white;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            text-align: center;
        }

        .stat-value {
            font-size: 2rem;
            font-weight: bold;
            color: #2c3e50;
            margin: 10px 0;
        }

        .stat-label {
            color: #7f8c8d;
        }

        .logs {
            background-color: white;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        .log-list {
            max-height: 200px;
            overflow-y: auto;
            border: 1px solid #eee;
            padding: 10px;
            border-radius: 4px;
        }

        .log-entry {
            padding: 8px 0;
            border-bottom: 1px solid #eee;
            font-size: 0.9rem;
        }

        .log-entry:last-child {
            border-bottom: none;
        }

        .timestamp {
            color: #7f8c8d;
            font-size: 0.8rem;
        }

        @media (max-width: 768px) {
            .dashboard {
                grid-template-columns: 1fr;
            }

            .parking-slots {
                grid-template-columns: repeat(3, 1fr);
            }

            .stats {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Bus Parking Management System</h1>
            <p>Efficiently manage bus parking operations</p>
        </header>

        <div class="stats">
            <div class="stat-card">
                <div class="stat-label">Total Slots</div>
                <div class="stat-value" id="total-slots">20</div>
            </div>
            <div class="stat-card">
                <div class="stat-label">Available</div>
                <div class="stat-value" id="available-slots">15</div>
            </div>
            <div class="stat-card">
                <div class="stat-label">Occupied</div>
                <div class="stat-value" id="occupied-slots">5</div>
            </div>
        </div>

        <div class="dashboard">
            <div class="controls">
                <h2>Parking Controls</h2>
                <div class="form-group">
                    <label for="bus-number">Bus Number</label>
                    <input type="text" id="bus-number" placeholder="Enter bus number">
                </div>
                <div class="form-group">
                    <label for="driver-name">Driver Name</label>
                    <input type="text" id="driver-name" placeholder="Enter driver name">
                </div>
                <div class="form-group">
                    <label for="slot-select">Select Slot</label>
                    <select id="slot-select">
                        <option value="">-- Select a slot --</option>
                        <!-- Options will be populated by JavaScript -->
                    </select>
                </div>
                <div class="form-group">
                    <label for="parking-time">Parking Time</label>
                    <input type="datetime-local" id="parking-time">
                </div>
                <button id="park-btn">Park Bus</button>
                <button id="release-btn" style="background-color: #e74c3c; margin-top: 10px;">Release Slot</button>
            </div>

            <div class="parking-grid">
                <h2>Parking Slots</h2>
                <div class="parking-slots" id="parking-slots">
                    <!-- Slots will be populated by JavaScript -->
                </div>
            </div>
        </div>

        <div class="logs">
            <h2>Activity Log</h2>
            <div class="log-list" id="log-list">
                <!-- Log entries will be added by JavaScript -->
            </div>
        </div>
    </div>

    <script>
        // JavaScript for Bus Parking System
        document.addEventListener('DOMContentLoaded', function() {
            // Initialize the system
            const parkingSystem = {
                totalSlots: 20,
                availableSlots: 15,
                occupiedSlots: 5,
                slots: [],
                logs: [],
                
                init: function() {
                    // Initialize slots
                    for (let i = 1; i <= this.totalSlots; i++) {
                        let status = 'available';
                        let bus = null;
                        
                        // Mark some slots as occupied for demo
                        if (i <= this.occupiedSlots) {
                            status = 'occupied';
                            bus = {
                                number: `BUS${100 + i}`,
                                driver: `Driver ${i}`,
                                time: new Date().toISOString()
                            };
                        }
                        
                        this.slots.push({
                            id: i,
                            status: status,
                            bus: bus
                        });
                    }
                    
                    this.renderSlots();
                    this.updateStats();
                    this.populateSlotSelect();
                    this.addLog('System initialized', 'info');
                },
                
                renderSlots: function() {
                    const slotsContainer = document.getElementById('parking-slots');
                    slotsContainer.innerHTML = '';
                    
                    this.slots.forEach(slot => {
                        const slotElement = document.createElement('div');
                        slotElement.className = `slot ${slot.status}`;
                        slotElement.dataset.id = slot.id;
                        
                        let info = 'Available';
                        if (slot.status === 'occupied' && slot.bus) {
                            info = `${slot.bus.number}<br>${slot.bus.driver}`;
                        }
                        
                        slotElement.innerHTML = `
                            <div class="slot-number">${slot.id}</div>
                            <div class="slot-info">${info}</div>
                        `;
                        
                        // Add click event to select slot
                        slotElement.addEventListener('click', () => {
                            this.selectSlot(slot.id);
                        });
                        
                        slotsContainer.appendChild(slotElement);
                    });
                },
                
                populateSlotSelect: function() {
                    const select = document.getElementById('slot-select');
                    select.innerHTML = '<option value="">-- Select a slot --</option>';
                    
                    this.slots.forEach(slot => {
                        if (slot.status === 'available') {
                            const option = document.createElement('option');
                            option.value = slot.id;
                            option.textContent = `Slot ${slot.id}`;
                            select.appendChild(option);
                        }
                    });
                },
                
                selectSlot: function(slotId) {
                    const slot = this.slots.find(s => s.id === slotId);
                    if (!slot) return;
                    
                    // Highlight selected slot
                    document.querySelectorAll('.slot').forEach(el => {
                        el.classList.remove('selected');
                    });
                    document.querySelector(`.slot[data-id="${slotId}"]`).classList.add('selected');
                    
                    // Update form fields if slot is occupied
                    if (slot.status === 'occupied' && slot.bus) {
                        document.getElementById('bus-number').value = slot.bus.number;
                        document.getElementById('driver-name').value = slot.bus.driver;
                        document.getElementById('slot-select').value = slot.id;
                        
                        // Format the date for the datetime-local input
                        const date = new Date(slot.bus.time);
                        const formattedDate = date.toISOString().slice(0, 16);
                        document.getElementById('parking-time').value = formattedDate;
                    }
                },
                
                parkBus: function() {
                    const busNumber = document.getElementById('bus-number').value.trim();
                    const driverName = document.getElementById('driver-name').value.trim();
                    const slotId = parseInt(document.getElementById('slot-select').value);
                    const parkingTime = document.getElementById('parking-time').value;
                    
                    if (!busNumber || !driverName || !slotId || !parkingTime) {
                        alert('Please fill all fields');
                        return;
                    }
                    
                    const slot = this.slots.find(s => s.id === slotId);
                    if (!slot || slot.status !== 'available') {
                        alert('Selected slot is not available');
                        return;
                    }
                    
                    // Update slot
                    slot.status = 'occupied';
                    slot.bus = {
                        number: busNumber,
                        driver: driverName,
                        time: parkingTime
                    };
                    
                    // Update counts
                    this.availableSlots--;
                    this.occupiedSlots++;
                    
                    // Update UI
                    this.renderSlots();
                    this.updateStats();
                    this.populateSlotSelect();
                    this.addLog(`Bus ${busNumber} parked in slot ${slotId} by ${driverName}`, 'park');
                    
                    // Clear form
                    document.getElementById('bus-number').value = '';
                    document.getElementById('driver-name').value = '';
                    document.getElementById('slot-select').value = '';
                    document.getElementById('parking-time').value = '';
                },
                
                releaseSlot: function() {
                    const slotId = parseInt(document.getElementById('slot-select').value);
                    if (!slotId) {
                        alert('Please select a slot to release');
                        return;
                    }
                    
                    const slot = this.slots.find(s => s.id === slotId);
                    if (!slot || slot.status !== 'occupied') {
                        alert('Selected slot is not occupied');
                        return;
                    }
                    
                    const busNumber = slot.bus.number;
                    const driverName = slot.bus.driver;
                    
                    // Update slot
                    slot.status = 'available';
                    slot.bus = null;
                    
                    // Update counts
                    this.availableSlots++;
                    this.occupiedSlots--;
                    
                    // Update UI
                    this.renderSlots();
                    this.updateStats();
                    this.populateSlotSelect();
                    this.addLog(`Bus ${busNumber} released from slot ${slotId} (Driver: ${driverName})`, 'release');
                    
                    // Clear form
                    document.getElementById('bus-number').value = '';
                    document.getElementById('driver-name').value = '';
                    document.getElementById('slot-select').value = '';
                    document.getElementById('parking-time').value = '';
                },
                
                updateStats: function() {
                    document.getElementById('total-slots').textContent = this.totalSlots;
                    document.getElementById('available-slots').textContent = this.availableSlots;
                    document.getElementById('occupied-slots').textContent = this.occupiedSlots;
                },
                
                addLog: function(message, type) {
                    const timestamp = new Date().toLocaleString();
                    const logEntry = {
                        message: message,
                        type: type,
                        timestamp: timestamp
                    };
                    
                    this.logs.unshift(logEntry); // Add to beginning of array
                    if (this.logs.length > 50) {
                        this.logs.pop(); // Keep only last 50 entries
                    }
                    
                    this.renderLogs();
                },
                
                renderLogs: function() {
                    const logList = document.getElementById('log-list');
                    logList.innerHTML = '';
                    
                    this.logs.forEach(log => {
                        const logEntry = document.createElement('div');
                        logEntry.className = `log-entry ${log.type}`;
                        
                        let icon = 'ℹ️';
                        if (log.type === 'park') icon = '🅿️';
                        if (log.type === 'release') icon = '🚌';
                        
                        logEntry.innerHTML = `
                            <span class="timestamp">[${log.timestamp}]</span> ${icon} ${log.message}
                        `;
                        
                        logList.appendChild(logEntry);
                    });
                }
            };
            
            // Initialize the system
            parkingSystem.init();
            
            // Event listeners
            document.getElementById('park-btn').addEventListener('click', () => {
                parkingSystem.parkBus();
            });
            
            document.getElementById('release-btn').addEventListener('click', () => {
                parkingSystem.releaseSlot();
            });
            
            // Set current time as default for parking time
            const now = new Date();
            const formattedNow = now.toISOString().slice(0, 16);
            document.getElementById('parking-time').value = formattedNow;
        });
    </script>
</body>
</html>
