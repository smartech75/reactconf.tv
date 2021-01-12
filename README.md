# 📺 ReactConf.TV

ReactConf.TV is a place where passionate React developers are able to search organized and up-to-date react conference videos. Offering friendly features to promptly watch all these fantastic contents in one place. 

Come and [check it out](https://reactconf.tv)!

<p align="center">
  <img width="320" src="https://static.revtel-api.com/common/a107f1d8328847709c300ba25d675d6f.png" />
</p>

## Outline

- [Getting Started](#getting-started)<br/>

- [Motivation](#motivation)<br/>

- [Built With](#built-with)<br/>

- [Contribute](#contribute)<br/>

- [Directory Structure](#directory-structure)<br/>

- [Contributors](#contributors)<br/>

## Getting Started

```
cd reactconf-tv
npm install
npm start
```

open [http://localhost:8000/](http://localhost:8000/) for running locally reactconf-tv


## Motivation

We love React. Since there are always awesome tech talks and information online, we would like to build up a place where everyone can enjoy smooth learning experience.

## Built with

- [GatsbyJS](https://www.gatsbyjs.com/)
- [YouTube API](https://developers.google.com/youtube/v3)

## Contribute

Welcome to contribute!
If you have any idea or suggestion, feel free to open an issue or create a PR.

####  How To Contribute a New Conference Resource for Reactconf-tv

- Can see the file `data.json` in `data` folder , and then you would see below data structure

```
  "ytChannels": [
    {
      "name": "react-conf",
      "display": "React Conf",
      "channelId": "UCz5vTaEhvh7dOHEyd1efcaQ",
      "conferences": [
        {
          "name": "react-conf",
          "display": "React Conf",
          "filters": ["React Conf"]
        }
      ]
    }
  ]
```

- ytChannels
  - `name` Channel Name
  - `display` Unused
  - `channelId` Channel id which use to fetch youtube api
    - conferences
      - `name` The name of the playlist
      - `display` The playlist name will display on the reactconf-tv playlist
      - `filters` The keyword to get the playlist

- How to get the channel id ?
   - Select the channel which you want to append to reactconf-tv,<br/>
     you would see the channel id on the url.

     `https://www.youtube.com/channel/${channel_id}`

- Where the keyword which I would place in the filters array ?
   - See the below picture , you will see the two playlists,<br/>
     what they have in common is the keyword `React Conf`,<br/>
     so if you want to append these palylists,<br/>
     please concat the `React Conf` in the filters of the channel.<br/>

     - p.s. Because system limitations, please choose the playlist that postfix has particular year.

    ![Imgur](https://i.imgur.com/WevsAiU.png)

- Why I concat the structure of channel, but I didn’t see the list in reactconf-tv ?
   - because reactconf-tv is static site, we will output static files we need first.<br/>
     so maybe you can run below script, you will fetch the data you want,
     then submit pull request.

      `node scripts/fetch-data.js`


### step
1. Open a new issue with description.
2. Fork and clone the repo. https://github.com/your-username/reactconf-tv.git.
3. Create a new branch based off the develop branch.
4. `npm install && npm start` to run the development enviroment.
5. Make changes.
6. Make commit message with [conventional commits specification](https://www.conventionalcommits.org/en/v1.0.0/).
7. Submit a pull request, referencing any issues it addresses.
8. We will review your Pull Request as soon as possible. Thank you for your contribution ✨

## Directory Structure

The following is the hign level folder structure of reactconf-tv

```
reactconf-tv
├── CHANGELOG.md
├── LICENSE
├── README.md
├── data
│   ├── data.json
│   └── playlist
├── gatsby-browser.js
├── gatsby-config.js
├── gatsby-node.js
├── gatsby-ssr.js
├── package-lock.json
├── package.json
├── scripts
│   └── fetch-data.js
├── src
│   ├── AppContext.js
│   ├── PageContainer.js
│   ├── components
│   ├── hooks
│   ├── images
│   ├── index.css
│   ├── pages
│   ├── templates
│   └── utils
└── static
    ├── fonts
    ├── images
    └── playlistitems
```


## Contributors

<table>
  <tbody>
    <tr>
      <td align="center">
        <a href="https://github.com/whitedogg13">
          <img src="https://www.revtel.tech/static/27c58c6bb6f59c00bb890c4d2f9a823f/b7b73/Richie.png" width="100px" />
        </a>
        <br/>
        <div>Richie Hsieh</div>
      </td>
      <td align="center">
        <a href="https://github.com/whitedogg13">
          <img src="https://www.revtel.tech/static/803d205f3d3ae32b16ab8bbbaa5c11c8/b7b73/Sam.png" width="100px" />
        </a>
        <br/>
        <div>Sam Huang</div>
      </td>
      <td align="center">
        <a href="https://github.com/Mylio-chang">
          <img src="https://www.revtel.tech/static/8d3cbe17e6fc8aa9adb2f37129e71084/3b974/Mylio.png" width="100px" />
        </a>
        <br/>
        <div>Mylio Chang</div>
      </td>
      <td align="center">
        <a href="https://github.com/ulayab">
          <img src="https://www.revtel.tech/static/82e3edac286008386fed7b945d46b99c/b7b73/Ula.png" width="100px" />
        </a>
        <br/>
        <div>Ula Chao</div>
      </td>
      <td align="center">
        <a href="https://github.com/guychienll">
          <img src="https://www.revtel.tech/static/c0be7e3b863d6941f4946b68cd181ded/b7b73/Guy.png" width="100px" />
        </a>
        <br/>
        <div>Guy Chien</div>
      </td>
    </tr>
  </tbody>
</table>
