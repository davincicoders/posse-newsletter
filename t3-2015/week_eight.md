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

> * Riley - Shout out to Andrew Lampert for sharing his time answering my questions about his experience in programming.

> * Tim - Shout out to Andy for helping me with questions about Active Record.




### Week 8 - In Review

This week, we spent a lot of time in class creating a rails app called DaVinci Shopping Cart. It was a great exercise in incorporating a lot of the techniques we’ve learned so far, as well as an introduction to new tools such as scaffolding. Our goal was to create an app that could create a list of products that were for sale and enable a user to add desired products to a shopping cart. One of the first things we did was generate a rails scaffold for products. Scaffolding is an extremely useful Rails tool that quickly generates all of the necessary files for a given model. In our shopping cart, we wanted to create a product model with four attributes: name, description, image, and price. Rails scaffolding will automatically generate and modify the model, views, controller, and tests for our Product so it saves HOURS of work and enables you to start working on other functionalities in your app.

```
rails generate scaffold Product name:string description:string image_url:string price:decimal
```

As we continued to add features (carts, line items) to our DaVinci Shopping Cart, we learned about the subtle distinctions between Behavior (BDD) and Test Driven Development (TDD). BDD is an extension of TDD, but aims to implement tests that can be read more naturally. It also focuses more on a user’s experience of an app, rather than the actual result of code. This is helpful for collaborating with others and also reduces the amount of effort required to write good tests. 

Consider the following test, written with the `capybara` gem, which allows a user to sign into their profile page:
```
feature ‘Signing in’ do
  scenario ‘allows a user to sign in to profile page’ do
    visit ‘/home’

    click_button ‘Sign In’

    fill_in ‘Email’, with: ‘person@company.com’
    fill_in ‘Password’, with: ‘secret123’

    expect(page).to have_content(‘Sign in successful.’)
  end
end
```

The syntax is so simple that you can focus on building your app instead of wasting time writing complex tests. While the distinction between BDD and TDD is subtle, it helps to think of them as answer two different questions: ‘How would I use this?’ and ‘How does this work?’ When writing tests for BDD and TDD, the general workflow is the same: ‘red, green, refactor’.  The general idea is to write a failing test (red), write the code to make it pass (green), (refactor) either the code or the test, and repeat.

While building the DaVinci Shoping Cart, we also learned about a couple of new gems that are extremely useful in developing Rails apps: 

> * [factory_girl_rails](https://github.com/thoughtbot/factory_girl_rails) and [faker](https://github.com/stympy/faker). These two gems can be used in tandem to generate fake data that is useful in testing your app. More importantly, being able to see how your website operates with fake data allows you to pinpoint bugs in your code and other issues that might detract from a user’s experience.

To help us get more comfortable with Rails, Jason gave us a challenging warmup exercise on Wednesday. We had to fork a repository for a rails app that was broken and the challenge was to fix the code to pass tests that Jason had already written. This ended up taking longer than we expected because of our unfamiliarity in reading test errors and fixing the ‘right’ problem. However, the nice thing about TDD and BDD is that we can focus on one error at a time until we make the right changes to pass our tests. At this point in the course, we are just immersing ourselves with practicing with the Rails framework until all of the pieces come together.

Sincerely,

Boole posse, t3-2015

Tim Park,  Danny Debevec,  Sue Uyetake,  Matt Michnal,  Riley Jones  

