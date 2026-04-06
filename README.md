# AndroMate — Support & Feedback

> Got a question, a suggestion, or found something that's not working as expected?
> You're in the right place.

📧 Email: **support@andromate.net**
🐛 Issues: [Open an issue](https://github.com/andromate/andromate-support/issues/new)

---

## What is AndroMate?

AndroMate is a cloud-native automation platform built specifically for Android. It lets you design workflows visually in your browser and execute them on real Android devices — remotely, on a schedule, or on demand.

No scripts. No ADB setup. No manual effort.

You build your workflow once in **AndroMate Studio**, and the **AndroMate Android app** installed on your device picks it up, runs it natively, and sends the results back to your **Backoffice** dashboard in real time.

---

## Available Tasks

AndroMate comes with a growing library of built-in tasks organized by category. Every task is a node you can drag, configure, and connect in the visual workflow editor.

### Workflow Control
The foundation of every workflow. Control how execution flows from one step to the next.

- **Start** — the entry point of any workflow
- **End** — terminates the workflow cleanly
- **Condition** — evaluates a boolean expression and branches to a True or False path
- **Check Exception** — detects if an error occurred in a previous step and reacts accordingly

### Workflow Runtime
Manage data and variables during execution.

- **Set Variable** — define or update a variable at any point in the workflow
- **Arithmetic Operations** — perform calculations between numeric variables (add, subtract, multiply, divide, increment, decrement)
- **Compare Numbers** — compare two numeric values and use the result in a condition
- **Compare Variables** — compare two string or dynamic variables
- **JSON Object Operation** — extract, manipulate, or read values from a JSON object at runtime

### Android UI
Interact with the Android interface directly — just like a real user would.

- **UI Automator** — tap, swipe, scroll, type text, click by element ID or text — full UI interaction on any app
- **Screen Series Automation** — execute a sequence of UI actions in a defined order
- **Intent** — send a broadcast or start an activity on the device (deep integration with the Android OS)
- **Screen OCR** — capture the screen and extract text using optical character recognition

### Communication
Test and interact with networks and remote services.

- **HTTP Request** — make GET, POST, PUT, DELETE requests to any API or server
- **DNS Lookup** — resolve a domain name and measure DNS response time
- **Download / Upload Bitrate** — measure real download and upload speeds on the device
- **Iperf3** — run advanced network performance benchmarks (throughput, jitter, packet loss)

### Bluetooth (BLE)
Automate Bluetooth Low Energy interactions end-to-end.

- **BLE Scan** — discover nearby BLE devices
- **BLE Connect** — connect to a specific BLE device by address
- **BLE Disconnect** — cleanly terminate a BLE connection
- **BLE Pairing** — initiate pairing with a BLE device
- **BLE Read Characteristic** — read a value from a GATT characteristic
- **BLE Write Characteristic** — write a value to a GATT characteristic

### SMS
Automate SMS interactions on the device.

- **Send SMS** — send a text message to any phone number
- **Wait for SMS** — pause the workflow until a specific SMS is received (with timeout support)

### Location
Work with GPS and movement data in real time.

- **Get Current Location** — retrieve the device's current GPS coordinates (latitude, longitude, altitude)
- **Get Current Speed** — measure the device's real-time movement speed

### Time
Control timing and synchronization within your workflow.

- **Sleep** — pause execution for a defined duration
- **NTP Sync** — synchronize the device clock with an NTP server before time-sensitive operations

### Reporting
Generate structured output as part of your workflow.

- **Text Report** — write a custom message to the execution log with support for AML dynamic variables (e.g. `${BRAND}`, `${ANDROID_VERSION}`, `${CURRENT_DATE}`)

### Code & Commands
For advanced use cases that need lower-level access.

- **Shell Command** — execute a shell command directly on the device
- **Java Code** — run a custom Java snippet inline within the workflow

---

## AML — AndroMate Language

Every task field supports AML variables — dynamic values that are resolved at runtime directly on the device. Use them in any text field, report, or HTTP request body without hardcoding anything.

Some examples:

- `${ANDROID_VERSION}` — the Android version running on the device
- `${BRAND}` — the device manufacturer (Samsung, Google, Xiaomi…)
- `${CURRENT_DATE}` — today's date at execution time
- `${CURRENT_TIME_STAMP}` — Unix timestamp when the task runs
- `${CURRENT_SDK}` — the Android SDK level

---

## How to Get Help

### Open a GitHub Issue
The best way to track your request. Use it for:

- Something that is not working the way you expect
- A task or feature you'd like to see added
- A question about how a specific task or workflow works
- Anything missing or unclear

👉 [Open an issue](https://github.com/andromate/andromate-support/issues/new)

Before opening, please check if a similar issue already exists to avoid duplicates.

### Send an Email
For anything you'd prefer to discuss privately — billing, partnerships, or sensitive bug reports:

📧 **support@andromate.net**

We respond to every message. Typical response time is within 48 hours.

---

> © 2026 AndroMate — Built for Android automation.
