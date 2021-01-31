<h1 align="center">
    AWC Generator
</h1>

## About

Anime Watching Club Generator is a front-end application that generates challenge codes automatically from your Anilist anime username and URL.

Disclaimer: This app is completely unrelated with AWC or Anilist.

## Getting Started

JSON Format

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
        "preset?": "https://anilist.co/anime/759/", //Anime already set by the challenge
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
