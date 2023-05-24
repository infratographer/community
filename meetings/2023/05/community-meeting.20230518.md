# Infratographer Community Meeting 2023-05-18 @10:30am CT

[Zoom Link](https://us06web.zoom.us/j/88057942869?pwd=Vnd1OWplazFwREJQeWFHWks4MUptQT09)

## Agenda

* [ ] Welcome new members and guests
* [ ] Review previous meeting minutes
<!-- WIP
* [ ] Review open issues and pull requests
* [ ] Review new issues and pull requests
-->
* [ ] Review project board
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
*
*
*

## Previous Meeting Minutes

2023-05-11

* [x] @andy-v-h to create a new doc for the next meeting
* [ ] @andy-v-h to move membership info to the website
* [x] @nicolerenee publish roadmap

## Project Status

## SIG Updates

Updates from representatives of each SIG, as needed.

### Community

#### Github

SIG Community discussed a handful of issues around community management. The SIG is working on a proposal for an endstate where org membership is not required to participate in contributions, but searching for a solution that will enable far more granular control over permissions. As we work through this, the intended workflow is to make a personal fork of the Infratographer repos, make changes there, and then submit a PR to the Infratographer repo. This will allow us to maintain a single source of truth for the Infratographer repos while allowing for more granular control over permissions. Generally speaking, we want to enable SIG Leaders to be able to manage their SIGs without having to be an org owner.

### Bootstrap

#### Interfaces

We are going to be using `@interfaceObject` to add functions to interfaces. This works really well in the testing, but we did find one important gotcha. A subgraph that defines an `@interfaceObject` can not implement any objects that implement that interface. 

Meaning tenant-api can't declare that a tenant has a parent resource owner since tenant implements resource owner. 

#### Examples

  * [ ] Make an example API that will show how an `example` node is added to the graph.
  * [ ] Make a lab-style repo that can be forked and worked through to learn how to work with `ent` and `gqlgen` and how to reference nodes as external attributes managed by another subgraph.

#### More cowbell

  * Complete components listed as a foundational piece of the project
  * Initial a release process for composing the supergraph

### SIG Make more SIGS

  * Identify SIGs that need to be created
    * Identify broad areas and narrow areas to specify SIGs around
    * Identify SIG Leaders
    * Lower priority

## Open Discussion

## Action Items

* [ ] @andy-v-h to move membership info to the website
