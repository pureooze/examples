When embedding a Twitch `iframe` as described in https://dev.twitch.tv/docs/embed/video-and-clips/ the following will work in a Blazor Web App but does not work in a MAUI Blazor Hybrid app:

```
<iframe src="https://player.twitch.tv/?channel={channelName}&parent=localhost"
        height="400px"
        width="400px"
        allowfullscreen>
</iframe>
```

Doing the above in MAUI Hybrid Blazor App gives the following error:
```
Refused to frame 'https://player.twitch.tv/' because an ancestor violates the following Content Security Policy directive: "frame-ancestors http://localhost:* https://localhost:*".
```

The `IframeTestMAUIBlazorHybridApp` project demonstrates this error and the `BlazorIframeTest` project demonstrates this working in Blazor.