---
title: About Myself
date: 2022-09-23
published: true
tags: ['Daniel','Ye']
canonical_url: false
description: "Hi there! I'm Daniel and welcome to my portfolio! I am a current Software Engineering student at the University of Waterloo and am looking for co-op opportunities."
---
I am a hard-working, dedicated individual that is always looking for learning opportunities! 

Please find my resume attached to the link below

```html
<template>
  <Layout>
    <h2>Latest blog posts</h2>
    <ul>
      <li v-for="edge in $page.allWordPressPost.edges" :key="edge.node.id">
        {{ edge.node.title }}
      </li>
    </ul>
  </Layout>
</template>

<page-query>
query Blog {
  allWordPressPost (limit: 5) {
    edges {
      node {
        _id
        title
      }
    }
  }
}
</page-query>