FORMAT: 1A
HOST: http://polls.apiblueprint.org/

# Sistema control de tráfico urbano

Administración de cámaras que almacenan datos del tráfico en tiempo real.

## Camara Trafico Urbano [/videos]

### Mostrar Camaras [GET]

+ Response 200 (application/json)

        [
            {
                "atributo_video": "Favourite programming language?",
                "atributo_video1": "2015-08-05T08:40:51.620Z",
                 "videos": [
                    {
                        "id": 1,
                        "url_transmision":"http://ejemplovideo/broadcast/1",
                        "inicio_transmision":"05-09-2015 11:00",
                        "camara":
                        {
                            "idCamara": 1,
                            "marca":"Camara x HD Pro 1",
                            "ipCamara":"192.168.40.1",
                            "status":"online",
                            "configuracion":
                            {
                                "brillo": 10,
                                "calidad": "720p",
                                "color":"rgba(0,0,0)",
                                "contraste":"30"
                            }
                        }
                    },
                    {
                        "id": 2,
                        "url_transmision":"http://ejemplovideo/broadcast/2",
                        "inicio_transmision":"05-09-2015 11:00",
                        "camara":{
                            "idCamara": 2,
                            "marca":"Camara x HD Pro 2",
                            "ipCamara":"192.168.40.2",
                            "status":"online",
                            "configuracion":{
                                "brillo": 10,
                                "calidad": "720p",
                                "color":"rgba(0,0,0)",
                                "contraste":"30"
                            }
                        }
                    },
                    {
                        "id": 3,
                        "url_transmision":"http://ejemplovideo/broadcast/3",
                        "inicio_transmision":"05-09-2015 11:00",
                        "camara":{
                            "idCamara": 3,
                            "marca":"Camara x HD Pro 3",
                            "ipCamara":"192.168.40.3",
                            "status":"online",
                            "configuracion":{
                                "brillo": 10,
                                "calidad": "720p",
                                "color":"rgba(0,0,0)",
                                "contraste":"30"
                            }
                        }
                    }
                ]
            }
        ]

### Nueva Camara [PUT]

+ Response 200 (application/json)

        [
            {
                "atributo_video": "Favourite programming language?",
                "atributo_video1": "2015-08-05T08:40:51.620Z",
                 "videos": [
                    {
                        "id": 4,
                        "url_transmision":"http://ejemplovideo/broadcast/1",
                        "inicio_transmision":"05-09-2015 11:00",
                        "camara":
                        {
                            "idCamara": 4,
                            "marca":"Camara x HD Pro 4",
                            "ipCamara":"192.168.40.4",
                            "status":"online",
                            "configuracion":
                            {
                                "brillo": 10,
                                "calidad": "720p",
                                "color":"rgba(0,0,0)",
                                "contraste":"30"
                            }
                        }
                    }
                ]
            }
        ]
        
## Grabar Video [/grabar]

### Grabar Video [POST]
+ Response 200 (application/json)

        [
            {
                "idCamara": 1,
                "fechaInicioGrabacion": "2015-09-06 08:40:51",
                "fechaTerminoGrabacion": "2015-09-06 08:45:51",
                "formatoCompresion":"Mp4"
            }
        ]
