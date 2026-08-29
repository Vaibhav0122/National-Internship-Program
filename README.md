#  Movie Ticket Booking System

A **Pega-based Movie Ticket Booking application** developed using **Pega
App Studio** as part of the National Internship Program project.

The application automates the complete movie-ticket booking lifecycle
--- from submitting a ticket request and checking show availability to
calculating the booking cost, processing payment, allocating seats,
generating a confirmation number/ticket, and completing the booking.

------------------------------------------------------------------------

##  Project Overview

The **Movie Ticket Booking System** is designed to simplify and automate
movie/event ticket booking through a structured Pega workflow.

The system captures booking details, validates availability, calculates
the total booking cost, routes requests according to the selected show
type, processes payment, automatically allocates seats according to
ticket quantity, generates a confirmation number, and updates the
booking status.

------------------------------------------------------------------------

##  Objectives

-   Provide a structured workflow for movie ticket booking.
-   Capture and manage customer/attendee and event information.
-   Check show and seat availability before booking.
-   Calculate the total booking cost automatically.
-   Support different payment methods.
-   Route bookings based on show type.
-   Automatically allocate seats according to ticket quantity.
-   Generate a unique confirmation number after successful booking.
-   Generate and maintain ticket information.
-   Update booking status throughout the case lifecycle.
-   Provide a clear resolution/completion stage for completed bookings.

------------------------------------------------------------------------

##  Key Features

###  Ticket Request

Users can submit a movie ticket request with relevant booking
information such as:

-   Movie ticket request name
-   Attendee
-   Event name
-   Show date and time
-   Ticket quantity
-   Ticket price
-   Payment method
-   Discount code
-   Notes

###  Show Availability

The application checks the available seat count and show-related
information before proceeding with the booking.

###  Automatic Booking Cost Calculation

The total booking cost is calculated automatically based on:

**Total Booking Cost = Ticket Price × Ticket Quantity**

###  Conditional Booking Routing

Bookings can be routed to different work queues based on the selected
**Show Type**.

Example:

-   Premium → `PremiumShowQueue`
-   Standard → `StandardShowQueue`

###  Payment Processing

The booking workflow includes a payment-processing stage before final
ticket generation.

###  Automatic Seat Allocation

The system automatically allocates seats based on the requested **Ticket
Quantity**, rather than allocating only one seat.

###  Confirmation Number

After successful booking, the system generates a confirmation number
used for booking verification and tracking.

Example:

`CONF-M-2001`

###  Ticket Generation

After payment and seat allocation, the workflow generates the ticket
information.

###  Booking Status

The booking status is updated as the case progresses, including
confirmation and completion.

------------------------------------------------------------------------

##  Application Workflow

``` text
Submit Movie Ticket Request
            ↓
Check Show Availability
            ↓
Calculate Booking Cost
            ↓
Review Booking Details
            ↓
Confirm Booking Request
            ↓
Process Payment
            ↓
Allocate Seats
            ↓
Generate Ticket
            ↓
Update Booking Status
            ↓
Resolution / Completion
```

------------------------------------------------------------------------

##    Main Workflow Stages

### 1. Booking Request

The user enters the required movie/event and ticket information.

### 2. Availability Check

The application validates the availability of seats for the requested
show.

### 3. Booking Cost Calculation

The system calculates the total cost automatically using ticket price
and ticket quantity.

### 4. Booking Review & Approval

The booking details are reviewed before execution.

### 5. Booking Execution

The execution stage contains:

-   Process Payment
-   Allocate Seats
-   Generate Tickets
-   Update Booking Status

### 6. Resolution / Completion

After successful processing, the booking reaches the
resolution/completion stage.

------------------------------------------------------------------------

##  User Stories

The project is organized around the following user stories:

  ID       User Story
  -------- ----------------------------------
  US-001   Submit Movie Ticket Request
  US-002   Check Show Availability
  US-003   Calculate Booking Cost
  US-004   Confirm Booking Request
  US-005   Maintain Movie and Show Data
  US-006   Review Booking Details
  US-007   Process Payment
  US-008   Allocate Seats
  US-009   Generate Ticket
  US-010   Route Booking Based on Show Type

------------------------------------------------------------------------

##  Important Data Fields

Some of the important fields used in the application include:

  Field                       Purpose
  --------------------------- -------------------------------------------------
  Movie Ticket Request Name   Identifies the booking request
  Attendee                    Stores the person making/receiving the booking
  Event Name                  Stores the selected event/show
  Show Date and Time          Stores the scheduled show
  Ticket Price                Stores the price per ticket
  Ticket Quantity             Stores the number of tickets requested
  Total Booking Cost          Automatically calculated booking amount
  Available Seat Count        Represents available seats
  Seat Allocation             Stores automatically allocated seat information
  Payment Method              Stores the selected payment method
  Booking Status              Tracks the booking state
  Confirmation Number         Unique booking verification/tracking number
  Discount Code               Stores an applicable discount code
  Notes                       Stores additional booking information

------------------------------------------------------------------------

##  Technology Used

-   **Pega App Studio**
-   **Pega Platform**
-   **Pega Workflow Automation**
-   **GitHub** for project documentation and demonstration evidence

------------------------------------------------------------------------

##  Testing & Validation

The application was tested through the Pega preview/work portal to
validate the major booking functions.

Testing included:

-   Submitting a movie ticket request
-   Checking show availability
-   Verifying booking cost calculation
-   Confirming booking details
-   Processing payment
-   Verifying automatic seat allocation
-   Verifying confirmation number generation
-   Generating ticket information
-   Updating booking status
-   Testing conditional routing based on Show Type
-   Completing the booking case successfully

------------------------------------------------------------------------

##  Project Evidence

Screenshots demonstrating the application's configuration, workflow,
business logic, data fields, and successful case execution are included
in this repository.

The screenshots provide implementation evidence for the different user
stories and workflow stages.

------------------------------------------------------------------------

##  Repository Contents

``` text
National-Internship-Program/
│
├── README.md
├── MovieTicket_Vaibhav_Tiwari.docx
│
└── Screenshots/
    └── Project implementation and testing screenshots
```

> **Note:** The current repository also contains the uploaded project
> documentation and implementation screenshots. Additional files can be
> organized into folders as the project documentation is expanded.

------------------------------------------------------------------------

##  How the Booking Works

A typical successful booking follows this sequence:

1.  User submits a movie ticket request.
2.  Show information and availability are checked.
3.  Ticket price and quantity are used to calculate the total booking
    cost.
4.  Booking details are reviewed and confirmed.
5.  The request is routed according to the selected show type where
    applicable.
6.  Payment is processed.
7.  Required number of seats are automatically allocated.
8.  A confirmation number is generated.
9.  Ticket information is generated.
10. Booking status is updated.
11. The case reaches Resolution/Completion.

------------------------------------------------------------------------

##  Sample Successful Booking

Example of a successfully processed booking:

``` text
Movie Ticket Request : iron man
Ticket Quantity      : 5
Ticket Price         : US$25.00
Total Booking Cost   : US$125.00
Payment Method       : Credit Card
Seat Allocation      : Seat-1, Seat-2, Seat-3, Seat-4, Seat-5
Booking Status       : Confirmed
Confirmation Number : CONF-M-2001
```

------------------------------------------------------------------------

##  Demo

**Pega Application Demo:**\
*(https://xmyzg7ek.pegacea.net/prweb/app/movie-ticket-booking-Vaibhav-tiwari/)*

The demo should demonstrate the complete booking lifecycle, including
request submission, availability validation, cost calculation, booking
confirmation, payment processing, seat allocation, ticket generation,
and final resolution.

------------------------------------------------------------------------

##  Documentation

The project documentation and implementation evidence are available in
this repository.

For a better presentation, project screenshots should be organized under
a dedicated `Screenshots` folder and supporting documentation under a
`Documentation` folder.

------------------------------------------------------------------------

##  Project

**Project:** Movie Ticket Booking System\
**Platform:** Pega App Studio\
**Project Program:** National Internship Program

------------------------------------------------------------------------

##  Conclusion

The Movie Ticket Booking System demonstrates how **Pega App Studio and
workflow automation** can be used to build a structured booking
solution.

The application brings together data management, conditional routing,
automated calculations, payment processing, seat allocation, ticket
generation, and case lifecycle management into a single workflow.

This project provides practical experience in designing and implementing
a business application using a low-code workflow automation platform.
