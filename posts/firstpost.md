---
title: First post!
description: The one where I'm optimistic about starting a blog.
date: 2022-09-16
scheduled: 2022-09-17
tags:
  - first-post
layout: layouts/post.njk
image: https://cdn.pixabay.com/photo/2020/08/30/20/54/rice-field-5530707_1280.jpg
---



I've gone & started a blog. We'll see how this pans out.

In any case, I don't quite have readily-available musings to blog about yet. Just some recent **momentum** spurred by refreshing my personal site; momentum enough to (_temporarily_??) surpass insecure misgivings about posting my thoughts for the world to see \[`read: ignore` 🤷‍♂️\].

Surely, it will be rare if I do get around to writing things.

A start may be to writeup the talk I'll give soon at [Strange Loop 2022](https://www.thestrangeloop.com/2022/a-commerce-centric-approach-to-queuing-fairly-at-high-throughput.html)

![Moebius Strip I, M.C. Escher](https://uploads6.wikiart.org/images/m-c-escher/moebius-strip-i.jpg)

### Talk Preview

As my first external technical conference talk, inescapably, I'm anxious.

If all goes well, I'll transcribe the talk contents in blog form afterwards.

For now, a small snippet of Lua code previewing a queue-centric algorithm:

``` lua
-- reject unless (ARGV[6]==client_bin_idx) <= working_bin
if tonumber(ARGV[6]) > working_bin then
  if hmset_idx > 1 then
    redis.call("HMSET", shop_queue_key, unpack(hmset_args))
  end
  return "reject," .. tostring(working_bin)
end
```
