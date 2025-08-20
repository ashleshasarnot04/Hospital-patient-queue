# Hospital-patient-queue
 Project Overview

This is a hospital queue management system.
Patients can be either:

Emergency/Critical → treated first using a Priority Queue.

Regular/Normal → treated in FCFS (First Come First Serve) order with a normal queue.

The system will:

Add patients with details (ID, name, severity, estimated treatment time).

Always treat emergency patients first.

Calculate and show estimated wait time for any patient.

Show current queue status.

 Features in Detail
1. Patient Data Structure

Every patient has:

Patient ID

Name

Severity (serious or normal)

Estimated treatment time (e.g., 15 minutes)

Arrival order (for fairness in normal queue)

2. Emergency Queue for Critical Cases

Critical patients enter a max-priority queue (priority = severity level, higher = more critical).

Guarantees life-threatening cases to be treated first.

3. Normal Queue for Normal Patients

Executed as a basic FIFO queue.

Patients are treated according to the order of arrival.

4. Estimated Wait Time

For emergency patients → wait time = total of treatment times of emergency patients in priority order.

For regular patients → wait time =
(total of all emergency patients' treatment time) + (treatment time of all regular patients in front of them).

5. Operations

Add new patient (emergency/regular).

Serve next patient (according to queue rules).

Display estimated wait time of a patient.

Display all patients in both queues.

 How to Run

Build the C++ program:
g++ hospital_queue.cpp -o hospital_queue

