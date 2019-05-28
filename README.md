# hello-boot-camp

Hello Ryan!

Here is my recording of my progress through the Alchemy Learning Readiness Exercise:

5/23
I saw that the exercise was in GitHub. I played with the views that were available for the readme file: raw, blame, history, normal. 
I wanted to learn how to put my notes into GitHub - I wanted to practice. 
I don’t know how to create my own repository on GitHub. I need to research. 
I went through the tutorial on the GitHub front page. It turns out GitHub on my phone does not have a good way to create repositories, but on my iPad it is very easy! Now I have a readme file.

I looked at the friends.json file. What format is this file? After sone research on wikipedia I learned that JSON is its own programming language, and the data in friends.json is an array of objects. Objects are collections of name-value pairs.

5/27
Now on to the JavaScript (take 2 because doing this on my phone is a bad idea, but it’s what I have right now. And, the notes I took last night are now gone because I didn’t commit. Local storage of files isn’t great on phones. Wah wah)

We create a constant to point at the unordered friends list from the page. We are not modifying the location of the list, just adding list items to it. Between this and the desire to locally scope the definition of ul (a pretty generic variable name), this is why we declare it as “const”.
- I had to look up the scoping details and the details around list references in js (modifiable v. static pointer)

The fetch command is used to get the json file from local storage. I don’t know how to guarantee the file is in the same directory as the html.

I’ve never seen fetch before, so I’ll need to look that up. Is there a searchable manual of built-in js function calls? Does this one come from a library? I don’t see any references or includes. 
- fetch is an API but the important thing here is the object type returned by Fetch is a Response object. It has a json method to parse a stream that is json formatted. It returns a “promise”. Is this an object as well?

I’ve never seen .then before. Need to learn about that. ... time passes ... whoa. There’s a lot to learn. I’m on developer.mozilla.org and every link of interest leads to 2 or more LOI’s. I found a browser compatibility table and it blows my mind to think about the developers who work to support all these browsers. 
- so I’m learning about promises but it doesn’t make sense in context. But now I’m reading about chaining. This is sweet. I’ve experienced the “classic callback pyramid of doom” before and I was able to intuitively read the code written with the .then approach even though it’s taking me some hours to dissect the full meaning of each line. 
- the first .then returns a promise of the object created by .json() method. Actually, this is a “json” object (assuming the .json method doesn’t fail in some way ... in this case the second .then is never executed.)
- the second .then is confusing to me. I’m not clear why the json object has a .foreach method. I’m not entirely sure that the promise object received here is the object I think it is. 
- it seems that a cleaner version of this code would have a .catch implemented after the 2nd .then segment. This is shown in every example I’m seeing online for chaining .then calls. 

Finally, I need to brush up on the arrow operator. Okay. Brush up is the wrong word. There’s a lot to consider. I’m reading from FreeCodeCamp - when and why to use ES6 arrow functions and when you shouldn’t. 
- the complexity of this short bit of code is with the combination of .then and the arrow operator. The base implementation of arrow operator is as “var addFriends = (friendsParameter) => {statements}”. We can omit the parens around the parameter because there is only one. And because .then provides a promise as input, we can omit the “var variable =“. 





