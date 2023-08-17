# Infratographer Community Meeting 2023-08-17 @10:30am CT

[Zoom Link](https://us06web.zoom.us/j/88057942869?pwd=Vnd1OWplazFwREJQeWFHWks4MUptQT09)

## Agenda

* [ ] Welcome new members and guests
* [ ] Review previous meeting minutes
* [ ] Review project status
* [ ] SIG updates
* [ ] Open discussion
* [ ] Review action items

## Attendees

* @andy-v-h
* @nicolerenee
* @sfunkhouser
*
*

## Project Status

## SIG Updates

Updates from representatives of each SIG, as needed.

### Virtual machines

Kicked off work on the VM SIG.  We have a few volunteers to help with the SIG.  We are working on the basics of the code bases. Design will roughly follow load balancers for now

### Compute

The initial work for server-api is kicking off for tracking bare metal servers.

### Events

Update on current state of events refactor.

As of [x@v0.3.5](https://github.com/infratographer/x/releases/tag/v0.3.5) the events package has been reworked to remove watermill and has been updated in a few of the services
[tenant-api](https://github.com/infratographer/tenant-api/pull/117)
[permissions-api](https://github.com/infratographer/permissions-api/pull/148)
[load-balancer-api](https://github.com/infratographer/load-balancer-api/pull/207)

Additionally with this change included the Auth Relationship Request / Reply events that should be used to create relationships between resources instead of change messages, which ensures proper permissions exist before any other service attempts to request these resources. (This is already handled for you by the x/entx event hooks template for many services).

## Open Discussion

## Action Items
