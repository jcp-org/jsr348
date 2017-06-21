# JCP.next JSR1 list of proposed changes

_Updated June 10 2011_

## Documents to be modified

*   The Process Document
    *   Normative
*   The EC Members' Guide
    *   Create a normative _EC Standing Rules_ document from Appendix A of the Process Document and the currently non-normative EC Members Guide.
    *   This will be referenced from the Process Doc and will address issues such as:
        *   Meeting schedules, quorum requirements.
        *   Voting procedures.
        *   Publish EC meeting agenda in advance.
        *   Specify whether agenda items are for discussion or for action.
    *   NOTE: once created, this document will not require a new JSR to modify - instead this can be done by a vote of the ECs after a one-month review period.
*   The Spec Lead Guide
    *   Non-normative: referenced from Process Document

## Procedural issues

*   **When will the changes in the Process Document take effect?**
    *   The JSPA currently prohibits us from applying Process Document changes to JSRs that are in progress:
        *   "The Process is described on the JCP Web Site (at http:/jcp.org), and may be revised from time to time in accordance with terms set forth in the Process document, provided that no such revisions shall apply to any JSR that has already been approved for development."
        *   We may fix this in JSR2 but for now we'll need to apply _moral pressure_ to in-flight JSRs to adopt the new procedures.

## Categories

*   [Transparency](#Transparency)
*   [Participation](#Participation)
*   [Agility](#Agility)
*   [Facilitating the EC merge](#ECmerge)
*   [Cleanup](#Cleanup)

## <a name="Transparency" id="Transparency"></a>1.Transparency

### 1.1 Expert Group transparency

*   Draft language required for the Process Document_._ (Alex)
    *   <span class="highlight">1.1.1 All significant business must be carried out on public mailing lists. (Alex)</span>
        *   EG-private mailing list may be maintained for administrative matters.

*   <span class="highlight">1.1.2 Issues must be tracked through a publicly viewable issue tracking mechanism. (Alex)</span>
*   <span class="highlight">1.1.3 Expert Groups must respond publicly to all comments before JSRs can move to the next stage. (Alex)</span>
    *   We have language requiring comments to be published, but not requiring responses - this must be tightened up.
*   Given the existing structure of the document, this new language won't easily fit anywhere.
*   <span class="highlight">1.1.4 Add **_Section 0/General Procedures_** that apply to all of the subsequently-described stages, to avoid duplication.(Patrick)</span> **PROPOSAL SUBMITTED TO ALIAS**

### 1.2 Executive Committee transparency

*   Draft language required for Process Document changes.
    *   <span class="highlight">1.2.1 Address PMO/Oracle Legal review of license terms (currently undocumented). (Mike)</span>
    *   **Recommendation:**
        *   Oracle legal drafts an opinion - presents to EC **befor****e** the appropriate vote.
        *   What if the license is in clear violation (eg, Apache license for Spec license) and ECs vote to approve this?
            *   We'll face that problem if/when it occurs.
        *   <span class="highlight">TODO: Patrick to review this suggestion with legal.</span>
            *   Need an SLA to guarantee turnaround (no unreasonable delay.)

### 1.3 License transparency

*   We have draft language for Process Document changes.
    *   <span class="highlight">1.3.1 Require that when the license terms associated with a JSR are significantly changed from the previous release, this is explicitly called out. (Alex)</span>
        *   We should also require change logs for the RI and TCK. (Alex).

    *   Note that strictly speaking the change log does not list all changes "after Final Release" but only those since the previous release. We should therefore change "after Final Release" to "since the previous release."

    *   **Recommendation** - in the _Process Document_ change:
        *   **definition - Change Log**: An area accessible from the Spec Page that lists all changes made to the Specification after Final Release. There are three sections: PROPOSED (changes not yet made to the Specification), ACCEPTED (changes made), and DEFERRED (change items to be considered in a new JSR).
    *   To:
        *   **definition - Change Log**: An area accessible from the Spec Page that lists all changes made to the Specification, RI, TCK, and licenses since the previous release. There are six sections: PROPOSED (changes not yet made to the Specification), ACCEPTED (changes made to the Specification), DEFERRED (changes to be considered in a new JSR) and RI (changes made to the RI), TCK (changes made to the TCK) and LICENSING (changes to licensing terms.)

*   Draft language required for Process Document changes.
    *   <span class="highlight">1.3.2 All approved licenses must be offered "for ever." New (modified) licenses may also be offered subsequently. (Alex)</span>
        *   NOTE: requiring licensees to adopt the latest TCK when updating their product may force them to accept new and unreasonable terms.
            *   Under these conditions, they should be permitted to take the updated TCK on the original licensing terms.  

### 1.4 TCK transparency

*   Draft language required for _General Procedures_ section of the Process Document
    *   **Recommendations**
        *   <span class="highlight">1.4.1 Publish lists of compatible implementations so users can see who's compatible and (by implication) who's not. (Patrick)</span> **PROPOSAL SUBMITTED TO ALIAS**
            *   Spec Leads must submit to the PMO (quarterly, and at every Maintenance Release) a list of all devices/platforms that have been certified as compatible.
                *   The PMO will publish these lists on jcp.org (and will publicise their existence.)
        *   Emphasize the value of compatibility & the brand and the risks of using incompatible implementations.
            *   This is a marketing issue - cannot be solved by Process Doc change.
        *   <span class="highlight">1.4.2 TCK documentation must be publicly available. (Patrick)</span> **PROPOSAL SUBMITTED TO ALIAS**
        *   <span class="highlight">1.4.3 TCK User's Guide must include Compatibility Requirements. (Patrick)</span> **PROPOSAL SUBMITTED TO ALIAS**
    *   **Non-recommendations (reconsider these for JSR2)**

    *   Do not publish lists of incompatible implementations.
        *   This is legally risky, and unnecessary (the list of incompatible implementations can be derived from the list of compatible implementations.)
    *   Do not (yet) publish information about optional features that are implemented.
        *   This is too difficult to implement (what level of granularity would we choose?)
    *   Do not strengthen the TCK quality requirements (except for requiring Compatibility Requirements)
        *   Better to police what we have now.
    *   Do not require more formal reporting requirements for conformance claims.
        *   Would require generalizing compatibility requirements.

    *   **TBD**
        *   Permit and encourage the discussion of individual TCK test results.
            *   We permit this now for OpenJDK testing - any value to generalizing to commercial testing?
                *   No value to discussing with the general public, but there may be value in discussing with the licensees' customers.

### 1.5 IP flow transparency

*   We have draft language for Process Document changes
    *   <span class="highlight">1.5.1 Review, clarify, expand the brief reference to anti-trust compliance. (Eduardo)</span> **PROPOSAL SUBMITTED TO ALIAS**
*   Draft language required for Process Document:
    *   <span class="highlight">1.5.2 Clarify _Terms of Use_ for collaboration software used by Expert Groups. (Patrick, John)</span>
        *   Should ensure sufficient IP grants, but not impose requirements more strict than the JSPA
        *   **Recommendation:**
            *   During the JSR submission process the Spec lead tells the PMO what collab software will be used.
            *   Oracle legal reviews the Terms Of Use and reports to the EC.
            *   EC approves, or requires an alternative.
                *   If OK - add to approved list. If not, look elsewhere
            *   We must ensure that java.net is on the _Approved List_.
            *   Must deal with possible changes to terms of use over time.
                *   May need to review each time, even if previously reviewed.
            *   TODO: Patrick to talk to Oracle Legal about this.
            *   We may need to delay to JSR2 because of the legal effort required.

## <a name="Participation" id="Participation"></a>2\. Participation

*   2.1 Draft language required for _EC Standing Rules_:
    *   <span class="highlight">2.1.1 Add semi-annual EC teleconferences that all JCP members are free to attend and where the agenda is chosen from topics suggested by the membership. (Eduardo)</span> **PROPOSAL SUBMITTED TO ALIAS**
    *   <span class="highlight">2.1.2 Hold an annual open meeting at JavaOne. (Eduardo)</span> **PROPOSAL SUBMITTED TO ALIAS**
    *   <span class="highlight">2.1.3 Create a public alias (with archive) for members to provide feedback to the ECs. (Eduardo)</span> **PROPOSAL SUBMITTED TO ALIAS**
*   2.2 Draft language required for Process Document:
    *   <span class="highlight">2.2.1 No barriers to participation in Expert Groups. (Eduardo)</span> **PROPOSAL SUBMITTED TO ALIAS**
        *   Requests to join EGs and the Spec Lead's responses, and decisions to remove or replace EG members, must be made in public.
    *   <span class="highlight">2.2.2 Uncooperative or Unresponsive Expert Group members. (Eduardo)</span> **PROPOSAL SUBMITTED TO ALIAS**
        *   2/3 majority of the EG can vote out an EG member (the company, or the person representing that company.)
            *   EG members should make a reasonable effort to resolve any such issues among themselves, for example by asking the member company to replace the representative.
                *   NOTE: this paragraph is buggy - switches to Spec Lead in the middle. Duplicate it so we have one section dealing with Spec Leads and one with EG members..
    *   <span class="highlight">2.2.3 Uncooperative, Unresponsive, or Inactive Spec Lead. (Eduardo)</span> **PROPOSAL SUBMITTED TO ALIAS**
        *   2/3 of EG can vote to refer a problem to the PMO. The PMO may ask the Spec Lead organization to replace the Spec Lead (individual) or to seek an alternative Spec Lead.
            *   If seeking an alternative Spec Lead, make sure this syncs with the _Transfer Ballot_ language.
    *   <span class="highlight">2.2.4 Individual members' votes - how to avoid ballot-stuffing? (Eduardo)</span> **PROPOSAL SUBMITTED TO ALIAS**
        *   **Recommendation:**
            *   Change this language in the Process Doc: "All JCP Members are eligible to vote in a ratification ballot subject to the provision that if a Member has majority-ownership of one or more other Members, then that group of Members will collectively have 1 vote." to “...has majority-ownership of or is the employer of one or more other Members...”
                *   NOTE: this doesn't deal with the JUG/JUG-member relationship. We think that's OK.
                *   It might be difficult for the PMO to enforce this in practice, but we would have the authority to do so if necessary or to take corrective action after the fact.
        *   <span class="highlight">2.2.5 Need similar language to clarify that employees of EC members are ineligible to run for election as individuals. (Eduardo)</span> **PROPOSAL SUBMITTED TO ALIAS**
*   2.3 Draft language required for EC Standing Rules:
    *   <span class="highlight">2.3.1 Penalties for EC members who do not attend meetings. (Eduardo)</span> **PROPOSAL SUBMITTED TO ALIAS**
        *   Miss two meetings in a row - lose voting privileges until you have attended two in a row.
            *   Non-voting members don't count towards quorum.
                *   Make sure we distinguish between voting and non-voting members elsewhere in the document.
            *   EC may waive this penalty under exceptional circumstances.
        *   Miss 6 meetings in a row (or 5, or 4?) and you lose your seat.
            *   EC may waive this penalty under exceptional circumstances.
        *   NOTE: we may want to consider attendance at f2f meetings separately from attendance at teleconferences.
            *   Does joining for a few hours by phone count as "attending" a f2f meeting?
        *   Need regular reports from the PMO to the EC and warnings to those who approach the limits.
    *   <span class="highlight">2.3.2 Penalties for EC members who don't vote?</span> <span class="highlight">(Eduardo)</span> **PROPOSAL SUBMITTED TO ALIAS**
        *   Can't take away voting privileges. We could expel from EC in extreme cases. (But if people aren't voting they're probably not attending meetings either...)

## <a name="Agility" id="Agility"></a>3\. Agility

*   We have draft language for Process Document:
    *   <span class="highlight">3.1 Time-outs for inactive JSRs. (Scott)</span>
        *   See _JSR Renewal Ballot_ suggestion from JSR 306.
            *   Reduce the numbers: 12 months to Early Draft, 2 years to Public Draft Review, 3 years to Final Release.
            *   Make sure this is sync'd with the _Dormant JSR_ language.
*   Draft language required for Process Document:
    *   <span class="highlight">3.2 Clarify the Maintenance process. (Scott)</span>
        *   Spec Leads want the EG to persist after Final Release. The Process Doc states that the EG must disband.
        *   This was presumably to ensure that IP vests in a clean manner. Need legal confirmation
        *   **Recommendation:**
            *   The _Expert Group_ must shut down and be re-formed at each release.
                *   Spec-lead will typically recruit from the previous EG, perhaps adding some new members.
            *   We need to maintain the history of which members have been on the EG between its most recent re-formation and the next release.
                *   These are the members who have potentially contributed IP.
            *   Need legal check on this, but hopefully we can complete this for JSR1\.

*   <span class="highlight">3.3 Clean up Maintenance Release requirements. Currently there's no absolute requirement for the Maintenance Lead to actually deliver an updated spec, RI, and TCK. (Scott)</span>
    *   The process simply says "the maintenance changes will be considered final when the RI and TCK are synchronized with the Specification."
    *   We should require a formal **_Maintenance Release_** just as we do a Final Release.
    *   What should the process be?
        *   For Maintenance Review we get a change log, an updated (supposedly-final) Spec, an updated RI and TCK if necessary (or a statement explaining why these aren't necessary.)
        *   We post these for review.
        *   At the end of the review period, if no objections by EC, approval is automatic.
            *   If there are objections, an exception ballot is held.
        *   Alternatively, should we get rid of the exception ballot process and always require an approval ballot, just as we do with Final Releases?
            *   **Recommendation: yes**
            *   We could then harmonize the two processes (JSR development/release and Maintenance)
*   <span class="highlight">3.4 Clarify requirements for RI and TCK to be posted within x weeks of Final Release and **_Maintenance Release_**. (Scott)</span>
    *   We post the Spec, but never the RI and TCK. We get a URL.
    *   When we get a working URL the state becomes "final" - IP vests at this point.
    *   What if the URL is later broken - becomes non-functional?
        *   PMO gives Spec/Maintenance lead 30 days to fix.
        *   If no fix, revert to Proposed Final Draft or Maintenance Review stage; must complete the process again.  

## <a name="ECmerge" id="ECmerge"></a>4\. Facilitating the EC merge

<span class="highlight">4.1 Take out of the Process Doc the definition of two ECs to simplify the process of merging the ECs later. (Put this into the Standing Rules.) (Mike)</span>

## <a name="Cleanup" id="Cleanup"></a>5\. Cleanup

*   Process Document changes
    *   <span class="highlight">5.1 Remove Process Doc section 1.1.4 J2ME building blocks (Eduardo)</span> **PROPOSAL SUBMITTED TO ALIAS**

    *   <span class="highlight">5.2 Remove the ambiguity of the term _Spec Lead_ in the Process Doc (Eduardo)</span> **PROPOSAL SUBMITTED TO ALIAS**
        *   Sometimes it refers to the Member and sometimes to the person representing the Member and leading the EG.
        *   See Wayne Carr document for explanation.
    *   <span class="highlight">5.3 Correct typos and errors in Process Document. (All, ongoing.)</span>