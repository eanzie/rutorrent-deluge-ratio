# rutorrent-deluge-ratio
ruTorrent plugin to show Deluge Ratio

This is a plug that will add 2 additional columns to ruTorrent UI so that there are 3 columns for ratio.

1. **Ratio** - Ratio since adding to rtorrent
2. **DlgRatio** - Custom field that hold the ratio prior to moving from Deluge
3. **TotalRatio** - Ratio + DlgRatio

I use rtorrent load.start with additional custom field

```js
[
        {key: 'd.directory.set', value: download_location}, // current path to data
        {key: 'd.custom.set', value: 'deluge_ratio,' + ratio}, // deluge ratio
        {key: 'd.custom.set', value: 'deluge_completed,' + completed_time} // deluge completed time
];
```

https://rtorrent-docs.readthedocs.io/en/latest/cmd-ref.html#term-load-start

---
Original Readme


This is used for transferring data from deluge into rtorrent, but don't want to lose the stats.

This plugin was originally copied from the seedingtime plugin, then modified.  I don't know much about JS or PHP, so this is what I came up with.
