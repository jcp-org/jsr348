## Introduction

This document describes proposed clarifications to the definitions of Membership within the Process Document. It is provided as a separate document in order to facilitiate the process of reviewing and providing comments within the issue-tracker. All comments on this document should be provided as comments to [JSR348-86:](http://java.net/jira/browse/JSR348-86) [Improve clarity of Member definition](http://java.net/jira/browse/JSR348-86). When we reach consensus, the agreed-upon changes will be documented in that and other issues as necessary.

## Goals

Clarify the different classes of membership, and identify the rights, privileges, and restrictions associated with them. Where possible, insert language to prevent an organization from gaming the system by enrolling its employees as individual members.

## Definitions

**Agent**: an individual - for example an employee, a contractor, or an officer - who is authorized to act on behalf of a company or organization.

NOTE: JUG members are not Agents.

**Java Community Process Member (Member):** A company, organization, or individual that has signed the JSPA and is abiding by its terms. In the case of an individual, that person may represent himself/herself, or may be an Agent of a company or organization.

NOTE: do we need the second sentence? There's a third case - the individual member may be both representing their own interests and may also be an Agent of a company or organization. Moreover, if he/she is an Agent, the company or organization may or may not be a member. It would be better not to get into all of these complications...

**Member Representative**: An Agent of a Member company or a Member organization who represents its interests within the JCP.

NOTE: there is no restriction on the number of Member Representatives from any company or organization. Member Representatives may join Expert Groups under the terms of the JSPA signed by the parent Member.

NOTE: as defined, a Member Representative may or may not be a Member in his/her own right.

**Member Associate**: An individual who is assoicated with a Member organization but is not an Agent of that organization.

NOTE: JUG members fall into this category. Current policy (unspecified in the Process Document) is that the PMO will require a signed Exhibit B before a Member Associate may join an Expert Group. However, this is legally insufficient, since such members are not and can not be bound by the JSPA signed by the parent organization. We really should require these people to join as individuals before allowing them to join an Expert Group. If we do so, then there's probably no need for this category of membership since strictly speaking it carries no privileges.

## **Restrictions**

During earlier discussion we proposed the following restrictions:

_**1) No more than three (or five) Agents of non-Members may join as individuals.**_

On legal advice, we will need to postpone any such restriction until JSR3, when we modify the JSPA.

_**2) Individual Members who are also Agents of Member organizations do not get separate votes in elections; only the Member organization gets a vote.**_

In section 6.4.2 ELECTION PROCESSES we should therefore say:

"All JCP Members are eligible to vote in ballots for Ratified and Elected Seats subject to the provisions that if a Member has majority-ownership of one or more other Members, or if one or more Members are Agents of another Member, then that group of Members will collectively have one vote, which will be cast by the person they designate to be their representative for the ballot in question."

_**3) Individual Members who are also Agents of Member organizations are not permitted to run in elections as individuals.**_

In section 6.4.4 SELECTION PROCESS FOR ELECTED SEATS we should therefore say:

"Any Member may nominate themselves except that Member Representatives who are also JCP Members in their own right cannot run for Elected Seats as individuals and the PMO shall reject such nominations."

## Discussion

This is a complicated subject, and until we modify the JSPA we're limited in what we can do. The minimal changes discussed above are all I believe we should implement.

**Lines 672-675**  

Change:  

"All JCP Members are eligible to vote in ballots for Ratified and Elected Seats subject to the provision that if a Member has majority-ownership of, or is the employer of, one or more other Members, then that group of Members will collectively have 1 vote, which will be cast by the person they designate to be their representative for the ballot in question.  

To:  

"All JCP Members are eligible to vote in ballots for Ratified and Elected Seats subject to the provisions that if a Member has majority-ownership of one or more other Members, or if one or more Members are Agents of another Member, then that group of Members will collectively have one vote, which will be cast by the person they designate to be their representative for the ballot in question."  

**Lines 698-699**  

Change:  

"except that employees of JCP Members cannot run for Elected Seats as individuals"  

To:  

"except that Agents of JCP Members cannot run for Elected Seats as individuals"