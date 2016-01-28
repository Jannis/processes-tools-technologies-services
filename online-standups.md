Note: This document is licensed under CC-BY-SA and was originally created by
Codethink Ltd. This is the original version.

--

Standing up
===========

We do standups to keep the team aware of what everyone is doing, and
to identify roadblocks. Doing them on IRC means we can

- log the minutes
- have remote participants
- be in more than one standup at once (eg Project Manager)

Standups should be short - approx 10 minutes. To make this happen 
attendees should have their minutes typed in advance, ready to cut
and paste.

Normally standups should be organised and run by **the engineers**, not the
project manager.  This is not to say that the project manager should not be
present; indeed they should be there.

Even projects involving one engineer working solo should create daily standup
minutes. Obviously this is not ideal and we should normally aim to ensure that
engineers are not working solo for long periods.  In this case, engineers may
be encouraged to simply email their standup notes to the internal project
mailing list instead.

To avoid wasting time, it is important for all participants to be prepared
ahead of time, and to not wait long for people who're present but not alert on
IRC. Wake them up with whatever means, or start the standup without
them. Otherwise a 10-minute standup may easily be preceded by a 15-minute wait
for everyone to be be awake on IRC.

Standups should be recorded in the project's log.  A good name for a standup
file would be standup-YYYYMMDD.mdwn in the log directory.  Don't forget to give
the standup a title and a date entry so that the log is kept in order.  All
engineers and managers associated with any given project should be capable of
running a standup, logging the activity and pushing standup minutes to the
project management wiki.

Performing a standup
--------------------

### Characters


* The Host
* The Engineers (Engineer 1, Engineer 2, Engineer 3)
* The Absent Engineers (Engineer 4)

### Notes

This script shows an example IRC standup, as performed at Codethink.
The format of the engineers' minutes may vary but the minutes posted
by everyone usually include the same things: done, doing, today/next,
issues/points.

The host drives the meeting, as follows:

* the host pings on IRC a short while in advance, eg 'standup in 17 minutes'
* engineers prepare their standup comments
* at the start time, the host asks engineers to indicate their presence
* the engineers participating in the meeting respond
* the host reports the order in which the engineers have responded as
  the order for posting their minutes
* engineers participating in the meeting post their minutes in the
  given order
  * the first engineer posts their name first, then their minutes, then
    the name of the next engineer (typically the first engineer's report
    will be that of the host themselves),
  * everyone else posts their sentences, ending with the name of the
    next engineer,
  * the last person ends by indicating that they is finished and
    that the discussion may begin
* the host drives the discussion by discussing the points raised in
  the minutes and anything that comes up during the discussion itself
  **CRITICALLY** the engineers should wait for the host to ask them to
  discuss any given point.  There should never be more than one point
  being discussed simultaneously.  Engineers may indicate a need to raise
  another discussion point by simply posting `_o/` to the channel (raising
  ones hand).
* the host should ensure actions are clearly identified, and assigned to
  named people, to follow up any issues which were raised but not fully
  resolved in the standup. If in doubt, the host should push actions to
  the project manager.

### Keep it short

Standups are supposed to be short. Avoid deep and long technical
discussions. Instead, decide to discuss them after the standup and
quickly agree a time, place and participants.

### Phrasing

The phrases used in this script are not set in stone, and may evolve
on specific projects. Some people use "meeting time, sound off" to ask
people to indicate their presence, others may prefer different phrasing.

### Raising hands during the discussion

A few emoticons that are commonly used to indicate someone has a point
or issue to raise in the discussion phase of standups:

    _o_ = nothing to say
    _o/ = I have something to discuss
    \o/ = Here! Here! Here! I have something urgent!

It's generally recommended to treat `\o/` like a regular `_o/`

An example standup
------------------

    <Host>        It's standup time everybody, please indicate your presence
    ... Host waits for people to say something ...
    <Engineer 3>  hi
    <Engineer 1>  here
    <Engineer 2>  hello
    ... Host waits some more, Engineer 4 is not responding ...
    <Host>        Is Engineer 4 working today?
    <Engineer 1>  No, he's off ill
    <Host>        Ok. Order: Host, Engineer 3, Engineer 1, Engineer 2
  <Host>        ## Lesley Engineeryface
    <Host>        * Done
                      - S6712: Get some cake made
                  * Today
                      - S6713: Eat some cake
                  ## Jon Smith
    <Engineer 3>  * Done
                      - S1234: Do this and that
                      - S4321: Do that other thing that needed to be done
                  * Today
                      - S5235: Debug this problem we're having
                      - S1235: Fix that bug in software X
                  * Points
                      - Hardware is dysfunctional, might need replacing
                  ## Flavia MacGrizzlie
    <Engineer 1>  * Done
                      - S5444: Build a system to deploy to the hardware
                      - S3311: Write some documentation for the customer
                      - A couple of meetings to discuss the next steps
                  * Today
                      - S4123: Write meeting report
                      - S1111: Document API for software X
    <Engineer 2>  ## Stewart Rod
                  * Done
                      - Nothing, had yesterday off
                  * Today
                      - S5930: Test functionality Y in software X
                  * Points
                      - I'm a bit short on tasks, can we do some planning?
                  # Discussion
    <Host>        Ok, we'll first discuss the points you've raised
    <Host>        Engineer 3, what are the problems with the board?
    <Engineer 3>  It randomly crashes, I'm suspecting damaged memory
    <Host>        Can you email me a summary of the problem so that I can
                  forward it to the customer to ask for a replacement?
    <Engineer 3>  Sure!
    <Host>        Engineer 2, unfortunately we have a tight schedule, so
                  we cannot do planning today. Please check with the
                  others about what you can do to help and we'll do some
                  planning tomorrow
    <Engineer 2>  Ok, no problem
    <Host>        Are there any other points to discuss?
    <Engineer 2>  o/
    <Engineer 3>  o/
    <Host>        Engineer 2, go ahead
    <Engineer 2>  I'm getting a haircut around lunchtime, so I might be
                  unavailable for about 1 1/2 hours
    <Host>        Ok, that shouldn't be a problem, just make sure nobody
                  is waiting for you on something
    <Engineer 2>  Will do
    <Host>        Engineer 3, your turn
    <Engineer 3>  This only just came to my mind: if we send my hardware
                  off to get a replacement, we only have a single board to
                  work with. That will impact our productivity. Can we get
                  some spares with the replacement perhaps to not have this
                  bottleneck again in the future?
    <Host>        I'll create a card for the Portia McManager to ask for that.
    <Host>        Anything else?
    ... Host waits 20-30 seconds ...
    <Host>        If not, I suggest we end the standup in 5
    ... Host waits 2 seconds ...
    <Host>        4
    ... Host waits 2 seconds ...
    <Host>        3
    ... Host waits 2 seconds ...
    <Host>        2
    ... Host waits 2 seconds ...
    <Host>        1
    ... Host waits 2 seconds ...
    <Host>        Meeting ends
    ... A few moments/minutes later ...
    <Host>        Meeting minutes uploaded: http://url/to/the/minutes
