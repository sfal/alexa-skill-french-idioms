<a href="https://www.amazon.it/dp/B07Q3XRLMP/ref=sr_1_2?__mk_it_IT=%C3%85M%C3%85%C5%BD%C3%95%C3%91&keywords=idiomi+inglesi&qid=1553708009&s=alexa-skills&sr=1-2-catcorr"><img src="https://i.imgur.com/66r5b5j.png" title="IdiomiFrancesi" alt="IdiomiFrancesi"></a>

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

## Now supports Alexa Presentation Language

```handler_input.response_builder.speak(speech).add_directive(
     RenderDocumentDirective(
        token="idiomiToken",
        document=_load_apl_document("apl-idioma.json"),
        datasources={
                'idiomaTemplateData': {
                        'type': 'object',
                        'properties': {
                             'text': "{}".format(idiom)
                         }
                },
                 'backgroundsData': {
                 'image': "{}".format(image)
                  }
                }
            ))
```

---

## Enable Skill (Italy only)


- <a href="https://www.amazon.it/dp/B07Q3XRLMP/ref=sr_1_2?__mk_it_IT=%C3%85M%C3%85%C5%BD%C3%95%C3%91&keywords=idiomi+inglesi&qid=1553708009&s=alexa-skills&sr=1-2-catcorr" target="_blank">Idiomi Francesi on Amazon.it</a>

## License

[![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](http://badges.mit-license.org)

- ##[MIT license](http://opensource.org/licenses/mit-license.php)**
- Copyright 2019 © <a href="https://github.com/sfal" target="_blank">sfal</a>.
