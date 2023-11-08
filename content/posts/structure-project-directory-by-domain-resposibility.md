+++
title = 'Structure Project Directory by Domain Resposibility'
date = 2023-11-09T00:58:08+08:00
draft = false
+++

As a backend developer at a startup company, I often jumps between multiple projects, and the scale ranging from small
to medium. As a result, I often find myself asking the question, "How to structure the project, so that everyone can
easily jump in and understand everything they need to in order to complete a task?".

Instead of the common separate by technical responsibilities

```
sample-project
├───Controllers
│   ├───Authors
│   ├───Books
│   └───Publishers
├───Models
│   ├───Authors
│   ├───Books
│   └───Publishers
└───Services
    ├───Authors
    ├───Books
    └───Publishers
```

I'm more keen on a structure as follow:

```
sample-project
├───Authors
│   ├───Controllers
│   ├───Models
│   └───Services
├───Books
│   ├───Controllers
│   ├───Models
│   └───Services
└───Publishers
    ├───Controllers
    ├───Models
    └───Services
```

I find the latter easier to work with for the following reasons:

## Similar to RESTful convention

At my company, we're using RESTful API for communication between frontend and backend. RESTful APIs are resource-based,
when designed right, it conveys the domain very clearly. When someone needs to jump into the codebase to fix a bug, he/
she can based on the API route, find the correct folder, and everything is contained within that same folder. There's no
need to jump back and forth between the different files in different layer just to grasp everything.
