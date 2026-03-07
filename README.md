# HCI Lab 5 – HCI Principles Demo

## Overview

This project demonstrates fundamental **Human-Computer Interaction (HCI)** principles through a simple, interactive web interface. The application showcases how users interact with systems and how the system communicates its state back to the user.

### Key Principles Showcased:

* **Visibility of system status**
* **Immediate feedback**
* **Constraints**
* **Signifiers**

The interface allows users to click a button to simulate processing an action, while dynamically updating system status and enforcing interaction limits.

---

## 📁 Project Structure

```bash
HCI_LAB5 
│
├── index.html      # Main HTML structure
├── style.css       # Styling and visual feedback
├── script.js       # Interaction logic and behavior
└── README.md       # Project documentation

```

---

## How It Works

1. **User Interaction:** The user clicks the "Process Data" button.
2. **Feedback:** The button temporarily changes appearance (yellow highlight) and the status message updates with the click count.
3. **Constraint Enforcement:** After **3 clicks**, the system:
* Disables the button.
* Changes styling to indicate a restriction.
* Displays a "Limit reached" message with a red visual constraint.



---

## HCI Principles Demonstrated

### ✅ 1. Visibility of System Status

The `<div id="status">` element continuously informs the user of their progress. This ensures the user is never left guessing about the current state of the application.

### ✅ 2. Feedback

Every action has a reaction. Immediate feedback occurs when:

* The button turns yellow upon clicking.
* The status text updates instantly.
* The limit message appears.

### ✅ 3. Constraints

Logical constraints prevent user error by restricting actions before they can lead to an invalid state.

```javascript
if (count >= 3) {
    btn.disabled = true;
}

```

> **Goal:** Prevent further interaction after three clicks, reducing errors and enforcing system rules.

### ✅ 4. Signifiers

Visual cues communicate the "soul" of the interface:

* **Disabled styling:** Greyed out button indicates it's no longer clickable.
* **Red border:** High-contrast color indicates a limit or error state.
* **Symbols:** Using (✔, ⛔) provides instant semantic meaning.

---

## Expected Behavior

| Click Count | System Response | Visual Feedback |
| --- | --- | --- |
| **1** | Button highlights, status updates | Yellow Glow / Text Update |
| **2** | Button highlights again, status updates | Yellow Glow / Text Update |
| **3** | Button disables, red warning displayed | **Red Border / Disabled State** |
| **4+** | No action (Interaction blocked) | Static Disabled UI |

---

## Concept Reference

This demo aligns with interaction design principles commonly discussed in:

* **Don Norman’s** Design Principles (The Design of Everyday Things)
* Fundamental **HCI Usability Heuristics**
* Feedback and Affordance models in UI design

---

**Course:** Human-Computer Interaction

**Project:** HCI Lab 5 Submission
