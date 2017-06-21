## Introduction

This document describes proposed changes to the Final Release and Maintenance Release processes. It is provided as a separate document in order to facilitiate the process of reviewing and providing comments within the issue-tracker. All comments on this document should be provided as comments to [JSR348-70:](http://java.net/jira/browse/JSR348-70) [Simplify Maintenance Review process by eliminating Item Exception Ballot and Change Log](http://java.net/jira/browse/JSR348-70).

The contents of this document were agreed at the Working Group meeting on August 31, 2011\.

## Goals

The goals of these proposed changes are to simplify the Maintenance Release process by eliminating the Item Exception Ballot and Change Log, to harmonize the Maintenance and regular Release processes, to ensure that Maintenance Release artifacts (updated Spec, RI, and TCK) are delivered within a reasonable (finite) time, and to ensure that the Maintenance Release process remains relatively light-weight.

In proposing changes we should recognize the fundamental differences between the JSR development and Maintenance processes: while the former is subject to strict scrutiny by the EC, and can be halted if the Spec Lead fails to satisfy the EC, in the latter case the Maintenance Lead is paramount, and the EC can do no more than indicate that a particular proposed change should be postponed to a follow-on JSR rather than being included in the Maintenance Release.

## Discussion

The Issue Tracker is the mechanism that will allow us to simplify the Maintenance Release process and to harmonize it with the JSR development process. A formal process for dealing with potential "show-stopper" issues will provide us with the equivalent of an Item Exception Ballot, and allow us to apply the same process to all ballots.

We already state that JSR ballots by EC members may be a accompanied by comments. We should require that comments other than those of a general nature must explicitly reference Issues (maybe we should formally define this term.) So, for example, a member might vote 'no' with the comment "I'm willing to change my vote to 'yes' if you deal with issue #17 to my satisfaction" or alternatively, vote 'yes' with the comment "if you don't address issue #17 to my satisfaction I'm going to have to vote 'no' at the next ballot. (Obviously, the EC member will in some cases need to log the Issue.)  

The Public Review draft includes the following statements:

*   "all open issues must be responded to publicly before the JSR moves to the next stage"
*   "EC members, when voting to approve a JSR's advance to the next stage, should take into consideration the EG's responses to comments, and may insist that a suggestion or issue the EG considers resolved be re-addressed before the JSR moves on."

How can we implement these requirements in practice?

*   "Responding to" an issue might be as simple as saying "we think that's a dumb idea" or "we agree this is important and we'll address it later." Neither response is very helpful at the time it's given - only later will it become clear whether the issue has really been "resolved."
*   Does the second requirement require us to define an appeals process whereby issues deemed showstoppers are addressed to the satisfaction of the submitter? I think not...

Whatever process we define cannot allow one person to mark an issue as a show-stopper and insist that the JSR be halted or the MR abandoned unless it's addressed - that would give everybody veto power, and lead to deadlock. Instead, we need to align this mechanism with the existing voting process.

Do we need to do anything new, or can we simply provide a mechanism whereby issues can be flagged as problematic (in someone's opinion,) and require that EC members take these (and all issues) into consideration when voting? I think we can, if we require that Spec and Maintenance Leads provide a list of issues and their disposition when submitting materials for review. This would encourage them to address issues in advance, and permit EC members to focus on potential problem areas.

If the list of  issues is clearly visible to all, and EC members take it into consideration when voting, then we have the moral equivalent of an Item Exception process for all JSR ballots; if a majority of the relevant EC considers that one or more issues have't been dealt with appropriately they will vote 'no' and the Spec/Maintenance Lead will have to adjust the contents of the proposed Release until the EC is satisfied.

## Proposal

### **New defined terms**

_Issue tracker_: define the requirements, including the different states/categories that can be associated with an Issue - don't specify the actual tool that should be used. (We probably need to define a category indicating that an Issue the Spec Lead claims to have resolved has been 'challenged' or 'disputed' in order to flag this as something requiring special attention from the EC.)

_Issue_: an explicit reference to an item defined in an _Issue Tracker__._

_Issue List_: a list of all Issues that have been logged against the current Release, summarizing the EG's response to (disposition of) each. The Issue List must clearly specify all items that will be fixed in the proposed Release and those that have been deferred to a future Release. These and other categories of Issue (such as Issues the EG has closed as "non-issues") are specified in the definition of _Issue Tracker._

_Maintenance Renewal Ballot_: a ballot during which EC members vote on whether to permit a Maintenance Lead to extend the deadline for delivery of materials for Maintenance Release, or whether the previous Maintenance Review should be "rescinded" and the ML be required to start the process again. [Note: this is analogous to the _JSR Renewal Ballot_ that we've currently defined, but it's probably easier to define a new term than to generalize the other definition and process.]

### Requirements

When a Spec Lead or a Maintenance Lead submits materials for a JSR ballot they must provide an Issue List for EC members' consideration.

EC members must review the supplied Issue list and take it into consideration when casting their ballot. If they have any reservations or concerns about a 'yes' vote, or if they wish to vote 'no' they should accompany their ballot with comments which reference Issues (perhaps logged by them) that they would like to see addressed.

For example, during a JSR development ballot a member might vote 'no' with the comment "I'm willing to change my vote to 'yes' if you deal with issue #17 to my satisfaction" or alternatively, vote 'yes' with the comment "if you don't address issue #17 to my satisfaction I'm will vote 'no' at the next ballot. Similarly, during a Maintenance Review ballot an EC member might vote 'no' with the comment "the change proposed in issue #17 is not appropriate for a Maintenance Release and should be deferred to a follow-on JSR."

EC members should vote 'no' if they believe that the SL/ML has not adequately addressed all outstanding Issues. (Issues logged during the ballot process itself would either be addressed in a later Release submission, or if not, lead to a future 'no' vote.)

When materials are delivered to the PMO for a Maintenance Review the ML must provide an estimate of when the final materials will be delivered for the Maintenance Release. If no estimate is provided the deadline will default to 30 days. EG members should take this estimate into consideration when voting, and may vote 'no' if they consider the proposed Release date too far in the future. (EC members should bear in mind that many Maintenance Releases need to be synchronized with updates to a Platform, and that a Maintenance Review may therefore need to be carried out signinficantly in advance of the propsed Release.)

NOTE: need to define a process for the PMO to gather information from SL/ML and pass it on to the EC for consideration during the ballot.

If the Maintenance Lead fails to deliver the final materials as promised, a Maintenance Renewal Ballot will be held to determine whether the deadline may be extended or whether the previous Maintenance Review should be "rescinded" and the ML required to go through another Maintenance Review/.

Maintenance Releases are different from regular Releases in the following ways:

*   'no' votes may only be cast for one of the following reasons - 'no' votes with any other justifcation will be rejected by the PMO
    *   an item the ML included in the list of proposed changes should be deferred to a follow-on JSR.
    *   the proposed date for the delivery of Maintenance Release materials is unreasonably far in the future.
    *   a change in license terms is unacceptable .
*   the ML can enter the Maintenance Review process any number of times.

## Analysis

Differences from current process:

No need for an Item Exception Ballot process.

No need for a Change Log (replaced by an Issue List.) Note, however, that we added requirements that the Change Log should also indicate changes to the license, the RI, and the TCK. These will now have to be provided to the PMO in an alternate form.

A majority of no votes will halt an MR even if each references a different issue. This is different from the current Item Exception process, but should be just as effective. The ML will adjust the contents and can come back as many times as they like until a majority is achieved. So, we're not looking for a majority to oppose an individual change (as we did with the Item Exception Ballot) but rather for a majority to oppose going forward because they believe that possibly different changes are inappropriate. This is a subtle change, but doesn't appear harmful.

If an ML fails to deliver the final materials within a 'reasonable' time the EC can vote to 'rescind' the previous Maintenance Review and require the ML to start the Maintenance Review process again.