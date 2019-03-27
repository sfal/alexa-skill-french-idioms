<img src="https://i.imgur.com/66r5b5j.png" title="IdiomiInglesi" alt="IdiomiInglesi">

# Alexa Skill: Idiomi Francesi (French Idioms)

> Alexa Skill written in Python that teaches you French idioms in Italian.

> More than 100 idioms read by the French voice of Alexa. Explanations are provided in Italian.

## Example

```def handle(self, handler_input):
        # type: (HandlerInput) -> Response
        logger.info("In IdiomaHandler")

        random_fact = random.choice(idioms_data.data)
        idiom = random_fact["Idioma"]
        meaning = random_fact["Significato"]

        speech = GET_FACT_MESSAGE + ("<voice name='Celine'><lang xml:lang='fr-FR'>{}</lang></voice>. Significa: {}.".format(idiom, meaning))
```

---

## License

[![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](http://badges.mit-license.org)

- ##[MIT license](http://opensource.org/licenses/mit-license.php)**
- Copyright 2019 © <a href="https://github.com/sfal" target="_blank">sfal</a>.
