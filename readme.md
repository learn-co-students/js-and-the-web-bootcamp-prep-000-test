### Javascript

### Objectives


### The anatomy of a web site

This is Alice.

<iframe height='300' scrolling='no' title='js and the web' src='//codepen.io/flatiron/embed/gmmpoz/?height=300&theme-id=27946&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/flatiron/pen/gmmpoz/'>js and the web</a> by Jeffrey Katz (<a href='http://codepen.io/flatiron'>@flatiron</a>) on <a href='http://codepen.io'>CodePen</a>.
</iframe>

If you click on Alice, you'll notice that Alice has some behavior.  Click on her and find out.  Uh oh, now you've done it.  When Alice is poked, she starts spinning.  She doesn't stop unless clicked again.  It's not a very nice to make a kitten based on the whims of someone's mouse click, so by the end of Alice we'll learn how to stop Alice.  

You'll also learn something about Javascript.

### Discovering Javascript's Powers

In previous lessons, you've seen that HTML structures the content of a webpage.  Now Javascript is a language that adds behavior to a website.  What do we mean by that?

When we say Javascript adds behavior to our HTML, we mean that it selects HTML, listens to events, and adds or remove HTML.  

In this case, the behavior that Javascript added was that when a user clicks on the picture of Alice, Alice spin.  If you look at the Javascript tab, you can see that the code is almost readable.  

```javascript 
let image = document.querySelector("#kitten")

image.onclick = toggleClass;

function toggleClass(){
  if(image.className == 'image'){
      image.className = ''
  } else {
      image.className = 'image'
  }
}
```

We'll spend the next few sections breaking down all of the components involved in the above section.  But for now, let's just go briefly explain what each chunk of code does.  By doing so, we can get a better sense of what exactly we mean when we say Javascript adds behavior to our HTML.



1. Select the image by referencing the id attribute set to kitten, and set it equal to the variable image.

	```javascript 
		let image = document.querySelector("#kitten")
	```

2. Listen for a click event on the image and on a click event call the toggleClass function.

	```javascript
		image.onclick = toggleClass;
	```
	
3. The toggleClass function, which is called every time there is a click event, will remove a css class of image if one exists, and add a css of click of image if none exists.  That css class makes the image spin.

	```javascript
	function toggleClass(){
	  if(image.className == 'image'){
	      image.className = ''
	  } else {
	      image.className = 'image'
	  }
	}
	```

So after exploring the above code, we now have a better sense of what we mean when we say Javascript adds behavior to our HTML.  Specifically Javascript allows us to (1) find HTML (2) listen and respond to specific events on our browser and (3) remove or add HTML.  

  1. Find HTML
	  - Javascript allows us to find specific pieces of HTML so that we can later change that HTML.  Above we found the image of the cat.
  2. Listen and respond to events
	  -  Javascript can listen events like clicking on or hovering over specific elements, the user pressing on specific keys, and many more.  
  3. Remove or add HTML  
	  - Javascript can remove or add HTML.  Above, we added and removed the css class image.  

You are not expected to read and understand the Javascript code at this point in time (you'll get there by going through this course), but do remember that Javascript allows us to find HTML, listen and respond to events, and remove or add HTML.  

Now that you know what Javascript does, you better determine how to change functionality of a website.  This is really nice, because as we'll see in a future lesson, the Javascript code of all websites is exposed and free for you to copy or interact with.  

### Completing Our Task

In this case, we want to get back to our problem of making sure that Alice does not start or stop spinning based on click events.  Ok, so how can we prevent the spinning upon a click.  Well we know that the Javascript code is responsible for behavior like listening to events and adding or changing content.  So what do we do?  We simply remove the Javascript code.  You'll see that after removing Javascript, you can click on Alice as much as you want.  She won't begin to spin.  

That may seem basic, but that's only because we now have understand the responsibilities of Javascript in a website: selecting elements, listening for events, and then adding or removing HTML.  

### Summary

When we view a webpage, we are really viewing three different components.  There is the HTML, which is responsible for the content.  There is CSS, which styles a webpage, and there is Javascript which adds behavior to that HTML.  

When we say Javascript adds behavior we mean three things.  Javascript allows us to:

1. Select certain elements
2. Add or remove HTML from a webpage
3. Listen to events on a webpage.

We still don't know how to implement any of this, by the way.  Don't worry, we will.

### What's next

After knowing how Javascript adds behavior, the next question is what's the big deal?  What's all the fuss about?  Just a bunch of spinning cats?

In the next section, we take a brief tour through the evolution of the web.  Afterwards, we will start writing Javascript to add the types of behavior we learned about above to our code.
