---
sip: 1
title: SIP Purpose and Guidelines
status: Implemented
author: SharedStake Community
created: 2021-02-18
updated: 2021-02-21
---

## What is a SIP?

SIP stands for SharedStake Improvement Proposal. Logging a SIP is the first step to ensure changes to SharedStake are transparent and well-governed. A SIP is a design document providing information to the SharedStake community about a proposed change to the system. The Author is responsible for building consensus within the community and documenting dissenting opinions.

## SIP Rationale

SIPs are the primary mechanisms for proposing new features, collecting community input on an issue, and for documenting the design decisions related to changes to SharedStake. They are maintained as text files in a versioned repository, so their revision history is the historical record of the feature proposal.

It is highly recommended that a single SIP contain a single key proposal or new idea. The more focused the SIP, the more successful it is likely to be.

A SIP must meet certain minimum criteria, it must be a clear and complete description of the proposed enhancement, and the enhancement must represent a net improvement.

## SIP Work Flow

Parties involved in the process are the _Author_, the [_SIP Editors_](#SIP-editors), and the SharedStake community.

:required: Before you begin, vet your idea to save time. Ask the SharedStake community first if an idea is original to avoid wasting time on something that will be rejected based on prior research (searching the Internet does not always do the trick). It also helps to confirm the idea is applicable to the entire community and not just the Author (the intended effect must be generalizable). The appropriate public forum to gauge interest around your SIP is [the unofficial SharedStake Discord] or [the unofficial SharedStake Telegram].

Your role as a SIP Champion is to write the SIP using the style and format described below, shepherd the discussions in the appropriate forums, and build community consensus around the idea. 

A successful SIP will follow this workflow:

```
Proposed -> Approved -> Implemented
  ^                     |
  +----> Rejected       +----> Moribund
  |
  +----> Withdrawn
  v
Deferred
```

Each status change is requested by the SIP Author and reviewed by the SIP Editors. Use a pull request to update the status. Please include a link to the SIP's discussion. The SIP Editors will process these requests as per the conditions below.

- **Proposed** If agreeable, the SIP Editor will assign the SIP a number (generally the issue or PR number related to the SIP) and merge your pull request. The SIP Editor will not unreasonably deny a SIP. Proposed SIPs will be discussed on governance calls and in Discord. If there is a reasonable level of consensus around the change on the governance call the change will be moved to Approved. If the change is contentious a vote of token holders may be held to resolve the issue or approval may be delayed until consensus is reached.
- **Approved** -- This SIP has passed community governance and is now being prioritised for development.
- **Implemented** -- This SIP has been implemented and deployed to mainnet.
- **Rejected** -- This SIP has failed to reach community consensus.
- **Withdrawn** -- This SIP has been withdrawn by the Author(s).
- **Deferred** -- This SIP is pending another SIP/additional change that should be bundled with it.
- **Moribund** -- This SIP has been implemented. It is now obsolete and requires no explicit replacement.

## What belongs in a successful SIP?

Each SIP should have the following parts:

- Preamble - RFC 822 style headers containing metadata about the SIP, including the SIP number, a short descriptive title (limited to a maximum of 44 characters), and the Author details.
- Simple Summary - “If you can’t explain it simply, you don’t understand it well enough.” Provide a simplified and layman-accessible explanation of the SIP.
- Abstract - a short (~200 word) description of the technical issue being addressed.
- Motivation (\*optional) - The motivation is critical for SIPs that want to change SharedStake. It should clearly explain why the existing specification is inadequate to address the problem that the SIP solves. SIP submissions without sufficient motivation may be rejected outright.
- Specification - The technical specification should describe the syntax and semantics of any new feature.
- Rationale - The rationale fleshes out the specification by describing what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work (e.g. how the feature is supported in other languages). The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.
- Test Cases - Test cases may be added during the implementation phase and are required before implementation.
- Copyright Waiver - All SIPs must be in the public domain. See the bottom of this SIP for an example copyright waiver.

## SIP Formats and Templates

SIPs should be written in [markdown] format.
Image files should be included in a subdirectory of the `assets` folder for that SIP as follows: `assets/SIP-X` (for SIP **X**). When linking to an image in the SIP, use relative links such as `../assets/sip-X/image.png`.

## SIP Header Preamble

Each SIP must begin with an [RFC 822](https://www.ietf.org/rfc/rfc822.txt) style header preamble, preceded and followed by three hyphens (`---`). This header is also termed ["front matter" by Jekyll](https://jekyllrb.com/docs/front-matter/). The headers must appear in the following order. Headers marked with "\*" are optional and are described below. All other headers are required.

`SIP:` <SIP number> (this is determined by the SIP Editor)

`title:` <SIP title>

`author:` <a list of author name(s) and/or username(s), or name(s) and email(s). Details are below.>

`* discussions-to:` \<a url pointing to the official discussion thread at gov.SharedStake.finance\>

`status:` < PROPOSED | APPROVED | IMPLEMENTED >

`created:` <date created on>

`* updated:` <comma separated list of dates>

`* requires:` <SIP number(s)>

`* resolution:` \<a url pointing to the resolution of this SIP\>

Headers that permit lists must separate elements with commas.

Headers requiring dates will always do so in the format of ISO 8601 (yyyy-mm-dd).

#### `author` header

The `author` header optionally lists the names, email addresses or usernames of the Authors/owners of the SIP. Those who prefer anonymity may use a username only, or a first name and a username. The format of the Author header value must be:

> Random J. User &lt;address@dom.ain&gt;

or

> Random J. User (@username)

if the email address or GitHub username is included, and

> Random J. User

if the email address is not given.

#### `created` header

The `created` header records the date that the SIP was assigned a number. Both headers should be in yyyy-mm-dd format, e.g. 2001-08-14.

#### `updated` header

The `updated` header records the date(s) when the SIP was updated with substantial changes. This header is only valid for SIPs in Draft and Active status.

#### `requires` header

SIPs may have a `requires` header, indicating the SIP number(s) that this SIP depends on.

## Auxiliary Files

SIPs may include auxiliary files such as diagrams. Such files must be named SIP-XXXX-Y.ext, where “XXXX” is the SIP number, “Y” is a serial number (starting at 1), and “ext” is replaced by the actual file extension (e.g. “png”).

## SIP Editors

The current SIP Editors are:

`* none`

## SIP Editor Responsibilities

For each new SIP that comes in, an Editor will do the following:

- Confirm the SIP is ready: sound and complete. The ideas must make technical sense, even if they don't seem likely to get to final status.
- Verify the title accurately describes the content.
- Check the SIP for language (spelling, grammar, sentence structure, etc.), markup (Github flavored Markdown), code style

If the SIP isn't ready, the Editor will send it back to the Author for revision, with specific instructions.

Once the SIP is ready for the repository, the SIP Editor will:

- Assign a SIP number (generally the PR number or, if preferred by the Author, the Issue # if there was discussion in the Issues section of the repository about this SIP)

- Merge the corresponding pull request

- Send a message to the SIP Author with the next step.

The SIP Editors monitor SIP changes and correct any structure, grammar, spelling, or markup mistakes.

The Editors perform administrative & editorial tasks. They do not pass judgment on SIPs.

## History

The SIP document has been adapted from the YIP (Yearn Improvement Proposal), which was heavily derived from the Synthetix Improvement Proposal document. In many places, open source text was simply copied and modified. Any comments about the SIP document should be directed to the SIP Editors.

### Bibliography

[markdown]: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet

## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
