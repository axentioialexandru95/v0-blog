---
title: "Nextjs 15 drop it like it's hot"
description: "Short description of the post"
pubDate: "2023-10-26"
tags: ["nextjs", "blog", "first post"]
heroImage: "/min.png"
---

## Target audience

Nextjs developers who want to learn about the new features and improvements in Next.js 15 and React developers who want to try nextjs.

## Title

Nextjs 15 drop it like it's hot

## Outline

1. Introduction
2. What's new in Nextjs 15
3. Diving deeper into the new features
4. Deployment
5. Outro and shout out to payload cms

## Chapter 1: Introduction

Just a few days before the Nextjs conference, Next.js has released version 15 and it's a really nice update in terms of performance and DX.
Firstly if you don't know me, I'm a full stack developer with 10 years of experience. I've been using Nextjs since version 11 and I'm excited to see where it's going.
So let's hop in.

## Chapter 2: What's new in Nextjs 15

Nextjs has been around for a while now and it's a powerful framework for building modern web applications.
It's a framework that allows you to build server-side rendered (SSR) React applications, static site generation (SSG) and incremental static regeneration (ISR) and much more.
You can even build your APIs with it.

With the release of Nextjs 15, we have some new features that are worth checking out.

1. Caching no longer is forced, you can now choose when to cache your pages.
2. React 19 support, even if react 19 hasn't been released yet due to some suspense issues.
3. Turbopack, the new build tool that is supposed to be 10x faster than Webpack.
4. Enhanced forms

And much more.

## Chapter 3: Diving deeper into the new features

Now, let's dive deeper into those new features.

### 1. Caching

Caching is a feature that allows you to cache your pages or data to improve performance.
And that's now off by default, you have to opt-in to it.
People ran into some issues with the previous caching mechanism, so they decided to change it.

As they said in the release post:

With Next.js 15, we're changing the caching default for GET Route Handlers and the Client Router Cache from cached by default to uncached by default. If you want to retain the previous behavior, you can continue to opt-into caching.

To actually enable caching, you have to do it manually like this:

```js
const nextConfig = {
  experimental: {
    staleTimes: {
      dynamic: 30,
    },
  },
};
 
export default nextConfig;
```

This will cache the page for 30 seconds.

This new caching mechanism is much more flexible and gives you more control over the caching process so a really thumbs up to the team for that.

### 2. React 19 support

While React 19 hasn't been released yet, Nextjs 15 supports it right now but I wouldn't recommend using it in production just yet, because of some suspense issues that will be fixed in React 19.
The transition should be smooth though and a really nice thing they added for the upgrade is that you can use codemod command to automatically upgrade your code.
I tested this on a new project and it worked like a charm.
Not sure how good it is on a big project though so use with caution.

### 3. Turbopack

Man, this is the thing I was waiting for ages.
Turbopack is the new rust based build tool that is supposed to be a lot faster than Webpack.
Finally there's a good alternative to Vite in the nextjs ecosystem.
This is turbopack dev though, not the production ready version.

So you're gonna use it in dev mode for now.

Now, I saw some posts that said that Turbopack is faster than Vite and I don't feel that's necessarily true.
I mean, Vite is already insanely fast and the ecosystem around it is growing.
But Turbopack is a good addition to the ecosystem and I'm sure it will only get better.

So what are the benefits of using Turbopack?

- Up to 76.7% faster local server startup.
- Up to 96.3% faster code updates with Fast Refresh.
- Up to 45.8% faster initial route compile without caching (Turbopack does not have disk caching yet).

These numbers alone are impressive, I just tested the dx on a new project and it felt really snappy.

Amazing work

### 4. Enhanced forms

Forms are a crucial part of any web application and Nextjs 15 has some new features that make them better.
While I feel a little bit funny about the whole forms thing, because I feel we're just going back to how php used to work, but I guess it's just a matter of time until we reach a full circle here.

The new `<Form>` component extends the HTML `<form>` element with prefetching, client-side navigation, and progressive enhancement.

```js
import Form from 'next/form';
 
export default function Page() {
  return (
    <Form action="/search">
      <input name="query" />
      <button type="submit">Submit</button>
    </Form>
  );
}
```

The `<Form>` component comes with:

- Prefetching: When the form is in view, the layout and loading UI are prefetched, making navigation fast.
- Client-side Navigation: On submission, shared layouts and client-side state are preserved.
- Progressive Enhancement: If JavaScript hasn't loaded yet, the form still works via full-page navigation.

This is a really nice addition and it makes forms way better than before.

Shout out to Alex Sidorenko for this example right here that shows the new forms in action: [check out his post](https://x.com/asidorenko_/status/1848469176924704919)

This looks really cool.

### 5. Many more

There are many other new features and improvements like Async Request APIs changes, a really nice looking static indicator, a new instrumentation file to tap into nextjs lifecycle and more.
If you like to dig deeper into the new features, you can check out the [release post](https://nextjs.org/blog/next-15).

## Chapter 4: Deployment

There's one really nice thing I want to mention is that the team from Nextjs were listening to the community and they decided to support others that had issues with deploying their apps to other platforms than Vercel.
So that's a really nice thing to see.

## Chapter 5: Outro and shout out to payload cms

With the whole drama about wordpress around I want to mention that I think now's the time for others to think more about some alternatives.
While I'm also developing products with Laravel and filament, I am really interested into trying something similar in the ecosystem.

I've found no better thing that fits my taste other than [Payload CMS](https://payloadcms.com/).
They're now on version 2 and since they're still new I haven't been using them yet but with the new version 3.0 coming out soon I think it's a good time to give them a shot.

As James Mikrut said they're gonna update into payload 3.0 in an ETA of 2 weeks now.
I'll really give them a shot and I'll let you know my thoughts in a separate video.

## Chapter 6: Outro

Thank you for watching and I hope you enjoyed the video.
If you have any questions or feedback, please let me know in the comments below.
See you in the next video.


🚀 Next.js 15 is here! Let's explore the most exciting features and improvements in this major release.

In this video, we'll cover:
- Server Actions improvements 
- New Form component
- Built-in SEO improvements
- Deployment changes
- Payload CMS thoughts


🔗 Useful Links:
Next.js 15 Release: https://nextjs.org/blog/next-15
Payload CMS: https://payloadcms.com/

👋 Let me know in the comments what feature excites you the most!

#NextJS #WebDevelopment #JavaScript #React #Programming #Tech #PayloadCMS

🔥
