-----------
Homework 5
-----------
This program takes an execution plan for processes and updates the Vector Clocks.

Input
-----

- 3 processes with id.
- Execution plan given


Output
------
Vector Clock at p0 : [vc=[5, 5, 5]]
Vector Clock at p1 : [vc=[2, 5, 5]]
Vector Clock at p2 : [vc=[2, 3, 7]]
 
--------------Output Displayed--------------

Starting execution for p0
Starting execution for p1

Receive initiated: p1 is waiting for p0
Starting execution for p2

---Compute by p2 Message [messageType=COMPUTATION, vc=null]
---VC for p2 is:VectorClock [vc=[0, 0, 1]]

### P2 tread is sleeping for 1sec before computing (Event Q11)

---Message sent by p0 to p1 Message [messageType=SEND, vc=VectorClock [vc=[1, 0, 0]]]
---VC for p0 is:VectorClock [vc=[1, 0, 0]]

### P0 tread is sleeping for 2sec before sending message to p2(Event Q2)

---Message received by p1 from p0 Message [messageType=RECEIVE, vc=VectorClock [vc=[0, 0, 0]]]
---VC for p1 is:VectorClock [vc=[1, 1, 0]]

Receive initiated: p1 is waiting for p2

---Compute by p2 Message [messageType=COMPUTATION, vc=null]
---VC for p2 is:VectorClock [vc=[0, 0, 2]]

---Message received by p1 from p2 Message [messageType=RECEIVE, vc=VectorClock [vc=[1, 1, 0]]]
---VC for p1 is:VectorClock [vc=[1, 2, 3]]

---Message sent by p2 to p1 Message [messageType=SEND, vc=VectorClock [vc=[0, 0, 3]]]
---VC for p2 is:VectorClock [vc=[0, 0, 3]]

---Message sent by p1 to p2 Message [messageType=SEND, vc=VectorClock [vc=[1, 3, 3]]]
---VC for p1 is:VectorClock [vc=[1, 3, 3]]

Receive initiated: p2 is waiting for p0

### P1 tread is sleeping for 3sec before receiving message to p2 (Event Q9)

---Message sent by p0 to p2 Message [messageType=SEND, vc=VectorClock [vc=[2, 0, 0]]]
---VC for p0 is:VectorClock [vc=[2, 0, 0]]

---Message received by p2 from p0 Message [messageType=RECEIVE, vc=VectorClock [vc=[0, 0, 3]]]
---VC for p2 is:VectorClock [vc=[2, 0, 4]]

---Message sent by p2 to p1 Message [messageType=SEND, vc=VectorClock [vc=[2, 0, 5]]]
---VC for p2 is:VectorClock [vc=[2, 0, 5]]

---Message received by p2 from p1 Message [messageType=RECEIVE, vc=VectorClock [vc=[2, 0, 5]]]
---VC for p2 is:VectorClock [vc=[2, 3, 6]]

---Compute by p2 Message [messageType=COMPUTATION, vc=null]
---VC for p2 is:VectorClock [vc=[2, 3, 7]]

*****Completed execution for p2. Vector Clock at p2 is:VectorClock [vc=[2, 3, 7]]

---Compute by p0 Message [messageType=COMPUTATION, vc=null]
---VC for p0 is:VectorClock [vc=[3, 0, 0]]

### P0 tread is sleeping for 1sec before receiving message from p1(Event Q4)

---Message received by p1 from p2 Message [messageType=RECEIVE, vc=VectorClock [vc=[1, 3, 3]]]
---VC for p1 is:VectorClock [vc=[2, 4, 5]]

---Message sent by p1 to p0 Message [messageType=SEND, vc=VectorClock [vc=[2, 5, 5]]]
---VC for p1 is:VectorClock [vc=[2, 5, 5]]

*****Completed execution for p1. Vector Clock at p1 is:VectorClock [vc=[2, 5, 5]]

---Message received by p0 from p1 Message [messageType=RECEIVE, vc=VectorClock [vc=[3, 0, 0]]]
---VC for p0 is:VectorClock [vc=[4, 5, 5]]

---Compute by p0 Message [messageType=COMPUTATION, vc=null]
---VC for p0 is:VectorClock [vc=[5, 5, 5]]

*****Completed execution for p0. Vector Clock at p0 is:VectorClock [vc=[5, 5, 5]]