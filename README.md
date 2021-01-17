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
   "link": "https://anilist.co/forum/thread/21957",
    "defaultRequired": true or false,
    "requirements": [
      {
        "id": 1,
        "question": "Watch an anime...",
        "additionalInformation": [
            { "type": "Episode" },  // Ep: 1/10
            { "type": "YearSeason" },  // 2021 and Winter
            { "type": "Label", "field": "Requirement" }, // Requirement: 1
            { "type": "Link", "field": "Screenshot" }, // [Screenshot](https://imgur.com/gallery/dXQyRYq)
            { "type": "Link", "field": "Staff Member", "subtype": "Staff" } // Staff Member: [Yuki Suetsugu](https://anilist.co/staff/97293/Yuki-Suetsugu)
        ],
        "required": true or false
      }
    ]
}
```
