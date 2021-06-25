---
layout: post
title:      "Semantic UI: A Component Library for the Design Challenged"
date:       2021-06-25 16:46:58 +0000
permalink:  semantic_ui_a_component_library_for_the_design_challenged
---


While working on my final portfolio project, I needed to find a styling solution
for my app. I tried Bootstrap, Material UI, Tailwinds CSS, and found all of to be
annoying to learn and integrate quickly into my app. This is likely no fault of
those code libraries, but I have little patience for styling, especially when trying
to complete a project in a timely fashion. After a week of attempting and failing
to implement any of the aforementioned frameworks, I found Semantic UI, a CSS and
React component library that as it's name implies, aims to make styling a website
a simpler process by making styling a simple, declarative framework to give projects
style. Material UI promised similar functionality, but some of the components in
the Material UI library, at the time of writing, do not work with React in strict.
Semantic UI was the only choice for a design amateur like myself.

## *Mostly* Abstracting Away CSS

I know CSS is an incredibly powerful tool, give developers limitless options when
styling their projects. That power and versatility comes at a cost. It is not uncommon
to see a stylesheet for a website grow to include over a thousand lines of code.
The logic of CSS is simple, styling rules cascade to allow fine grained control
over discrete details, while other rules can be set higher up in the cascade, like
setting the global font family for the site. It's an easy concept to understand,
but in practice, keeping track of what rules apply where can be a daunting task.
Tools to manage the complexity of bloated stylesheets exist, but users must learn
how to use those tools as well. Not to mention, they still require developers to
already have a robust knowledge of CSS to implement the more cutting edge features
of CSS like animations.

Semantic UI provides two modules to add to an App: ``` semantic-ui-css ``` and
``` semantic-ui-react ```. The first module providing a set of stylesheets to source
in your javascript entry file, and the second providing all of the styled components.
Here is an example of an implementation of a Card component in a project I have been
working on.

    return (
      <Card>
        <Card.Content>
          <Icon name='calendar' size='large' style={{float: "right"}} />
          <Card.Header>{props.jot.title}</Card.Header>
          <Card.Meta>{props.jot.location}</Card.Meta>
          <Card.Description>{props.jot.formattedDate}</Card.Description>
        </Card.Content>
        <Card.Content extra>
          <Button.Group widths='3'>
            <Button compact color='green' onClick={handleAccept}>
              Accept
            </Button>
            <Button compact color='red' onClick={handleReject}>
              Reject
            </Button>
            <Button compact onClick={() => setOpen(true)} >
              Edit
            </Button>
          </Button.Group>
          <JotEditModal jot={props.jot} opener={open} setOpener={setOpen} />
        </Card.Content>
      </Card>
    )

And here is what that looks like when rendered:


![](https://raw.githubusercontent.com/zacharytq/jot-frontend/master/public/Screenshot%20from%202021-06-25%2012-36-11.png)


I declared the buttons to have color and specified their size, all in JSX. It was
musch easier than styling a component like that myself. And I only needed to use
inline CSS styling once. If you are looking for a quick and easy solution to your
styling woes, checkout Semantic UI.
