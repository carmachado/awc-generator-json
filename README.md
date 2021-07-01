<h1 align="center">
    AWC Generator
</h1>

<h1> About </h1>

Anime Watching Club Generator is a front-end application that generates challenge codes automatically from your Anilist anime username and URL.

Disclaimer: This app is completely unrelated with AWC or Anilist.

<h1>JSON Basic Format</h1>

```json
{
   "name": "Challenge Name",
   "link?": "https://anilist.co/forum/thread/21957",
    "defaultRequired": true or false,
    "requirements": [
      {
        "splitter?": "### __Winter__",
        "id": 1,
        "question": "Watch an anime...",
        "required?": true or false,
        "preset?": "https://anilist.co/anime/759/", 
        "modes": [
          { "value": 0, "label": "Easy", "quantity": 20 },
          { "value": 1, "label": "Normal", "quantity": 20 },
          { "value": 2, "label": "Hard", "quantity": 20 }
        ],
        "additionalInformation?": [
            { "type": "Episode" },  // Ep: 1/10
            { "type": "YearSeason" },  // 2021 and Winter
            { "type": "Label", "field": "Requirement" }, // Requirement: 1
            {
              "type": "Link",
              "subtype": "Label",
              "field": "Setting",
              "fields": ["Year/Era", "Source URL"]
            }, // Settings: [Year/Era](Source URL)
            { "type": "Label", "field": "AWC Staff", "subtype": "UserFavorites" }, //AWC Staff: [username](https://anilist.co/user/username/favorites)
            { "type": "Link", "field": "Screenshot" }, // [Screenshot](https://imgur.com/gallery/00000)
            { "type": "Link", "field": "Staff Member", "subtype": "Staff" }, // Staff Member: [Yuki Suetsugu](https://anilist.co/staff/97293/Yuki-Suetsugu)
            { "type": "Link", "field": "Previously Completed", "subtype": "Anime" }, // Previously Completed: [Owarimonogatari (Ge)](https://anilist.co/anime/21745/Owarimonogatari-Ge/)
            {
              "type": "Link",
              "field": "Fellow Participant",
              "subtype": "CommentUser"
            }, //Fellow Participant: [username](https://anilist.co/forum/thread/1/comment/1)
            { "type": "Link", "field": "Challenge", "subtype": "CommentTitle" }, // Challenge: [Intermediate Challenge](https://anilist.co/forum/thread/5027/comment/552344)
            {
              "type": "Link",
              "field": "Challenge",
              "subtype": "ChallengeUser",
              "occultField": true
            }, // [User’s Challenge](https://anilist.co/forum/thread/8462/comment/184095)

            { "type": "Link", "field": "Character", "subtype": "Character" }, // Character: [Shirou Emiya](https://anilist.co/character/496)
            {
              "type": "Link",
              "field": "Character",
              "subtype": "Character",
              "splitter": ", ",
              "occultField": true
            }, //, [Shirou Emiya](https://anilist.co/character/496)
            { "type": "Label", "field": "User", "subtype": "User" }, //User: [Kondor](https://anilist.co/user/Kondor)
            { "type": "Label", "field": "Username", "subtype": "UserAnimeList" }, // User: [Kondor](https://anilist.co/user/Kondor/animelist)

        ]
      }
    ]
}
```

<h1>Challenge optional properties</h1>

**link**: the link to challenge page

**autoOccult**: not filled requirements will desapear on output

**run**: Methods to add information on end

**previouslyCompleted**: show previously completed when is true

**modes**: To genre challenges give mode easy/etc...

<h1>Requiriment optional properties:</h1>

**Spliter**: Add a string before the requirement

**Required**: Change the defaultRequirement property to this req

**Preset**: Define the default media for the req, this can't be changed

**Description**: Change the text to the user

**type**: bonus = can replace a requirement with that

**<h1>Addition Information</h1>**
Addition Information give fields like screenshot that need user input

<h2>Options</h2>

**field**: Description to add before user data.

**occultField**: Don't show field on output

**splitter**: Add text before output

**runAfter**: run a text after output


<h2>Types</h2>
Define waht will be showed on output

**Episode**: Show episode count, used on seasonal challenges

**YearSeason**: Give the Year Season on format "2021 and Summer"

**Label**: Add a input to user give a text

**Link**: Add a input to user give a URL

<h2>Label Subtypes</h2>
Give a personalized output at additional information for Label type

**User**: return `User: [user](https://anilist.co/user/user)`

**UserAnimeList**: return `User: [user](https://anilist.co/user/user/animelist)`

**Favorites**: return `User: [user](https://anilist.co/user/user/favorites)`

<h2>Link Subtypes</h2>
Give a personalized output at additional information for Link type

**Label**: Add a label to be added together. Like: 
`Test: [Field 1](Field 2)`

**Staff**: Search Staff name and show that. Like: 
`Test: [Oda Eiichirou](https://anilist.co/staff/96881/Oda-Eiichirou)`

**Character**: Search Character name and show that. Like: 
`Test: [Monkey D. Luffy](https://anilist.co/character/40/Monkey-D-Luffy)`

**Anime**: Search anime name and show that (Respect user setting). Like: 
`Test: [One Piece](https://anilist.co/anime/21/One-Piece/)` 

**CommentUser**: Search user name and show the comment link. Like: 
`Test: [Tepgam](https://anilist.co/forum/thread/4446/comment/102872)` 

**ChallengeUser**: Search user name and show the comment link. Like: 
`Challenge: [Tepgam’s Challenge](https://anilist.co/forum/thread/4446/comment/102872)` 

**CommentTitle**: Search thread name and show the comment link. Like: 
`Challenge: [Anime Watching Challenge: Challenge Submissions](https://anilist.co/forum/thread/4446/comment/102872)` 

