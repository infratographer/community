# Infratographer Community Meeting 2023-05-25 @10:30am CT

[Zoom Link](https://us06web.zoom.us/j/88057942869?pwd=Vnd1OWplazFwREJQeWFHWks4MUptQT09)

## Agenda

* [ ] Welcome new members and guests
* [ ] Review previous meeting minutes
<!-- WIP
* [ ] Review open issues and pull requests
* [ ] Review new issues and pull requests
* [ ] Review project board
-->
* [ ] Review project status
* [ ] SIG updates
* [ ] Open discussion
* [ ] Review action items

## Attendees

* @andy-v-h
* @nicolerenee
* @sfunkhouser
* @jnschaeffer
* @drewr
*
*
*

## Previous Meeting Minutes

* [YYYY-MM-DD]()

## Project Status

## SIG Updates

Updates from representatives of each SIG, as needed.

### Bootstrap

#### API Gateway

Started work on graphql schema validation on PRs. Example [PR output](https://github.com/infratographer/metadata-api/pull/26).
Supergraph "deployed" to [Apollo Studio](https://studio.apollographql.com/public/infratographer/variant/main/home). 

##### Generation

#### Interfaces

Bug around @interfaceObjects was found and [reported](https://github.com/apollographql/federation/issues/2590).

#### Demo / Web UI

### Identity

#### Predictable Subject IDs

Merged [PR #196](https://github.com/infratographer/identity-api/pull/169) in identity-api defining and implementing an algorithm for predictable subject ID generation during token exchange. However, some details warrant further discussion among the group.

#### Opaque Token Exchange

Discussed to some degree last week but there are situations where we want to accept opaque tokens from other services (possibly but not necessarily OAuth 2.0 providers). Current ideas include a JWT signing service that can be deployed in front of anything that responds to a request with an [OAuth 2.0 token introspection](https://www.rfc-editor.org/rfc/rfc7662#section-2.2) response to keep things generic.

## Open Discussion

## Action Items
