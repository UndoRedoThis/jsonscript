# JSONScript

### What the hell is JSONScript?

Good thing you're asking, my dear. JSONScript is a Javascript API which allows you to make your code look beautiful thanks to the power of JSON. Basically the API introduces one new object which is responsible of handling JSON formatted pieces of code and converting them into valid JS code. Sounds great, doesn't it? One function to memorize and you're almost done.

#### Yeah, but how do I use it?

`JSONScript.parse( jsonArray [, scope ] );`

That's the function I told you about. The first parameter is the array of JSON object which should be parsed by the API itself. The second parameter allows you to define a scope to which the returned and evaluated JSON objects should be assigned to. However, the latter is optional. If there's no scope set, then the API will add it to the global scope automatically.

#### Sounds legit. Why should I use it?

Thanks to the API, you don't need to worry about types in the slightest since everything is a string. Yes, you heard me right. No need to memorize redundant types if there's an API which can do the same for you. Look at the following example.

```
// This is the JSONScript way of handling different types.

JSONScript.parse([
    {
        type : "number",
        name : "myAwesomeNumber",
        value : "22.4"
    }
);

// And this is the JS way of handling different types.

var myAwesomeNumber = 22.4;
```

Assuming `myAwesomeNumber` isn't precisely a float but an integer, how can you even know if you hand the second section of the example above to someone who is completely unfamiliar with Javascript? Floats take up way more space than integers do and if we want to optimize stuff, then float which could be integers should be converted into integers. So what does that mean?

```
JSONScript.parse([
    {
        type : "number",
        name : "myAwesomeInteger",
        value : "47"
    }
);

// and just for comparison

var myAwesomeIDontReallyKnowWhatTypeThisIsNumberFloatIntegerThingy = 47;
```

You see, using JSONScript gives you the certanity that the number returned after parsing the "number" JSON object is indeed an integer and not a float whereas we don't know if we use Javascript and give it a number to work with. That way we can save valuable processing time.

And that's not the only example. Imagine the possibilities using this API for every one of your projects.

#### You're beating around the bush

That's because you don't work at an enterprise which uses high-quality software like the JSONScript API. They know how to cherish this intelectual masterpiece.

#### Okay, okay, okay. Is there any way I can read more about this?

Yes, you can on the official website. Everything you'll ever need to know is located there.

http://undoredothis.github.io/jsonscript

#### Will there be a download too?

There is.

#### Can I go home now?

You may.
