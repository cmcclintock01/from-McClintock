# Corben McClintock

My favorite movie is Star Wars: A New Hope. 
My parents started me out on the older star wars movies even though the new ones were coming out as I was growing up. 
It was one of the first movies that I remember watching and I loved getting introduced to all the characters. 


![Image of Myself](selfphoto.jpg)

---

This table is going to be giving you some recommendations.
You will get a title of a book, song, or video, a little description on why I recommend it, and the creator of the media.

| Name | Description | Creator |
| --- | --- | --- |
| Low | It is a very good song. It's R&B so if you are needing to wind down it can really help. | SZA |
| Star Wars | The star wars movies are a great way to spend free time. They take you on a journey with an amazing story. | George Lucas | 
| Creed | The Creed movies show you a lot about working hard and are a great set of motivational movies. It can help inspire you to maybe start working out if you don't or just be more involved in anything you are interested in. | Ryan Coogler |
| Diamonds | There is a really good beat to the song and Frank Ocean is an amazing vocalist so the song sounds really nice. | Frank Ocean |

---

## Favorite Quotes

> You miss 100% of the shots you don't take.

*Wayne Gretzky*

> Three can keep a secret, if two of them are dead.

*Benjamin Franklin*

---

# Code

This code will read chunks of input and write to the destination.
~~~
const http = require('http');
const fileSystem = require('fs');

http.createServer((request, response) => {
	// This opens up the writeable stream to `output`
	const writeStream = fileSystem.createWriteStream('./output');

	// This pipes the POST data to the file
	request.pipe(writeStream);

	// After all the data is saved, respond with a simple html form so they can post more data
	request.on('end', function() {
		response.writeHead(200, {
			"content-type": "text/html"
		});
		response.end('[-- Insert generic html FORM element here --]');
	});

	// This is here incase any errors occur
	writeStream.on('error', function(err) {
		console.log(err);
	});
}).listen(8080); 
~~~
Here is where I got the code <https://code.pieces.app/collections/node-js>

