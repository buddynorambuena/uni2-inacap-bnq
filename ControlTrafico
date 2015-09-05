FORMAT: 1A
HOST: http://polls.apiblueprint.org/

# Sistema control de tráfico urbano

qwdqwdq

## Recurso video [/video]

### Listar videos [GET]

+ Response 200 (application/json)

        [
            {
                "atributo_video": "Favourite programming language?",
                "atributo_video1": "2015-08-05T08:40:51.620Z",
                "choices": [
                    {
                        "choice": "Swift",
                        "votes": 2048
                    }, {
                        "choice": "Python",
                        "votes": 1024
                    }, {
                        "choice": "Objective-C",
                        "votes": 512
                    }, {
                        "choice": "Ruby",
                        "votes": 256
                    }
                ]
            }
        ]

### Nuevo Video [POST]

descripción del video bla bla bla

+ Request (application/json)

        {
            "atributo_video1": "Favourite programming language?",
            "choices": [
                "Swift",
                "Python",
                "Objective-C",
                "Ruby"
            ]
        }

+ Response 201 (application/json)

    + Headers

            Location: /video/2

    + Body

            {
                "atributo_video_id2": "Favourite programming language?",
                "atributo_video_id2": "2015-08-05T08:40:51.620Z",
                "choices": [
                    {
                        "choice": "Swift",
                        "votes": 0
                    }, {
                        "choice": "Python",
                        "votes": 0
                    }, {
                        "choice": "Objective-C",
                        "votes": 0
                    }, {
                        "choice": "Ruby",
                        "votes": 0
                    }
                ]
            }

## Recurso otros [/otros]

### Listar otros [GET]
+ Response 200 (application/json)

        [
            {
                "variable": "hola mundo",
                "publicado": "2015-08-05T08:40:51.620Z"
            }
        ]
