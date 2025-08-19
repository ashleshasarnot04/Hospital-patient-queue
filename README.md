# Hospital-patient-queue
🔹 Project Overview

This is a queue management system for a hospital.
Patients can be either:

Emergency/Critical → handled first using a Priority Queue.

Regular/Normal → handled in FCFS (First Come First Serve) order with a normal queue.

The system will:

Add patients with details (ID, name, severity, estimated treatment time).

Always serve emergency patients first.

Calculate and display estimated wait time for any patient.

Show current queue status.

🔹 Features in Detail
1. Patient Data Structure

Each patient has:

Patient ID

Name

Severity (critical or regular)

Estimated treatment time (e.g., 15 mins)

Arrival order (for fairness in regular queue)

2. Priority Queue for Emergency Cases

Critical patients go into a max-priority queue (priority = severity level, higher = more urgent).

Ensures life-threatening cases are handled first.

3. Normal Queue for Regular Patients

Implemented as a simple FIFO queue.

Patients are served in order of arrival.

4. Estimated Wait Time

For emergency patients → wait time = sum of treatment times of emergency patients ahead in priority order.

For regular patients → wait time =
(all emergency patients’ treatment time) + (treatment time of regular patients before them).

5. Operations

Add new patient (emergency/regular).

Serve next patient (based on queue rules).

Show estimated wait time of a patient.

Display all patients in both queues.

🔹 How to Run

Compile the C++ program:

g++ hospital_queue.cpp -o hospital_queue
