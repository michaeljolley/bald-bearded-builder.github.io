---
layout: post
date: 2019-09-01 17:09
title: "Playing with Node.js and making chat more interactive"
image: https://user-images.githubusercontent.com/1228996/64084956-7e540480-ccf5-11e9-8ec0-72a0d750574a.png
description: "Fixed a few bugs with sound clips playing on alerts and tracking chat in MongoDB"
comments: true
tags: [twitch, stream, javascript, mongo]
replay: https://youtu.be/7nNML4-DeHU
---

<img src="{{page.image}}"/>

## Stream Replay Link

[{{page.replay}}]({{page.replay}})

<!--more-->

### Segments

| Timestamp | Topic
| ---       | ---
| [00:05]({{page.replay}}?t=600)      | Kicking it off          |
| [00:22]({{page.replay}}?t=1324.056) | Candle Winner - Unicorn |
| [00:26]({{page.replay}}?t=1615.302) | Starting to write some code |
| [02:39]({{page.replay}}?t=9578.431) | Wrapping up and raid to [luckynos7evin](https://twitch.tv/luckynos7evin) |

---

### Today's Candle To Code By

[Unicorn Dust](https://amzn.to/320cEn1)

---

### Goals

- [x] Flag chatters as contributors on the stream

---

## Today's stream brought to you by

### Subscribers

- [phrakberg](https://twitch.tv/phrakberg) (6 mo)
- [Lannonbr](https://twitch.tv/lannonbr) (4 mo)
- [sorskoot](https://twitch.tv/sorskoot) (5 mo)
- [Taumee412](https://twitch.tv/taumee412)

### Cheers

| Compadre            | Bits        |
| ---                 | ---         |
| [codingisundercover](https://twitch.tv/codingisundercover) | 3 |
| [phrakberg](https://twitch.tv/phrakberg) | 10 |
| [roberttables](https://twitch.tv/roberttables) | 1 |

### Moderators

- [RamblingGeek](https://twitch.tv/ramblinggeek)
- [phrakberg](https://twitch.tv/phrakberg)
- [IAmNotMyself](https://twitch.tv/iamnotmyself)
- [roberttables](https://twitch.tv/roberttables)
- [parithon](https://twitch.tv/parithon)

### Contributors

<table class="user">
    <tr>
      <td><img class="profile" src="https://static-cdn.jtvnw.net/jtv_user_pictures/908fd818-1fbe-4b44-8633-dfc6bec175c9-profile_image-300x300.png"/><span>Flyken<br/>
      <i class="fab fa-twitch"></i> <i class="fab fa-twitter"></i> <i class="fab fa-github"></i></span></td>
      <td><img class="profile" src="https://static-cdn.jtvnw.net/jtv_user_pictures/3bdd5c96-e43c-4745-b3fc-d969f8f55121-profile_image-300x300.jpeg"/><span>FBoucheros</span></td>
      <td><img class="profile" src="https://static-cdn.jtvnw.net/jtv_user_pictures/20bd3f0a-ce68-4f5c-a9bf-f61b950be3d2-profile_image-300x300.png"/><span>IAmNotMyself</span></td>
      <td><img class="profile" src="https://static-cdn.jtvnw.net/jtv_user_pictures/8e4eab31-0a66-4b1a-a0df-ca962e4a9b8e-profile_image-300x300.jpeg"/><span>Lannonbr</span></td>
    </tr>
    <tr>
<td><img class="profile" src="https://static-cdn.jtvnw.net/jtv_user_pictures/f5373f0e-4fa8-4d90-8303-12c47001c08f-profile_image-300x300.jpeg"/><span>AncientCoder</span></td>
<td><img class="profile" src="https://static-cdn.jtvnw.net/jtv_user_pictures/926c0d6b-bc04-4dba-88a6-915dc6c6bb54-profile_image-300x300.png"/><span>CopperBeardy</span></td>
<td><img class="profile" src="https://static-cdn.jtvnw.net/jtv_user_pictures/a390873e-0dff-4ae6-a798-93c1e9516616-profile_image-300x300.png"/><span>RamblingGeek</span></td>
<td><img class="profile" src="https://static-cdn.jtvnw.net/jtv_user_pictures/3c435956-3fc3-4ccd-bac5-1c4e1671500b-profile_image-300x300.png"/><span>phrakberg</span></td>
    </tr>
    <tr>
<td><img class="profile" src="https://static-cdn.jtvnw.net/jtv_user_pictures/1e60395d-4246-4690-b486-40ebb3c8b00b-profile_image-300x300.png"/><span>tbdgamer</span></td>
<td><img class="profile" src="https://static-cdn.jtvnw.net/jtv_user_pictures/ae01250c-087b-4745-8bff-745731ce30da-profile_image-300x300.png"/><span>Lonely_Pl4yer1</span></td>
<td><img class="profile" src="https://static-cdn.jtvnw.net/jtv_user_pictures/16707a2a-fcac-48ec-b40d-6d6916162dcc-profile_image-300x300.png"/><span>LampeWebDev</span></td>
<td><img class="profile" src="https://static-cdn.jtvnw.net/jtv_user_pictures/6654d342-e3b6-45c4-83fe-32b523bdc7e2-profile_image-300x300.png"/><span>roberttables</span></td>
    </tr>
    <tr>
<td><img class="profile" src="https://static-cdn.jtvnw.net/jtv_user_pictures/7b926973-80d1-4ce5-9f1d-9153390a8d9c-profile_image-300x300.png"/><span>MihaZupan</span></td>
<td><img class="profile" src="https://static-cdn.jtvnw.net/jtv_user_pictures/9b76630d-fce3-46b9-a230-4fb0b20de988-profile_image-300x300.png"/><span>stuykgaming</span></td>
<td><img class="profile" src="https://static-cdn.jtvnw.net/jtv_user_pictures/095ad31c-6075-40b9-ad89-be9a01a0bf58-profile_image-300x300.png"/><span>BixxPlays</span></td>
<td><img class="profile" src="https://static-cdn.jtvnw.net/user-default-pictures/bb97f7e6-f11a-4194-9708-52bf5a5125e8-profile_image-300x300.jpg"/><span>Telluuu</span></td>
    </tr>
    <tr>
<td><img class="profile" src="https://static-cdn.jtvnw.net/jtv_user_pictures/958a22b1-e9e5-4390-8843-98d9def72a35-profile_image-300x300.png"/><span>sorskoot</span></td>
<td><img class="profile" src="https://static-cdn.jtvnw.net/user-default-pictures/bb97f7e6-f11a-4194-9708-52bf5a5125e8-profile_image-300x300.jpg"/><span>bl3nd865</span></td>
<td><img class="profile" src="https://static-cdn.jtvnw.net/jtv_user_pictures/tuesdaylte-profile_image-e422319120e08c90-300x300.jpeg"/><span>TuesdayLTE</span></td>
<td><img class="profile" src="https://static-cdn.jtvnw.net/user-default-pictures/bb97f7e6-f11a-4194-9708-52bf5a5125e8-profile_image-300x300.jpg"/><span>Taumee412</span></td>
    </tr>
    <tr>
<td><img class="profile" src="https://static-cdn.jtvnw.net/jtv_user_pictures/xlxacidxlx-profile_image-c2e051db5e04a5ae-300x300.png"/><span>xlxAciDxlx</span></td>
<td><img class="profile" src="https://static-cdn.jtvnw.net/user-default-pictures/b83b1794-7df9-4878-916c-88c2ad2e4f9f-profile_image-300x300.jpg"/><span>lotsoftzatziki</span></td>
<td><img class="profile" src="https://static-cdn.jtvnw.net/jtv_user_pictures/abd243dc-3790-4a73-b7b4-1269f89ce083-profile_image-300x300.png"/><span>parithon</span></td>
    </tr>
</table>
