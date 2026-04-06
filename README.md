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

## How it Works

```
┌─────────────────────────────────────────────────────────────┐
│                     Your Browser                            │
│                                                             │
│  ┌─────────────────────┐    ┌──────────────────────────┐   │
│  │   AndroMate Studio  │    │   AndroMate Backoffice   │   │
│  │                     │    │                          │   │
│  │  Design your        │    │  Monitor jobs, devices,  │   │
│  │  workflow visually  │    │  results & schedules     │   │
│  └──────────┬──────────┘    └──────────────────────────┘   │
└─────────────┼───────────────────────────────────────────────┘
              │  Save & dispatch
              ▼
┌─────────────────────────────┐
│   AndroMate Cloud           │
│                             │
│   Receives your workflow,   │
│   queues the job, and       │
│   dispatches it to the      │
│   right device              │
└──────────┬──────────────────┘
           │  Job delivered instantly
     ┌─────┼──────┐
     ▼     ▼      ▼
   📱      📱     📱
 Device  Device  Device
   #1      #2      #3

  Each device runs the workflow natively and
  streams results back to your Backoffice in real time.
```

---

## Available Tasks

Every task in AndroMate is a node you can drag, configure, and connect in the visual workflow editor. Each task can produce an **output** — a value that becomes available as a variable for any following task in the workflow. This is what makes AndroMate workflows dynamic: the result of one step directly feeds the next.

### Workflow Control

| Task | What it does |
|---|---|
| **Start** | Entry point of every workflow |
| **End** | Terminates the workflow cleanly |
| **Condition** | Evaluates a value and branches to a True or False path |
| **Check Exception** | Detects if an error occurred in a previous step and reacts accordingly |

### Workflow Runtime

| Task | What it does |
|---|---|
| **Set Variable** | Define or update a variable at any point in the workflow |
| **Arithmetic Operations** | Add, subtract, multiply, divide, increment, or decrement numeric variables |
| **Compare Numbers** | Compare two numeric values — output usable in a Condition node |
| **Compare Variables** | Compare two string or dynamic variables |
| **JSON Object Operation** | Extract or manipulate a value inside a JSON object — output available as a variable |

### Android UI

| Task | What it does |
|---|---|
| **UI Automator** | Tap, swipe, scroll, type text, or click by element ID — full UI control on any app |
| **Screen Series Automation** | Execute a sequence of UI actions in a defined order |
| **Intent** | Send a broadcast or start an activity on the device |
| **Screen OCR** | Capture the screen, extract its text — output available as a variable for the next task |

### Communication

| Task | What it does |
|---|---|
| **HTTP Request** | Make GET, POST, PUT, DELETE requests — the response body is available as output |
| **DNS Lookup** | Resolve a domain and measure DNS response time — result stored as output |
| **Download Bitrate** | Measure real download speed on the device — outputs the measured value |
| **Upload Bitrate** | Measure real upload speed on the device — outputs the measured value |
| **Iperf3** | Run advanced network benchmarks (throughput, jitter, packet loss) — full result as output |

### Bluetooth (BLE)

| Task | What it does |
|---|---|
| **BLE Scan** | Discover nearby BLE devices — outputs the list of found devices |
| **BLE Connect** | Connect to a specific BLE device by address |
| **BLE Disconnect** | Cleanly close a BLE connection |
| **BLE Pairing** | Initiate pairing with a BLE peripheral |
| **BLE Read Characteristic** | Read a GATT characteristic value — output available for the next task |
| **BLE Write Characteristic** | Write a value to a GATT characteristic |

### SMS

| Task | What it does |
|---|---|
| **Send SMS** | Send a text message to any phone number |
| **Wait for SMS** | Pause the workflow until a specific SMS arrives — the received message is available as output |

### Location

| Task | What it does |
|---|---|
| **Get Current Location** | Retrieve GPS coordinates (latitude, longitude, altitude) — all values available as output |
| **Get Current Speed** | Measure the device's real-time movement speed — output usable in the next step |

### Time

| Task | What it does |
|---|---|
| **Sleep** | Pause execution for a defined duration |
| **NTP Sync** | Synchronize the device clock with an NTP server |

### Reporting

| Task | What it does |
|---|---|
| **Text Report** | Write a custom message to the execution log — supports AML variables as dynamic content |

### Code & Commands

| Task | What it does |
|---|---|
| **Shell Command** | Execute a shell command on the device — standard output available as a variable |
| **Java Code** | Run a custom inline code snippet within the workflow |

---

## AML — AndroMate Language

AML is what makes AndroMate workflows truly dynamic. Every task that produces a result — an HTTP response, a GPS coordinate, a BLE read value, a measured bitrate, an OCR-extracted text — exposes that result as a named variable.

You can then inject that variable into any following task as input, simply by referencing it by name. This creates a natural data pipeline inside your workflow: the output of one step becomes the input of the next, without any manual wiring or scripting.

For example, you can run an HTTP request, extract a value from the response using a JSON Operation task, and pass that value directly into a Send SMS task — all within the same workflow, no code required.

On top of task outputs, AndroMate also provides a set of built-in device variables that are always available at runtime:

- `${ANDROID_VERSION}` — the Android version running on the device
- `${BRAND}` — the device manufacturer (Samsung, Google, Xiaomi…)
- `${CURRENT_DATE}` — today's date at execution time
- `${CURRENT_TIME_STAMP}` — Unix timestamp at the moment the task runs
- `${CURRENT_SDK}` — the Android SDK API level

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
