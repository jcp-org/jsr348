# JCP.next.3 list of proposed changes

_Updated October 20 2011_

## Categories

*   [Transparency](#Transparency)
*   [Participation](#Participation)
*   [Agility](#Agility)
*   [IP flow](#IPflow)
*   [Licensing](#Licensing)
*   [Legal issues](#LegalIssues)
*   [Collaboration](#Collaboration)
*   [Fee structure](#Fees)
*   [Cleanup](#Cleanup)
*   [Other](#Other)

## <a name="Transparency" id="Transparency"></a>Transparency

### Expert Group transparency

*   Eliminate confidentiality language from the JSPA.
    *   We have draft language (from the JSR 306 draft)

### Executive Committee transparency

*   Oracle Legal's review of license terms.
*   (Overflow from JSR1 if necessary.)

### License transparency

*   (Overflow from JSR1 if necessary.)

### TCK transparency

*   **Changes discussed but not incorporated into JSR1**

*   Publish lists of incompatible implementations.
    *   This is legally risky, and unnecessary (the list of incompatible implementations can be derived from the list of compatible implementations.)
*   Publish information about optional features that are implemented.
    *   This would be difficult to implement (what level of granularity would we choose?)
*   Strengthen the TCK quality requirements
    *   Before we do, make sure we're effectively policing existing requirements
*   Require more formal reporting requirements for conformance claims.
    *   Would require generalizing compatibility requirements.

*   JSR 348 issue: [Remove TCK Non-compete clauses/language](http://java.net/jira/browse/JSR348-14) (permit competing test suites)

### IP flow transparency

*   (Overflow from JSR1 if necessary.)

## <a name="Participation" id="Participation"></a>Participation

*   Make the JSPA less intimidating by refactoring into three layers
    *   Simple Terms Of Use for non-members who wish to comment on specs in public forums.
    *   A simple membership agreement for those who want voting privileges and the right to serve on Expert Groups.
    *   The complexities of IP and compatibility obligations are required only for Spec Leads – factor these out into a separate agreement.
*   Clarify classes of membership. _Agents_ of commercial or non-profit organizations (those authorized to act on their behalf) and _Associates_ of non-profits (those who are not so authorized.)
    *   Restrict the number of _Agents_ of a particular non-member commercial organization?

## <a name="Agility" id="Agility"></a>Agility

*   Enable implementations before specs are finalized, to gain real-world experience.
    *   Must maintain compatibility.  

    *   See _Transplant JSR proposals_
    *   Must declare during JSR submission that this **is** a Transplant JSR or that it will become one if the JSR doesn't complete within 3 years.
        *   The "it will become one" addition is new - need to revise the existing language.
*   What to do if a Spec Lead fails to deliver on the obligation to license the RI and TCK after Final Release? (See [JSR348-94: Spec leads can end-of-life a Specification, withdraw licenses](http://java.net/jira/browse/JSR348-94).)
    *   Is the obligation to license "perpetual?" JSRs reach a natural "end of life." Is a Spec Lead obliged to provide a functional TCK 20 years after Final Release?
*   Do we need a formal Early Draft Review now that we have transparency requirements and EGs continuously publish work-in-progress? See [JSR348-121:](http://java.net/jira/browse/JSR348-121) [PMO should not be involved in Early Draft Review](http://java.net/jira/browse/JSR348-121)

## <a name="IPflow" id="IPflow"></a>IP flow

*   Non-assertion patent covenant.
    *   We have draft language. Patrick to circulate this and ask people to get their lawyers to comment
    *   May need to add wording to ensure that the non-assert promise transfers with IP ownership.
*   Address the requirement that Expert Groups are required to dissolve at Final Release. Many people don't understand why this is so.
    *   Because we haven't specified IP flow during the Maintenance process?
    *   See closed issue: [JSR348-21 -Expert groups must not be dispanded after final release](http://java.net/jira/browse/JSR348-21)
*   Should people be permitted to withdraw their IP grants? At any time?
    *   JSPA Section 4D D. _Withdrawal of Contributions due to Change in Announced License Terms_ says Yes.
    *   Review this language - make sure it's consistent with possibly-changed processes.
*   Fix potential issues with _JSPA Exhibit B_.
    *   Needs legal review
    *   TODO: Oracle to start this
    *   Others should feel free to offer suggestions.
    *   Clarify what is a "duly authorized representative of Employer."
        *   Replace "Employer" with "Assignee"
    *   Implementation issues:
        *   People change employers
            *   Require individuals to "re-confirm" their membership each year and at that point to confirm that the Exhibit B is still valid or submit a new one.
            *   PMO to require a current Exhibit B whenever an individual (or someone associated with a group where there is not an employer-employee relationship joins an EG.
        *   What about members of groups where there is no employer relationship?
            *   Eg JUG, research institution, university, open source community.

## <a name="Licensing" id="Licensing"></a>Licensing

*   Define a mandatory standard Spec License.
    *   TODO: Patrick to circulate the "recommended" Spec License for comments.
*   Recommend (but do not require) standard RI and TCK licenses.
    *   Provide separate templates for Independent (open source) and commercial implementors.
    *   TODO: Patrick to circulate examples for discussion

## <a name="LegalIssues" id="LegalIssues"></a>Legal issues

*   Clarifiy the JSPA as discussed within the EC.
    *   Members will be asked to sign the new/revised JSPA (resulting from JSR2) - some may insist on this clarification at that point.
    *   Modified JSPA should not grant rights to one player that others don't have.
*   Address the issue of where litigation should be located. California, or elsewhere?
    *   California is an obstacle to Brazilian state involvement.
    *   According to Java Champion Douglas Jenssen this is also an issue within the US. He has said in private mail: "The issue is a legal one, where do legal disputes between Sun/Oracle and a member -- whether individual, sponsored by his employer, or corporation -- get litigated. When I last met with the JCP, the answer was it has to be in California. No public institution such as a state university is going to agree to that, and many corporations will not agree either. Hence I was told there are no members from public universities, only from private ones that choose to agree."
    *   The JSPA says: "Any action related to this Agreement will be governed by California law, excluding [choice of law rules](http://en.wikipedia.org/wiki/Choice_of_law), provided, however that neither party has consented to the jurisdiction of any court located in the other party�s country of incorporation."

## <a name="Collaboration" id="Collaboration"></a>Collaboration

*   Changes to make it easier to collaborate with other standards-setting organizations
*   Incorporate the _Hybrid_ and _Transplant_ JSR proposals from JSR 306\. .,
    *   _Transplant JSRs_ (enable incorporation and standardization of work developed outside the JCP)
    *   _Hybrid JSRs_ (allowing non-Java implementations of a JSR's specification)

## <a name="Fees" id="Fees"></a>Fee structure

*   Modify cost structure (in JSPA) to permit PMO to charge a nominal fee for individuals if this should prove necessary.
    *   Eg, "fees for individuals are $250 per year... Fees may be waived at the discretion of the PMO."
*   Iincrease fees for commercial entities?
*   Explicitly place JUGs in the same category as individuals.

## <a name="Cleanup" id="Cleanup"></a>Cleanup

*   Phase-out the IEPA provisions (no longer used.)
    *   IEPA agreements never expire - we need to deal with this.
    *   Encourage existing IEPA members to "resign" or to become full members.
        *   There aren't very many of them, so hopefully the PMO can handle this.
    *   Remove references to IEPA from JSPA.
        *   Need legal approval for this.
*   Clarify that a binary RI must be released by Spec Lead.
*   Clarify role of Proposed Final Draft - it seems strange that there are no formal requirements surrounding this. Should there be a minimum review period, for example?

## <a name="Other" id="Other"></a>Other

*   **Governance**
    *   Create an _Architecture Council?_
        *   Council would gather input from implementors, developers, and users and to provide guidance to Platform Expert Groups on platform evolution in the interests of maintaining competitiveness, compatibility and relevance.
        *   The membership of this group should be primarily technical, and it must operate by consensus and through negotiation with the Platform Spec Leads.
        *   Possible deliverables for the Council:
            *   Yearly survey of the community
            *   Written responses to Platform JSRs.

## Procedural issues

*   **When will the changes in the JSPA take effect?**
    *   We can not require that an existing JSR be ruled by new version of the JSPA.
    *   Currently there is no requirement that members upgrade to the latest JSPA.
        *   Note that section 2B uses the term "expires" but it seems there is no way for a JSPA to expire (merely "terminate") - we should fix this,
    *   Will the new version be version 3 (containing significant legal changes?)
        *   Presumably yes - otherwise why make the effort to modify it?
        *   If so, we want people to upgrade - all members should be operating under similar IP grants.
    *   **Recommendation:**
        *   Specify a lengthy transition period (two years?) with a common deadline, allowing ample time for review.
        *   All new JSRs must adopt the latest JSPA. This implies that the Spec Lead and EG members must sign it when the JSR is submitted.
*   **The JSPA also forbids us from applying changes to JSRs that are in-progress**
    *   "The Process is described on the JCP Web Site (at http:/jcp.org), and may be revised from time to time in accordance with terms set forth in the Process document, provided that no such revisions shall apply to any JSR that has already been approved for development."
    *   **Recommendation:**
        *   Modify this language to give us the power to apply Process Doc changes to in-flight JSRs.
            *   This wouldn't require us to do so, just make it possible if we wish.
            *   The language should specify that at the EC's discretion some or all of the requirements of the Process Document will apply to all JSRs when they next make a formal state-change through the process