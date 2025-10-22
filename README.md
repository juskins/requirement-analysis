# Requirement Analysis in Software Development
This repositry is a Requirement Analysis project that focuses on crafting a comprehensive foundation for software development by documenting, analyzing, and structuring requirements.
# What is Requirement Analysis?
## 📘 Overview

**Requirement Analysis** is the **first and one of the most crucial phases** of the Software Development Life Cycle (SDLC).  
It involves **gathering, understanding, and documenting** what a system is supposed to achieve — both from a **functional** and **non-functional** perspective.

The goal is to ensure **clarity, completeness, and alignment** between what stakeholders expect and what developers deliver.

---

## 🎯 Objectives of Requirement Analysis

1. **Identify Stakeholder Needs:**  
   Understand who the users are and what problems they are trying to solve.

2. **Define System Requirements:**  
   Translate user needs into clear, actionable technical requirements.

3. **Establish Scope:**  
   Clearly define what is included in (and excluded from) the system to prevent scope creep.

4. **Create a Foundation for Design & Development:**  
   Provide developers and designers with a roadmap that aligns with business objectives.

---

## 🧠 Why is Requirement Analysis Important?

| Phase | Dependency on Requirement Analysis |
|-------|------------------------------------|
| **Planning** | Determines project feasibility, cost, and timeline. |
| **Design** | Architecture and UI decisions depend on accurate requirements. |
| **Development** | Guides developers on what to build and how it should behave. |
| **Testing** | Test cases are derived directly from the requirements. |
| **Deployment & Maintenance** | Ensures updates and fixes align with the intended goals. |

A **poorly conducted requirement analysis** often leads to:
- Miscommunication among stakeholders  
- Cost overruns and schedule delays  
- Rework and technical debt  
- Low user satisfaction or system failure  

---

## 🧩 Key Activities in Requirement Analysis.

1. **Requirement Gathering:**  
   Collect raw information from stakeholders, end-users, and subject matter experts through:
   - Interviews  
   - Surveys  
   - Observation  
   - Document analysis  

2. **Requirement Elicitation:**  
   Engage with users to extract and clarify their needs, even the ones not explicitly stated.

3. **Requirement Documentation:**  
   Document requirements clearly and precisely using:
   - Software Requirement Specification (SRS)  
   - Use Cases  
   - User Stories
  
4. **Requirement Analysis and Modeling:**  
   Prioritizig requirements based on importance and impact, analyzing the feasibility, and creating models (e.g data flow diagrams) to visualize and analyze requirements.

4. **Requirement Validation:**  
   Review and confirm that documented requirements accurately reflect user needs and are feasible within constraints.

5. **Requirement Management:**  
   Continuously monitor and update requirements as the project evolves.

---

## 📄 Types of Requirements

In software engineering, requirements are generally classified into two broad categories: **Functional Requirements** and **Non-Functional Requirements**.  
This section provides clear definitions and examples for each, tailored to the **Booking Management System** (inspired by Airbnb/OYO’s system architecture).

---

### ⚙️ Functional Requirements

**Definition:**  
Functional requirements describe *what the system should do*. They define the specific behaviors, actions, and features that enable users to interact with the application.

**Examples (for the Booking Management Project):**
- The system shall allow users to **search for properties** by location, date range, number of guests, and filters such as price or amenities.
- The system shall allow users to **view detailed property information**, including images, host details, availability calendar, pricing, reviews, and booking options.
- The system shall allow users to **create and confirm bookings**, select dates, enter payment details, and receive a confirmation receipt.
- The system shall allow **hosts to list new properties**, upload images, define availability, and set pricing and rules.
- The system shall provide **real-time availability checks** using cached data (e.g., Redis) before confirming bookings.
- The system shall allow **user authentication and authorization**, supporting roles like Guest, Host, and Admin.
- The system shall generate **notifications** for booking confirmations, cancellations, or changes.
- The system shall allow **admins to monitor bookings and resolve disputes**.

---

### ⚡ Non-Functional Requirements

**Definition:**  
Non-functional requirements define *how well* the system performs. They refer to system qualities such as performance, scalability, reliability, and security rather than specific features.

**Examples (for the Booking Management Project):**

#### 🧠 Performance
- Search results should load within **2 seconds** for 95% of user requests under normal load.
- Cached queries (via Redis) for “recent booking history” should respond within **500 milliseconds**.

#### ☁️ Scalability
- The system should handle **1,000 concurrent booking requests** without service degradation.
- The architecture should support **horizontal scaling** through microservices and distributed databases.

#### 🔐 Security
- All payment transactions must use **HTTPS** and comply with **PCI DSS** standards.
- Passwords must be **hashed and salted** using secure algorithms such as bcrypt.
- Sensitive user data must be encrypted both in transit and at rest.

#### ⚙️ Reliability & Availability
- The system must achieve **99.9% uptime** during peak hours.
- Each booking transaction must follow **ACID principles**, ensuring complete or rollback behavior.

#### 🧩 Maintainability & Extensibility
- The system should adopt a **microservices architecture** to allow independent service updates and feature additions.
- Source code should follow **modular, well-documented** structure to simplify maintenance.

#### ♿ Usability & Accessibility
- The user interface (UI) must comply with **WCAG 2.1 AA** accessibility standards.
- The design should ensure a seamless experience on **mobile, tablet, and desktop devices**.


---

## 🧩 Use Case Diagrams

### 📖 What Are Use Case Diagrams?

A **Use Case Diagram** is a visual representation of how different users (called **actors**) interact with a system.  
It illustrates the **functional requirements** of a system by showing what each user can do and how the system responds.

In essence, a Use Case Diagram answers the question:  
**“Who does what in the system?”**

Use Case Diagrams are a key part of the **Requirement Analysis phase** in the **Software Development Life Cycle (SDLC)**.  
They help capture the intended behavior of the system from the user's point of view.

---

### 💡 Benefits of Use Case Diagrams

- **Clarity of Requirements:** Simplifies complex system behavior into easy-to-understand interactions.  
- **User-Focused Design:** Highlights user goals and how the system supports them.  
- **Improved Communication:** Bridges understanding between developers, designers, and stakeholders.  
- **Scope Definition:** Defines system boundaries and identifies external dependencies.  
- **Foundation for Design & Testing:** Serves as a base for creating detailed design and test cases.

---

### 🏨 Example: Booking Management System

Below is an example **Use Case Diagram** illustrating how different actors interact with the booking system.

![Use Case Diagram]((https://github.com/juskins/requirement-analysis/blob/main/alx-booking-uc.png?raw=true))

---

### 🎭 Actors

- **Guest/User:**  
  Can search hotels, view details, make bookings, complete payments, cancel reservations, and write reviews.  

- **Host:**  
  Can list properties, update details, and manage availability.  

- **Admin:**  
  Can approve listings, manage users, and oversee system activities.  

---

### ⚙️ Key Use Cases

| Use Case | Description |
|-----------|-------------|
| **Search Hotels** | Allows users to search for hotels by location, date, or filters. |
| **View Hotel Details** | Displays detailed property information including images and pricing. |
| **Book Room** | Enables users to reserve rooms for specific dates. |
| **Make Payment** | Facilitates secure checkout and payment processing. |
| **Cancel Booking** | Allows users to modify or cancel an existing booking. |
| **Write Review** | Enables users to leave feedback for properties. |
| **List Property** | Allows hosts to upload property details and manage listings. |
| **Manage Users** | Admin feature to handle user accounts and permissions. |

---

## ✅ Acceptance Criteria

### 📘 What Are Acceptance Criteria?

**Acceptance Criteria (AC)** are the predefined conditions that a software feature or system must meet to be accepted by stakeholders, clients, or end-users.  
They act as a **bridge between requirements and testing**, ensuring that the implemented feature behaves exactly as expected.

Acceptance Criteria define **“what success looks like”** for a feature and serve as a checklist for developers, QA testers, and product owners to confirm that a user story or requirement is complete.

---

### 💡 Importance of Acceptance Criteria in Requirement Analysis

- **Clarifies Expectations:** Ensures everyone (developers, testers, and stakeholders) has a shared understanding of what needs to be built.  
- **Improves Testability:** Helps QA teams design relevant test cases directly from business requirements.  
- **Prevents Scope Creep:** Keeps development focused on clearly defined outcomes.  
- **Enhances Quality Assurance:** Reduces ambiguity and helps identify edge cases early.  
- **Supports Agile Development:** Acts as a definition of “done” for each user story or feature.

---

### 🛒 Example: Acceptance Criteria for the Checkout Feature

**Feature:** Secure Checkout and Payment Processing for the Booking Management System  

| ID | Acceptance Criterion | Description |
|----|----------------------|--------------|
| AC-01 | User can access the checkout page | After selecting a property and booking dates, the user is redirected to the checkout page. |
| AC-02 | User can review booking details | The checkout page displays booking summary including property name, dates, number of guests, and total cost. |
| AC-03 | Payment gateway integration | The system integrates with a secure payment provider (e.g., Stripe, PayPal) to process transactions. |
| AC-04 | Validation of payment details | The system validates card or payment details before submission and displays appropriate error messages. |
| AC-05 | Confirmation on successful payment | The user receives an on-screen confirmation and a booking reference number. |
| AC-06 | Email notification | A confirmation email is sent to the user containing booking and payment details. |
| AC-07 | Failed payment handling | If the payment fails, the system provides a clear error message and allows the user to retry. |

---

## 🧰 Techniques & Tools

| Technique | Description |
|------------|--------------|
| **Interviews** | Direct discussions with stakeholders to capture expectations. |
| **Brainstorming** | Collaborative idea generation for potential features. |
| **Use Case Modeling** | Describes interactions between users and the system. |
| **Prototyping** | Visual models or mockups to clarify ambiguous requirements. |
| **Document Analysis** | Review existing materials or processes to extract needs. |

**Common Tools:**  
- JIRA / Trello — for tracking requirements  
- Lucidchart / Draw.io — for diagrams and flowcharts  
- Figma / Miro — for UI mockups  
- Google Docs / Confluence — for documentation and collaboration  

---

## 🧭 Best Practices

- Involve all key stakeholders early.  
- Avoid ambiguous terms like “user-friendly” — define measurable criteria.  
- Prioritize requirements (e.g., *Must Have*, *Should Have*, *Could Have*).  
- Maintain a **traceability matrix** to link requirements with design, code, and tests.  
- Review frequently as business goals evolve.

---

## 📚 References

- *Software Engineering: A Practitioner’s Approach* — Roger S. Pressman  
- IEEE Standard 830 — *Software Requirements Specification*  
- ALX ProDev Program — *Software Development Lifecycle Module*

---

> ✨ Authored by **Babatunde Omojuwa** —  
> *Aspiring Full-Stack Engineer | ALX ProDev Learner | Passionate about building meaningful digital experiences.*

