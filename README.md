Incoming Mobilities API
=======================

* [What is the status of this document?][statuses]
* [See the index of all other EWP Specifications][develhub]


Summary
-------

This document describes the **Incoming Mobilities API**. This API is
implemented by the receiving institution. It allows the sending HEI to read the
receiving HEI's "part" of the information related to the sending HEIs outgoing
mobilities. (From the receiving HEI's perspective, these are the incoming
mobilities.)

Currently, this API describes mobilities **of one type only** - *Student
Mobilities for Studies*. More types MAY be added in the future.


Reminder on vocabulary
----------------------

Keep in mind that definitions of "sending HEI" and "receiving HEI" come from
the "mobility vocabulary", not the "HTTP vocabulary". In case of this
particular API this means that:

* **sending HEI == requesting HEI** (HEI which is sending the student == HEI
  which implements the client, and *sends* the HTTP request),
* **receiving HEI == responding HEI** (HEI which is receiving the student ==
  HEI which implements the API, *receives* the HTTP request, and responds to
  it).

As long as we use these terms consistently, there shouldn't be much confusion
though.


Security
--------

This version of this API uses [standard EWP Authentication and Security,
Version 2][sec-v2]. Server implementers choose which security methods they
support by declaring them in their Manifest API entry.

This API handles data which is considered private. Server implementers are
allowed to forbid less-secure methods of authentication and encryption for this
API (by dropping support for them). Currently, we leave it for the server
implementers to decide which methods are "secure enough". These recommendations
MAY change in the future.


Endpoints to be implemented
---------------------------

Server implementers MUST:

 * Implement the [`get` endpoint](endpoints/get.md).
 * Put the URL of this endpoint in their [manifest file][discovery-api], as
   described in [manifest-entry.xsd](manifest-entry.xsd).

The details on each of these endpoints are described on separate pages of this
API specification (use the links above).


[develhub]: http://developers.erasmuswithoutpaper.eu/
[statuses]: https://github.com/erasmus-without-paper/ewp-specs-management#statuses
[registry-spec]: https://github.com/erasmus-without-paper/ewp-specs-api-registry
[discovery-api]: https://github.com/erasmus-without-paper/ewp-specs-api-discovery
[echo]: https://github.com/erasmus-without-paper/ewp-specs-api-echo
[error-handling]: https://github.com/erasmus-without-paper/ewp-specs-architecture#error-handling
[institutions-api]: https://github.com/erasmus-without-paper/ewp-specs-api-institutions
[sec-v2]: https://github.com/erasmus-without-paper/ewp-specs-sec-intro/tree/stable-v2
