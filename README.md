# aptv-playlist

APTV 官方播放列表（Kimentanm/aptv）的通用格式转换版，供 IPTVX、UHF 等通用 IPTV 播放器使用。

- `aptv_vlc.m3u` — #EXTVLCOPT 格式（每频道单独标注 User-Agent / Referer），适合 VLC 内核播放器（如 IPTVX）
- `aptv_suffix.m3u` — URL 后缀格式（|User-Agent=…），适合不识别 EXTVLCOPT 的播放器（如 UHF）

原始列表的频道在 APTV 里是按频道标注 UA 的，通用播放器不认这种标注，所以在其他播放器里播不了；这两个文件把同样的信息改写成了通用格式。内容为转换当日的快照，原列表更新后需重新转换。
