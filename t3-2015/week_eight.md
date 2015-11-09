## RubyOnRails - Week 8 Newsletter

### Upcoming Events

* SQuAD - Software Quality Association of Denver - Tue Nov 10, 4p-6p - PPA Event Center, Denver - easy free parking
http://www.meetup.com/SQUADCO/events/222539066/
“Shifting the Test Role Pendulum” by Melissa Tondi

* All Things API meetup - Wed Nov 11, 6p-8p - Industry coworking space in Denver 
http://www.meetup.com/All-Things-API/events/226057914/
“When RESTful may be Considered Harmful” by Ross Garrett
<we can’t attend, but interesting to know about..>

* DaVinci - HTML and CSS Inroduction Workshop - Tue Nov 16, 6p-9:15p - $20 RSVP http://www.davinciinstitute.com/colorado-events/#!event/2015/11/18/introduction-to-html-css-workshop 
http://www.meetup.com/DaVinci-Institute/events/226520283/

* DaVinci - Mobile App Dev using Swift - 11 weeks - Mon Jan 18, 6:30p - 9:30p
http://www.davinciinstitute.com/colorado-events/#!event/2016/1/19/learn-ios-mobile-app-development-using-swift-programming-language

### Shoutouts

> * Sue  - Shoutout to Wendy for TDD setup assists during the week, shoutout to John for onsite discussions around rails and html interactions on Friday, shoutout to Andrew for being an excellent TDD trainer, shoutout to Jason for remaining after class to answer questions.. week after week!

> * Lucas - Shoutout to Bill LeBorgne for your tdd wizardry.

> * Danny - Shoutout to Tim for being a TDD master.  Thanks for your help!






### Week 8 - In Review

Welcome to Week 8 in Review or: Scaffolding Appreciation Week Part Deux.  

This week we contemplated the subtle distinctions between behavior driven development (BDD) and test driven development (TDD). BDD is an extension of the ideas behind test driven development, yet is designed to implement tests that can be read more naturally and is helpful for designing the software in collaboration with others in addition to making sure that it works. Test driven development is more for the benefit of developers and BDD is more for the benefit of users. So in other words, there isn’t a hard and fast rule to determine which is which but Jason insists there is a difference, and I trust him. 

When writing tests for BDD and TDD the general idea is the same, and that is ‘red, green, refactor’.  This concept is to write a failing test (red), write the code to make it pass (green), and then refactor either the code or the test, rinse and repeat.  With BDD we are testing the behaviors that we want to be present in our website, such as being able to push a button that takes you to the homepage.  The red, green, refactor steps would have us write a behavioral test stating we need to button that takes us to the homepage.  Our test would fail (red) so we would then write the code make this pass (green).  We would then adjust our code or our test to make sure everything else within our app works with our changes (refactor).  Rinse and repeat.

On Wednesday our warm up exercise involved forking a rails repo that Jason gave us and then modifying the app to pass the specs that were included in it. This ended up taking longer than we expected because we tended to over complicate our objective as is often the case when we are overwhelmed with multicolor strobes of unit tests. At this point in the course we are just immersing and re-immersing ourselves in this framework and until the pieces come together and we memorize more shortcuts in RubyMine. I’ve found it is a good newbie rails practice to write tests twice and scaffold once. But does it really matter if you can just run rollback the migration you just raked? I don’t know. What I do know is this :

“I’m a factory girl in an automatically generated world. Helping make good tests pass, I must refactor this class.”

We were introduced to tests that filled in form fields with fake content and were shown how to make that content be randomly generated with FactoryGirl. 

Sincerely,

Boole posse, t3-2015

Tim Park,  Danny Debevec,  Sue Uyetake,  Matt Michnal,  Riley Jones  
