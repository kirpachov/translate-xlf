# translate-xlf
Ruby gem that uses OpenAI API to translate xlf files in many laguages.

> You will have to generate an OpenAPI key. We'll use YOUR key to make API requests.

## Basics
Given a .xlf file that we will call `source`, it will create a translated version of the file for the required locales.
```
translate-xlf <source> [outfile] --locales=en,es,de --source-locale=it
```

## Caching / Importing translations
Every translation that was made should not be made again.
For this reason, we must be able to cache translations while making them, and import translations manually.
You must be able to use translations made in another computer.
For this reason, export functionalities are mandatory as well.


## Community-based translations
You will be able to use other people's translations as long as you accept to share yours.

How it works:
When you need a translation, we'll check if there is one available for that exact string for that language. If it's available, you can use that one.
Otherwise, if the translation was not found, you will have to translate it with OpenAI APIs. After you translated it, we'll save that translation in our community database, in order to allow other people to use it.

In this way we'll be able to save money and share a large amuont of translations.

In short, common words and senteces won't require any request.
