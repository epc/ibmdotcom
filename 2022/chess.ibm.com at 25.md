Twenty five years ago “Deep Blue” “beat” Garry Kasparov in Game 6 of “Deep Blue vs. Kasparov: The Rematch”.  I’ve read many opinions over the years about the meaning of the victory for AI and the human vs. machine competition.  There’s been very little written about the web site, chess.ibm.com, which alternated between running fine, and crashing as soon as a match would start.  I should know, I was the “webmaster” for chess.ibm.com.

By December 1995 I was the so–called “Corporate Webmaster” for IBM.  It was an entirely made–up title I created to describe the pile of responsibilities I had, ranging from technical operations of www.ibm.com, to being the guy everyone (inside IBM) called to complain about some aspect of IBM’s web presence, to being the guy who had to bless (or reject) every web site that wanted to be part of the IBM “web”.
chess.ibm.park.org
I was called into a meeting with a variety of people to weigh in on the upcoming Kasparov vs. Deep Blue ACM Chess Challenge.  The details are fuzzy now but as I recall someone brought up that IBM should host a web site for the match and that it should be part of the 1996 Internet World’s Fair (www.park.org) with the URL chess.ibm.park.org.

There was no question of us hosting it, we couldn’t.  At the time ibm.com ran on a pair of small RS/6000 servers which themselves weren’t dedicated to ibm.com and hosted other customers of Advantis (IBM’s networking company co–owned with Sears).  So the decision was made to outsource the hosting to a third party hosting provider out of Boston.  The content would be developed by an agency, with IBM providing some editorial and management support.  My role in chess.ibm.park.org was basically non–existent, and I was more focused on helping with the upcoming Australian Open web site which IBM was hosting on our shared infrastructure.

When the match started in February 1996 the web site crashed almost immediately.  The web site became a huge fiasco and embarrassment for IBM and for my team even though we (in theory) had zero direct responsibility for the hosting.  The guys from the Olympics team down the hall from us in Armonk dove in to help and over a couple of days they moved the site from the third party provider to an SP1 rack somewhere in an Advantis hosting center in White Plains, NY.  My contribution to the effort was to surreptitiously “borrow” eight RS/6000 SP “wide” nodes from Poughkeepsie and drive them to White Plains in my 1990 Sunbird (which was worth less than a single one of the nodes).

The Olympics guys managed to save our collective faces over the remaining games.  The web site still had issues, the hosting center in White Plains wasn’t exactly well sited on the network for hosting an event web site.  But we eked out a…draw.

Afterwards, inside IBM there were many recriminations and many meetings.  Many FOILS presentations were put together and a few Freelance Graphics ones as well (we’d just acquired Lotus the previous year).  The net outcome of the fairly disastrous experience was that the Olympics team reworked and rearchitected their plans for hosting the 1996 Atlanta Olympic Games web site, and I was told to figure out how to design and build some sort of hosting complex for IBM corporate events and www.ibm.com.

I didn’t want to be a webmaster…
I feel like I should stop here for a moment and explain how I ended up in this role. I was an English major in college, minoring in Comp Sci at Allegheny College.  In utter fear of entering the real world I went to grad school at Carnegie Mellon for a Master’s in English as well, focusing on “professional writing”.  I interned at IBM in 1990 and returned as a Junior Information Developer in 1991, working on documentation for MVS/ESA and an internal software development environment.

At no time did I study to be a webmaster, corporate webmaster, or CTO.

To be honest, I was a rather mediocre technical writer.  I got the job done, but I didn’t find particular joy in it.  I was absolutely fascinated by the Internet though.

As an intern I was one of the first IBM employees to get an internet email address, costello@pokvmcr3.vnet.ibm.com.  In short order I became one of the denizens of the internal “INTERNET FORUM” answering questions about how to decipher addresses like oncoast!sir-alan!costello into internet addressable addresses.  On returning to IBM in 1991 I dove into the TCP/IP toolkit for OS/2, eventually writing some internal tools and becoming an unexpected expert on sendmail.cf configurations for OS/2 (and eventually AIX).

In 1993 I set up an internal gopher server, toolsinc.mcl.ibm.com, serving a hodgepodge of documentation and the daily Dilbert. A colleague and I worked together to “publish” some MVS documentation online using one of the few IBM gopher servers.

By 1994 I annoyed enough people that “internet stuff” was more or less a formal part of my responsibilities, eventually launching a divisional web server (lscftp.kgn.ibm.com).

In December 1994 I joined IBM Corporate Communications, initially on a temporary assignment, as “the HTML guy”.

Again, zero training to be a webmaster, Corporate Webmaster, large scale web site architect, etc.  Not that there was any such training to be had.

The biggest “event” site I had dealt with prior to Deep Blue was when IBM launched a hostile takeover of Lotus Development Corporation in June 1995.  I had to ask that the server running www.ibm.com be rebooted at 4:00 a.m. because the version of AIX it was running had a hard limit on TCP connections and I thought we might hit it that day.

If I recall correctly…we had the single biggest day of traffic I’d seen on www.ibm.com to date, over 100,000 hits. Yes, we still valued hits, not page views, nor visitors, in June 1995.

Back to 1996…through processes I wasn’t particularly aware of, funding was secured to “buy” an IBM RS/6000 SP complex for me to run www.ibm.com and IBM Corporate events on.  The RS/6000 SP was IBM’s brand for supercomputers. The Atlanta Olympic Games web site was architected around the SP and there was a growing set of skills within Advantis (again, then an IBM–Sears Joint Venture) to manage RS/6000 SP complexes.

In June 1996 the first SP complex was up and running, in Advantis’ facilities in Schaumburg, IL.  It consisted of 8 66Mhz “wide” nodes and assorted support servers.  We used the Andrew File Server (AFS) to serve content across the nodes and eventually to the second complex in Columbus, OH.

Neither complex was particularly well positioned on the Internet, though the Schaumburg complex was “close” to a peering facility in Chicago.

Content was served through AFS.  Surprisingly we didn’t have an IBM DB2 database server set up, partly because due to weird IBM/Advantis cross-company policies I couldn’t actually get a commercial license to use IBM’s DB2 for AIX on IBM’s RS/6000 SP servers because they were managed by Advantis and “owned” by IBM Commercial Credit Corp.  

We used a custom build of NCSA httpd 1.3 for serving www.ibm.com at that point. IBM had a web server product, Lotus Go Webserver. But we’d found it utterly failed to stay up on www.ibm.com. It had been designed around utilizing plug–ins, not CGI scripts, and froze more or less any time it had to run a CGI script.

By mid–1996 we knew there would be a second Deep Blue vs. Kasparov Match, some time in April or May 1997.  This time I would be involved from the start, responsible for architecting the site from scratch while working with various vendors who developed the content and a Java applet that would serve the game in near real time.  I was even granted a small budget to hire someone to handle the day to day work.

We also knew that we, IBM Corporate Web Programs, would be moving.  IBM had decided to build a new corporate headquarters, either in Armonk or in Greenwich Connecticut (the difference being about 1500 feet).  And we, the “internet people” were unwelcome in the new building, and more or less offered the chance to be moved out of the old headquarters (now IBM North Castle).

1996 is probably better known as the year of the Atlanta Olympic Games and IBM’s web site, www.atlanta.olympic.org.  I had little officially to do with the web site, and yet ended up being a very public face of the web site to officials from ACOG, the IOC, and IBM as I got tasked with running www.ibm.com and IBM’s web from inside the Olympic Technology Center.  IBM had a lot of problems with the Atlanta Olympic Games and I don’t think it’s my story to tell.

Post Olympics we started running other sports events on what regrettably became known as the “EdPlex”, my RS/6000 SP complexes in Schaumburg and Columbus, to differentiate from the Olympic team’s “WomPlex”.  We felt like we were getting into a rhythm and as we saw traffic increasing ended up adding more nodes to the “EdPlex”, this time PowerPC “high” nodes.

In theory the high nodes were to be much, much better than the existing servers, they had multiple processors, much more memory, and were faster than the 66Mhz wide nodes.

In practice they became a sort of nightmare to utilize well.  I kept tweaking my NCSA httpd build to iron out problems we were experiencing running on the high nodes but could not understand why performance was so abysmal.  The NCSA build was performing just as badly as we’d experienced with the IBM Domino httpd previously.  We resorted to using them in a support role, running Lotus Notes / Domino servers, eventually we even ironed out the issues with using IBM DB2 for AIX on IBM RS/6000 SP systems, though I think that was done primarily by IBM buying out Sears’ ownership of Advantis and merging it into IBM Global Services.

All through 1996 the prospect of Deep Blue Ⅱ was just over the horizon.

But this time, this time would be different, we knew exactly what we were getting into.

The sports events we were hosting gave us a heads up on how the overall audience of the web was growing.

We knew going in to the event we’d have to use as much IBM technology and products as possible so we committed to using the IBM Lotus Domino Go Web Server (LDGW).  Even with its fatal flaw about CGIs.

I thought we had the perfect solution: there would be no CGI scripts.  At all.  None. The site would be static, served as much as possible from cache.  We’d carefully tune the headers to ensure that once you loaded the site you cached as much content as possible.  The Java Applet would be the primary tool for dynamic content.  We’d still update specific pages on the site, some times every minute, but they’d be served statically, not via a script or server plug–in.

We set up a series of tests for ourselves including migrating www.ibm.com to IBM Lotus Domino Go WebServer (yes, the name kept changing, these are not typos).  We’d migrate ibm.com first, in March 1997, and we’d run the masters.org web site on ’Go in April 1997.

That was the plan.
Redirect /IBM/Armonk /IBM/New York/55BroadSt
In December 1996 we rather abruptly moved out of IBM Corporate HQ to temporary offices at 55 Broad St in Manhattan.  What I mean by abrupt is that while we knew we were moving, we did not know that IBM Real Estate hadn’t really managed to acquire what we needed for the temporary offices, namely, Internet service.  Phone lines? Yes, we had several phone lines.  But no network links.  Furthermore, IBM Armonk decided to turn off our phones the Monday after we moved, so anyone trying to reach us via phone flat out couldn’t except through email.

Honestly, this was the start of the most productive four months of my career at IBM.  I could actually spend more than a few minutes reviewing and responding to the hundreds of emails I received every day.  I could even write code again.  Albeit everything we did within the IBM network had to be over 53 kilobit dialup.

Jean, one of my close assistants (I’m not naming names unless they tell me privately they’re ok with it) figured out how to get Internet service from one of the in–building ISPs.  She and I wired up the desks across our two offices (in opposite corners of 55 Broad St) with ethernet (quietly breaking IBM’s I/T rules about using Token Ring, not ethernet).  We learned how to drape a cable between the two offices and how to reconnect it when it would get severed every couple of weeks.

We trudged along migrating www.ibm.com to Domino Go (yes, yes, it changed names again, and I do not guarantee that I have the exact sequence of changes correct at this point).  We rewrote many of our applications to be server side plug–ins.  In parallel the Domino Go development team added a form of cgid so that we could use CGI scripts, albeit not nearly as straightforward as under NCSA/Apache httpd.

The chess.ibm.com web site was coming along.  Everyone across the IBMers, the people from Poppe.Tyson, and (I believe, someone can correct me if this is wrong) StudioArchetype did their bit to ensure that we’d have a slick but effectively static web site.  There’d be no changing of graphics during the event, and if possible, ever after launch.  New graphics would require new URLs, which was fine.  But getting everyone on the same page about intentionally focusing on the cacheability of the site was an ongoing challenge.
Escalate me, go ahead, escalate me!
The thing you learn inside a large corporation like IBM is…it takes a long time for people throughout the organization to learn about things going on.  As the date for the rematch approached, more and more organizations across IBM with more and more products wanted to “pitch in to help”.  And you end up spending more and more time not only saying “no” but saying “no” to higher and higher leveled executives.

So, at some point late in 1996 or early in 1997 I ended up meeting with senior executives from IBM’s Software Group where I was pressed to explain why I wasn’t using IBM’s premier software products like DB2, Lotus Notes, InfoMarket, or Domino Go WebServer.  Now, I was just a schmuck.  I wasn’t an executive, I wasn’t a senior manager, I was barely a Band 7 on IBM’s ladder.  So, I did not have a lot of clout, but I didn’t have a lot to lose either by being honest and, well, I honestly explained why none of those products, or several others, were being used on www.ibm.com, nor the various sports events sites, nor the upcoming Deep Blue web site with the exception of Domino Go.

This had a weird salutary effect.  I did not get fired.  IBM Software Group took over responsibility for running IBM’s search engine (another story for another time).  And a new urgency was given to the Lotus Domino Go WebServer development team to work with us to get the server to work on www.ibm.com, the sports sites, and www.chess.ibm.com.

Going into the meeting I’d already told the head of IBM Software Group that we were moving to Domino Go in March.  And, I felt confident that we could meet that commitment.  ibm.com was hovering between 1MM and 1.5MM hits/day having crested 1MM hits/day during the Summer Olympics, then dropping down and building back up over the magical one million hits/day line late in 1996.

So, working out of our temporary space on a weekend in March 1997 we flipped the switch and slowly moved nodes from my bastardized NCSA httpd build to the official IBM Web Server. And, it seemed to work? No catastrophic failures.  Weekend traffic was a lot lower than week day traffic so the real test would happen around 0900 UTC on the following Monday morning.

By this time I’d moved into Manhattan, changing a two hour commute from Poughkeepsie to a ten minute walk from Battery Park City to Wall Street.

So, when my pager started going off at 4:00 a.m. that Monday morning that www.ibm.com was down it wasn’t too difficult to walk over and get online (yes, I had dialup internet access at home, no, it wasn’t particularly useful for an outage).

All of the IBM Lotus Domino Go Web Server instances had died or were in a weird state of thinking they were serving traffic but not.  They’d accept connections and…just…stall.

So, having gone through this exercise multiple times since 1995 I had a script ready to revert to NCSA httpd and restart the site.

But we were stuck with trying to figure out what was going wrong.  We’d eliminated the CGI problem (so we thought), the few plug–in services we’d written were not the apparent cause of the hangs.

And, you know, a sense of dread slowly built up. In March 1996, www.ibm.com was mostly static, stale, content.  The homepage was dynamic, there were some other server side scripts, but most of the content, most of the requests, were against static data.  Images, text, etc.

It was a subset of what www.chess.ibm.com was, with the major exception that we had the server side plug–ins on www.ibm.com, and there were none planned for chess.ibm.com.

In a little over four weeks we were expecting far, far, far more traffic for the Deep Blue vs. Kasparov web site on the same complex, with the same web server and file systems, and, well, we had to work out a solution because it was too late to buy more equipment.

In a worst case scenario we could fall back onto my NCSA httpd build (you can still see traces of it as IBM/Planetwide on ancient web crawler sites).
Tiger Woods Plays Some Golf
The 61st Masters Golf Tournament started April 10, 1997.  IBM hosted the official tournament web site, www.masters.org.  While my team didn’t have a direct role in the sports sites, they still ran on the “EdPlex” and there was a lot of cross–team coordination and collaboration. At that point in time we typically only ran www.ibm.com on a few nodes in each complex, using round robin DNS to split traffic between complexes, and IBM’s Network Dispatcher to load balance across individual servers.

Hosting the 1997 Masters site was such a non–event I don’t think we did anything extraordinary to plan for it.

My team and I were busy planning not only for the Deep Blue rematch, we were also moving from our temporary offices on the 13th floor to the IBM office suite on the 27th floor of 55 Broad St.  Two weeks out from Deep Blue, we were moving offices again.  Fixing network glitches.  Re–adapting to the constraints of Token Ring networks since, as a now official IBM location, we were expected to use Token Ring again and not the ethernet we’d been using.

Anyway.  I don’t play golf.  It never appealed to me as a kid, and a long forgotten injury to my shoulder makes swinging a golf club painful enough that I’d just as soon avoid it.  Paul was running www.masters.org.  We were all hanging out on our IRC server (yes, IBM was using IRC, in 1997, at least the web nerds were).  And Paul was seeing something new.

Apparently Tiger Woods had turned pro the previous year, and this was his first Masters.  And everyone in the world apparently wanted to “watch” him play via the web site.  And we were utterly failing to keep up.  We quickly threw everything we had available, going from four nodes for the site to 16 across both complexes.  We threw in the “high” nodes which we’d generally avoided using for web servers.

It just kept tanking. Over, and over, and over again.  Paul flipped between my NCSA build, to an Apache build we threw together, to IBM Lotus Domino Go Web Server.

Nothing worked. The site would yoyo up and down all afternoon.  As soon as game play ended the site would return to nominal load and operations.

And, again, the Deep Blue vs Kasparov rematch was only a couple of weeks away.

And, just to be clear, Paul and I were probably the top two people doing “web stuff” at that point at IBM.  The guys who ran the Atlanta Olympics site had moved on to advanced technology development.  No one else inside IBM ran sites anywhere near as complex or with as much traffic as we did.

And we had no idea what to do.

It was somewhere after the Masters site debacle but before the Deep Blue match started that I pulled one of the few cards I had and more or less demanded that the IBM Lotus &etc; Web Server team spend some time with us. In New York.  Running www.ibm.com.  On Lotus Domino Go Web Server.  

I don’t remember the actual particulars of the request any more but believe it was one of the few times I called an IBM Senior Executive directly.  Because, again, I was just a Band 7 schmuck, you don’t just call the head of IBM Software Group if you’re a Band 7.

In short order, the guys (I know I keep using “guys” but, well, with the exception of my awesome staffer Jean, there were generally no women in any of these organizations, that I dealt with)…the guys were in New York.  We handed them the virtual keys to www.ibm.com and gave them access to our IRC chat while we headed into the onslaught of Deep Blue vs. Kasparov: The Rematch.

We just, we were not remotely ready for what was about to happen.

Deep Blue vs. Kasparov: The Rematch Pre–Game
In the four months leading up to the Deep Blue vs Kasparov match we moved offices twice, worked out of temporary offices with just phone lines, watched as an IBM organization who’d escalated us to take over running IBM’s public search utterly failed to do so, and had a minor security breach (one part of IBM “ethically” hacked into the “EdPlex” and notified me as IBM’s Corporate Webmaster to let me know, not knowing that they’d actually breached www.ibm.com; in parallel IBM Global Services called me to warn that someone was trying to breach www.ibm.com).  I had moved from commuting four hours a day between Poughkeepsie and Manhattan to walking ten minutes each way between Battery Park City and Wall Street.  And I managed to avoid being part of some sort of event on a Metro North train involving a man with a machete hidden in a newspaper in Beacon, NY.

My team at the time consisted of Jean, Adam, and Kapil as assistant “webmasters”. Bob was our I/T support guy. Albert had been added to help out with pretty much all technology issues related to the chess.ibm.com site and served to be my eyes and ears when I couldn’t be in two places at the same time.  Chet was a friend from IBM Research who camped out in our offices and would do things like port Java over a couple of days to new platforms just for kicks. There were many, many more people working on chess.ibm.com from the content side.  There were a couple of engineers from Poppe.Tyson who developed the Java application.  We had a couple of people on the Advantis/IBM Global Services side who were heads down working with us as well and I apologize for not remembering who specifically was working with us (Rosa or Shelia thank you where ever you are today and I’m sorry for the nightmare this turned out to be).

Tiger Woods’ performance at the 1997 Masters and the resulting impact on the www.masters.org web site was an eye opener.  I mean.  As much as I downplayed my background and experience earlier, we had every resource at our disposal to do this right, and even before the match started I knew we were in for a disaster.

And yet, IBM continued to surprise me by asking for more.  It wasn’t enough to move offices in the weeks before the match. Or to redo our networking and phones yet again in the week before the match.  Or to continue “running” IBM’s web presence, whatever that mean.

No, literally at the last minute we were told to host “Club Kasparov”.  An interactive web site developed by an IBM multimedia studio in conjunction with Garry Kasparov (so I am told, he may not have been directly involved).  Club Kasparov was developed completely independently of us, with zero understanding of the “EdPlex” hosting complexes or the peculiarities of of working across multiple nodes using AFS as the common filesystem.  And yeah, we were expected to just sort of drop it in on the site and host it.  For good measure I recall there was a Lotus Notes / Lotus Domino Notes server as well which had to run somewhere so we threw that onto a “high” node.

So, we’re heading into the rematch hosting www.ibm.com, www.chess.ibm.com, and whatever the URL was for Club Kasparov.

The chess match was to be held at an upper floor of the Equitable Building on Sixth Avenue (now the AXA Equitable Building).  I was expected on site at Equitable every match day as was Bob.  One of the Jean, Adam, and Kapil trio stayed behind at our 55 Broad St offices to oversee www.ibm.com (we quickly forgot about Club Kasparov), the guys from the IBM Lotus Domino Go Web Server team, and to serve as a backup operator in case we lost network access at Equitable. Chet just sorted of picked a spot in our space at Equitable and camped out for the duration of the match.

And just to complete the setup: our space at the Equitable Building was in a dressing / shower room off the building’s auditorium.  None of us thought this was a problem, because none of us knew that in the days before the match someone, presumably with good intentions, poured a caustic cleaning mixture down the drains of the unused showers.  They did not run water down the drains afterwards.  The outgasses from the cleaning mixture were noxious, causing several people to feel ill if not fall ill.  We learned this the day before the first match.

May 3, 1997: Kasparov vs. Deep Blue, Réti Opening, King's Indian Attack
In retrospect, the one thing I failed to understand was that I simply did not have the tools, nor the experience to know I needed the tools in the first place, to even remotely approximate the amount of traffic directed towards www.chess.ibm.com at 3:00 p.m. Eastern on May 3, 1997.

All our planning, our strategies, everything went up in flames.  Almost literally.  I toasted a brand new IBM RS/6000 43P work station in the first 30 minutes of the match.  See, at the time the only decent monitoring tool I had was something I’d written called “webmon”.  And webmon did its thing by tailing the log files, doing some sampling, and some calculations, and displaying the results using ANSI control characters in a terminal window.

I, being a not at all intelligent person, had set up to pipe a subset of the logs from the 20 nodes across the two complexes to the 43P I was using at the Equitable.  A modified version of webmon would display various things on the screen that we could point executives and media relations to.  Because how else do you “prove” to executives and media that a web server is doing anything?  We had a dedicated T3 line, what could go wrong?

Yeah, well, the 43P hissed a little just after the match started and went black.

And yes, I know, writing log files is stupid, just dump the data to a NoSQL database.  Unfortunately that was not an option in 1997.  And definitely not an approved IBM Program Product.

So, ten minutes into the match and we were effectively blind to what was going on with the web servers.  They seemed to be up and running, and there were…a lot of connections…and a lot of requests…and bandwidth utilization was high but not reaching saturation.

Now, you might ask why I wasn’t using any of IBM’s monitoring products, and that’s a good question that I’ve never gotten an answer to except that it wasn’t a priority of the people responsible for that area.  Effectively IBM did not have any tools, at the time, focused on monitoring web server performance. In my mainframe youth we used something called “Resource Management Facility” and while there were a set of similar tools for managing AIX or the RS/6000 SP; none tied into the web servers, neither NCSA/Apache, nor IBM’s Lotus Domino Go Web Server.

Anyway.  We were blind.  But the site seemed to be handling traffic.

Except it wasn’t.  It was rapidly hitting a point where it would collapse.

We then performed a routine similar to Paul’s previous routine with the masters.org web site: bouncing from one web server to the next trying to keep the site up in some way, shape, or form.  

And the performance problems were cratering everything else running on the “EdPlex” including www.ibm.com and the Club Kasparov web site.

We managed to find some amount of stability by running NCSA httpd on the single processor wide nodes and Domino Go on the multiprocessor “high” nodes.

What? Single processor? Multi processor?  Yeah.  
May 3, 1997: Game 1 Over, Kasparov wins in 45 Moves
So, we learned a number of things in the first 24 hours after the rematch started that would have been extremely helpful to know a month earlier if not a year earlier.

Problem 1: IBM Lotus Domino Go Web Server was based on the cern httpd binary, but multithreaded. And with IBM goodness. A multithreaded server was actually, theoretically, perfect for running on the multiprocessor “high” nodes.  The thread architecture was the reason we had such terrible performance with CGI scripts. As I recall, and it’s been 25 years and a lot of gin since, in order to fork() to invoke the CGI, the server has to stop or pause all threads.  And that can be a problem on a single processor, let alone a multiprocessor system, let alone either under any sort of load.
Problem 2: IBM Lotus Domino Go Web Server had a peculiar need to fork() occasionally even when no CGI script was involved.  I have forgotten the details of why.
Problem 3: DNS on AIX 4 was…not thread friendly.  I don’t recall if it was explicitly thread unsafe but definitely not thread friendly.  And I can hear you asking “But why on earth were you using DNS?” and the answer is: we were not explicitly using DNS in the web servers.  Both the NCSA and Apache binaries had DNS explicitly disabled.  And LDGW had it explicitly disabled in its server configuration.  But we found LDGW was occasionally invoking name server routines, even though it was explicitly disabled. 
Problem 4: The Andrew File System (AFS) was not thread safe, at all.  While it worked more or less as expected on the single processor “wide” nodes, it had issues on the multiprocessor nodes, even in non–thread environments.  When the threaded LDGW servers did filesystem activities that interacted with AFS on the multiprocessor nodes it was like throwing glue or molasses into a machine.  It kept trudging on, but slowly, and eventually causing the load level to overwhelm the system.

When we picked AFS in early 1996 there were three motivating factors: we were already using it, while we’d gotten the millions of dollars in capital to buy the RS/6000 SP complexes we couldn’t get additional capital for the servers needed to set up a new AFS cell, and everyone we knew warned us off DCE/DFS.

I don’t know that I would have done anything differently for the filesystem, because a fourth motivating factor was a strict limit on how much disk space I could put in each node.  I don’t remember the limits now but they would seem ridiculous in a world where I can get a 256Gb SD card.

The odd DNS lookup we encountered in the IBM Lotus Domino Go Web Server was easily eliminated by the guys we’d ensconced in our offices at 55 Broad.  As I recall they would give us a new build of LDGW httpd nearly every day through the rest of the match.
May 
May 4, 1997: Deep Blue vs. Kasparov, Ruy Lopez, Smyslov Variation
To be honest, the days following the first game sort of blurred together, both as they happened and certainly from 25 years’ distance.

We had a little 20, maybe 21 hours between matches to figure out a revised game plan for the web site.  I don’t recall what we did, only that it barely mitigated the problems we’d encountered the day before.

One thing we learned after the first match was that we were not even getting all of the traffic being sent to www.chess.ibm.com.  Traffic was being dropped at the network layer.  So, we were cratering and we weren’t even experiencing the true load being sent our way.

Chet and I cobbled together some meagre monitoring solutions that would give us feedback to how the servers were running and a heads up when a server was bound to fall over.  We’d observed that if we could kill the server before it reached that point, the connection backlog would clear and we could restart it after a minute or so (and move on to the next server about to fall over).

For Game 2 we called in the cavalry, the Olympics team in Southbury, CT.  They had a more or less idle SP2 complex left over from the Atlanta Games that they were using for various internal and external projects.  I do not recall if they were able to step in for Game 2 or if it was Game 3 but they helped handle the load.  Chet figured out a way to copy content from our complex to the Southbury complex while either adhering to or just routing around the various security policies we’d had set in place.

Kasparov resigned Game 2.  From a web site perspective I felt less bad than after the first game, but we still were dealing with servers failing left and right.  My phonemail mailbox (you know IBM couldn’t just call it voicemail) kept filling up with complaints from other IBM employees as well as demands that we use one program product or another, typically from a sales executive who’d previously turned down the opportunity to work with us before the match started.

May 6–10, Games 3–5
It’s all a blur at this point.  We reached a sort of stability on the site though many people complained that they could not access the site on the various newsgroups and chess sites we were monitoring.  The Domino Go developers knocked out fix after fix as we encountered issues and by the end of the match we were mostly running on Domino Go, as I recall.  But the site was still suffering issues and hangs and required frequent restarts on the individual servers.
Each of the games ended with a draw
May 11, 1997: Game 6 Deep Blue vs. Kasparov, Caro–Kann Defense, Steinitz Variation
The only thing I remember about this final game was that it felt like it ended almost immediately after it began.  Wikipedia reports it lasted just over an hour which is probably correct but it felt shorter.  We were still stuck in the shower room, several of us still coughing from whatever had been poured down the drains before the match started.

The RS/6000 43P that had failed at the outset of the match was picked up by IBM service personnel.  They’d replaced multiple parts over the course of the preceding week and, while it would boot, it was clearly damaged in some deep way.

The web site didn’t die? It ran slowly, as it had been for the past week, but was now running across three SP2 complexes as well as a solitary European mirror site in Portsmouth, UK that users had to explicitly select.

Deep Blue vs. Kasparov: The Rematch: The Aftermath thereof
The match ended on a Sunday.  As a weird appendage to IBM’s Corporate Communications team we basked in the overall glow of the “victory” over Kasparov.  But I had utterly failed to put together a site that just worked, and in the minds of many of my IBM colleagues, had not only failed this time but failed inexplicably twice with something as easy as a “chess web site”.

I felt like I’d let down many people around me, we’d all burned far too many hours working on this thing only for it to once again be a glaring failure.

In turn I felt incredibly let down by IBM’s product groups.  I was expected to utilize all sort of IBM products and figure out how to piece them together with minimal support, and zero funding to hire people to do the labor.  I later learned that IBM had an awesome monitoring tool we could have used if I had licensed it in time and spent several months installing and configuring it.  That just wasn’t an option.

I spent the week enjoying our new offices at 55 Broad Street and announced I was taking the following two weeks off.  I just sort of assumed I’d at least be removed from the role if not fired outright (neither event occurred).

I spent a couple of days moping around my apartment finally unpacking (two months after moving to New York City).  Eventually I realized that if I didn’t physically get on a plane in the next couple of hours I was not going to actually go on vacation.

I managed to be on vacation for a little over two days before someone from IBM tracked me down to ask me to weigh in, yet again, on us (literally my team, not just IBM) hosting yet another event web site.

I said “no” and returned to being off the grid for the remainder of the week.

The utter failure of www.chess.ibm.com served to kick IBM into gear to build a “serious” web event hosting platform for the 1998 Nagano Olympic Games.  From my goofy 20 node setup they would put together an 192 node complex based across multiple locations around the US and Japan.

IBM Lotus Domino Go Web Server genuinely improved a lot because of the Deep Blue experience.  We eventually, finally ported www.ibm.com to Domino Go in early 1998.  In June 1998 IBM announced that Domino Go would be canceled and that IBM would put its full support behind Apache and the open source ecosystem.  The weird result of that was my getting called out on various conference calls for not supporting open source because we were running IBM’s only–recently–canceled web server.  Even moreso since I’d spent most of the preceding years defending using the NCSA web server.

The Nagano Olympic Games web site was a success as much as I can remember.  My contribution was to manage the build–out of the SP2 complexes in parallel to my day time job as IBM’s Corporate Webmaster (it was such a nonsense job that I kept picking up additional full time jobs, I guess).  

IBM once again would ignore my advice and offered to host the 1998 Superbowl web site.  Once again I got tasked to sit on site and baby sit a system I had not architected “in case something goes wrong”.  As an added twist, two days before the Superbowl I was tasked to fly instead to Tokyo, Japan where I would get a two day crash course in the Nagano Olympic Games and then return to the US where I’d “run” the nagano.olympic.org web site during the US day time from Schaumburg, IL.

For once, when the 1998 superbowl.com web site crashed, I was no where near it nor capable of doing anything to fix it.  I watched as Paul (from masters.org, now on the Olympics team) and Cameron manually updated scores on the rapidly-ported-to-the-Olympics complex superbowl.com while watching the TV feed.

Retrospectively from 2022…
I burned out in 1999. Many things went wrong personally and professionally in a short period of time.  It’s great that companies have mental health awareness today, it wasn’t my experience at IBM in 1999. Delaying leaving IBM entirely, I took an easier role as a manager of the content and applications team for the Sydney Olympic Games.

My team on the engineering side of ibm.com was never more than seven people, and most of them were contractors.  I’ve had the opportunity to compare notes with similar teams from other Fortune 500 companies over the years and…well, most are surprised at the size of my team.  Getting headcount, either contract or “real” headcount was always a struggle at IBM.  Of the many straws that broke my will to continue as Corporate Webmaster, being told to cut most of my staff because “it’s just HTML” was one of the primary reasons.

I did not know then, and don’t understand today, why IBM kept signing us up for grand web events but would not invest in a dedicated team to manage and run them.  My primary job was to run the systems side of www.ibm.com; my second primary job was to be the primary technical point of contact for all things Internet related at IBM; my third primary job was to be a proto–CTO of all things web related across IBM Corporate.  And into that, over and over again, we’d tack on managing a chess rematch, a superbowl, the Olympic Games (twice), and a variety of now forgotten extremely highly important and critical web sites.

I did not know then that executives were

