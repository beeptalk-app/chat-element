
# Beeptalk Widget

[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/) 
[![GitHub release](https://img.shields.io/badge/release-v1.2.2-green)](https://github.com/beeptalk-app/chat-embedder/releases)


Official [Beeptalk](https://beeptalk.app) chat widget.


### Deployment

To include Beeptalk widget on your page, you need to include this script at the end of the `<body>`:

```html
<script src="https://cdn.jsdelivr.net/gh/beeptalk-app/beeptalk-widget@1.2.2/index.min.js"></script>
<script type="text/javascript">beeptalkInit({id: 'YOUR_PROJECT_ID'});</script>
```


### Options documentation

You can pass options to beeptalkInit() function to use some extra features:

```js
  beeptalkInit({
    id
    suid
    uuid
    darkIcon
    primaryColor
    path
    agent
  });
```

| Parameter | Type     | Required      | Description                |
| :-------- | :--------- | :------------ | :----------------------- |
| `id` | `string` | **Yes** | Beeptalk project ID |
| `suid` | `string` | No |  Session unique ID, this is needed to preserve a chat between sessions. |
| `uuid` | `string` | No |  User unique ID (this will be recorderd on Beeptalk, and it might be useful for analytics) |
| `darkIcon` | `boolean` | No |  If `true`, the icon of the widget will be dark instead of white, default to `false`. |
| `primaryColor` | `string` | No |  The background color (hexadecimal) of the widget, defaults to the primary color of Beeptalk. |
| `path` | `string` | No |  The path of the page (without the base url), eg. "/home" (this will be recorderd on Beeptalk, and it might be useful for analytics) |
| `agent` | `SHA1` | No |  The Beeptalk user (must be added to your project) email to assign to the chat, the email must be SHA1 hash encrypted. This is automatically handled if no agent is provided. |


