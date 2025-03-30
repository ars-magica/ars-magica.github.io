# hArM - Character Generator in Haskell for Ars Magica

Ars Magica is a table-top roleplaying game from
[Atlas Games](https://atlas-games.com/).

There are many ways to do a character generator.  The present one, hArM,
is based on the following principles,
+ The user does not edit the character sheet in itself.
    + Instead, the user edits the advancement history, defining what 
      traits and XP are gained for each phase of character generation
      and each season of play.
    + The character sheet, at any point in time, is computed from the
      advancement history.
+ The software will validate the advancements, but never forbid anything.
  Thus the player may break the rules, as is expected in RPG.
    + Few validation rules are implemented at present. 
+ In the future, covenants can be recorded as well, and validation can
  check consistency across all characters in the covenant, to check for
  instance that teacher and student spend the same season, and that 
  books are only read by one person at a time.
+ A version control system (git) is used to edit the advancement logs.
+ The character and covenant sheets are automatically generated in a 
  github workflow.
+ In the future, many different views will be generated, to allow reviewing
  all activities for all characters in a given season, or one character's
  history since game entry.
This is **work in progress**, and should be seen as a proof of concept
at present.

+ The Hibernia Saga showcases the generator.  It is not a complete saga
  at present.
    + The [Hibernia Web Site](hibernia/) shows the generated character sheets
    + The saga source code is at
      [github](https://github.com/ars-magica/hibernia),
      with characters stored as JSON under the 
      [Data directory](https://github.com/ars-magica/hibernia/tree/main/Data)
+ Source code form hArM at  [github](https://github.com/ars-magica/harm)
+ Documentation for the [Haskell API](doc/) (haddock)
+ Source for this website at 
  [github](https://github.com/ars-magica/ars-magica.github.io)

If you want to play with it, you can clone the 
[Hibernia Saga](https://github.com/ars-magica/hibernia) and 
configure it for 
[github pages](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site) with deployment from workflow.
You can now edit the the JSON files, and the pages are updated when you push.
The repository contains the hArM binary under `bin` and a github workflow.

Caveats
+ Error handling is poor, and hArM gives little help in getting the JSON
  syntax right.
+ Only a few validation rules have been implemented yet.
+ Few virtues and flaws have been implemented and most advantages and
  disadvantages must be handled manually.
+ There is not yet any documentation for the JSON format.

