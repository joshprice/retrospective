Retrospective
=============

`retrospective` is like markdown but for tracking stories in plain text. It's a simple DSL for capturing the results of a retrospective.

Put it in your version control of choice and keep it versioned right alongside your project, maybe even tag with it with your iteration or release number.

It was inspired by the [Storywall project](http://github.com/joshprice/storywall). In fact, you might have noticed that the syntax is almost identical. The files are intended to be treated somewhat differently by any tools which might enhance them, so they are distinguished by their file extensions. A retrospective file should end in `.retrospective` and likewise a storywall file should end in `.storywall`


Traditional retrospective example
---------------------------------

A `retrospective` is just a text file (ending in `.retrospective`) that looks like this:

    # retrospective example
    #
    # <Column name>:
    #   <Title> <Description>
    
    What we did well:
      * Released first version on time. 
    
    What we learnt:
      * Must give hosting company 2 days more notice before deployment
      * Clearcase sucks
    
    What should we do differently next time:
      * Automate all deployment procedures. We need repeatability so we can deploy more reliably, more often.
    
    What still puzzles us:
      * Why are we still using such a horrible VCS? It's 2010.
    
    Actions:
        * Investigate moving to Git [AB/CD]
        * Give at 1 week notice to hosting co [XY]
        * Keep being awesome! [All]
    
Use this style if you run [traditional style retrospectives](http://www.retrospectives.com/pages/RetrospectiveKeyQuestions.html)


Simple retrospective example
---------------------------------

The categories used in the above example help to guide participants, but in doing so sometimes complicates the thinking process.
You also want to action the things that your team needs to improve or change. 
In this case simply record the things you want to discuss.
Place them in a single column, then proceed to discuss the event, ordering them in terms of how positively that event affected the team.
When this has been decided place it on a wall, between the top of the column (being the best possible outcome for the team) and the bottom (being the worst outcome).
Then work up from the bottom actioning each event and assigning an owner.
Finally prioritise the actions by ordering them by importance.

    # retrospective example
    #
    # <Column name>:
    #   <Title> [Owner Initials] <Description>
    
    Events:
      * Released first version on time.
      * Must give hosting company 2 days more notice before deployment
      * Clearcase sucks

    Actions:
      * Investigate moving to Git [AB/CD]
      * Give at 1 week notice to hosting co [XY]
      * Keep being awesome! [All]


Why would I use retrospective over a more fancy tool?
-----------------------------------------------------

* This is the only retrospective tool I've heard of. Please let me know if you've seen one.
* You like simple tools
* The format can be as simple or as complex as you like
* Your data is in a format that anybody can understand
* You can edit your storywall with whatever tool you like to edit text with
* In other words you don't need to learn another complex tool which never does quite what you want
* Your storywall is versioned and distributed right alongside your code so you know your history is always there when you need it
* Text is regular and parsable, like a text-based API
* You can extend the format if it doesn't have the feature you want


How do I get started?
---------------------

`retrospective` is currently just a spec, but you can use it right now!

Just create a file called `iteration-1.retrospective` or even `release-2.0.retrospective` in your project directory. Use one of the formats above, or  and check it in to your version control system.

Run your retrospective as normal

When you're done editing, commit and push the result so the rest of your team can see the progress.

If you get a merge conflict just resolve as you normally would. You might want to check with your team member to make sure no data was lost in the merge.

