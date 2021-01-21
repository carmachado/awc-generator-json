<h1 align="center">
    AWC Generator
</h1>

## About

Anime Watching Club Generator is a front-end application that generates challenge codes automatically from your Anilist anime username and URL.

Disclaimer: This app is completely unrelated with AWC or Anilist.

## Getting Started

JSON Format

```bash
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
        "additionalInformation?": [
            { "type": "Episode" },  // Ep: 1/10
            { "type": "YearSeason" },  // 2021 and Winter
            { "type": "Label", "field": "Requirement" }, // Requirement: 1
            { "type": "Label", "field": "AWC Staff", "subtype": "UserFavorites" }, //AWC Staff: [Kondor](https://anilist.co/user/Kondor/favorites)
            { "type": "Link", "field": "Screenshot" }, // [Screenshot](https://imgur.com/gallery/dXQyRYq)
            { "type": "Link", "field": "Staff Member", "subtype": "Staff" }, // Staff Member: [Yuki Suetsugu](https://anilist.co/staff/97293/Yuki-Suetsugu)
            { "type": "Link", "field": "Previously Completed", "subtype": "Anime" }, // Previously Completed: [Owarimonogatari (Ge)](https://anilist.co/anime/21745/Owarimonogatari-Ge/)
            {
              "type": "Link",
              "field": "Fellow Participant",
              "subtype": "CommentUser"
            }, //Fellow Participant: [Shoxi](https://anilist.co/forum/thread/4448/comment/93023)
            { "type": "Link", "field": "Character", "subtype": "Character" }, Character: [Shirou Emiya](https://anilist.co/character/496),
            { "type": "Label", "field": "User", "subtype": "User" }, //User: [Kondor](https://anilist.co/user/Kondor)

        ]
      }
    ]
}
```
