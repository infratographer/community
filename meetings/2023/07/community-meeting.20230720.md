# Infratographer Community Meeting 2023-07-20 @10:30am CT

[Zoom Link](https://us06web.zoom.us/j/88057942869?pwd=Vnd1OWplazFwREJQeWFHWks4MUptQT09)

## Agenda

* [ ] Welcome new members and guests
* [ ] Review previous meeting minutes
* [ ] Review project status
* [ ] SIG updates
* [ ] Open discussion

## Attendees

* @andy-v-h
* @nicolerenee
* @sfunkhouser
* @jnschaeffer
*

## Project Status

## SIG Updates

Updates from representatives of each SIG, as needed.

### SIG Bootstrap

* IPAM Becoming Network API
* Finalizers
* Lifecycle status tracking for objects

### SIG Identity

* Observability for permissions-related lifecycle events
* Synchronous permissions management
* Authorization for permissions-api

### SIG 2

## Open Discussion
* Use of [Watermill](https://watermill.io/) to stay event bus agnostic causing other challenges, such as the support `NackDelay`, `Request-Reply`, and keeping the full infratographer language agnostic (watermill locks pretty heavily into requiring the use of `go`).
* New `sig-events` created to work on addressing NATs + events open issues 
