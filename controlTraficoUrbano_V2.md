FORMAT: 1A
HOST: http://private-4e90b-ctrltraficourbano.apiary-mock.com

# Sistema Control Tráfico Urbano (SIS_CTU V2)
Administración de cámaras que almacenan datos del tráfico en tiempo real.

## Videos [/version2/videos]

+ Parameters
    + id (required, int) ... PK video

+ Model (application/hal+json)
    + Body

            {
                "idVideo": 1,
                "timestamp_inicio": "15-09-2015 08:00",
                "timestamp_fin": "16-09-2015 08:00",
                "size_video": "2840Mb"
            }

## Buscar Video [GET /version2/videos/{id}]

+ Response 200 (application/json)

    [Videos][]

+ Response 404 (application/json)

        {
            "Error"
        }

+ Response 404

        {
            "Error"
        }

+ Response 400

        {
            "Error"
        }

## Eliminar Video [DELETE /version2/videos/{id}]

+ Response 200

        {
            "result": True,
            "message": "Video Eliminado"
        }

    [Videos][]


# Lista de videos [/version2/videos]

+ Model (application/hal+json)

    + Body

            {
                 "videos":[
                    {
                        "id": 1,
                        "timestamp_inicio": "15-09-2015 08:00",
                        "fin_transmision": "16-09-2015 08:00",
                        "size_video": "2840Mb"
                    },
                    {
                        "id": 2,
                         "timestamp_inicio": "15-09-2015 08:00",
                        "fin_transmision": "16-09-2015 08:00",
                        "tamano_video": "2840Mb"
                    },{
                        "id": 3,
                         "timestamp_inicio": "15-09-2015 08:00",
                        "fin_transmision": "16-09-2015 08:00",
                        "tamano_video": "2840Mb"
                    },
                    {
                        "id": 4,
                        "timestamp_inicio": "15-09-2015 08:00",
                        "fin_transmision": "16-09-2015 08:00",
                        "tamano_video": "2840Mb"
                    }
                ]
            }


## Obtener lista de videos [GET]

+ Response 200

    [Lista de videos][]


## Camaras [/version2/camaras]

+ Parameters
    + id (required, int) ... PK Cámara

+ Model (application/hal+json)

    + Body

            {
                "id": 1,
                "marca_Camara":"Camara x HD Pro 1",
                "ip_Camara":"192.100.1.1",
                "configuración":{
                    "brillo": 10,
                    "calidad": "720p"
                }
            }

## Buscar Cámara [GET /version2/camaras/{id}]

+ Response 200 (application/json)

    [Camaras][]

+ Response 404 (application/json)

        {
            "Error"
        }

## Eliminar Cámara [DELETE /version2/camaras/{id}]

+ Response 200

        {
            "result": True,
            "message": "Cámara eliminada"
        }

## Nueva Cámara [POST /version2/camaras]

+ Request (application/json)

        {
            "marca_Camara":"Camara x HD Pro 2",
            "brillo": 1,
            "calidad": "720p"
        }

+ Response 201

    [Camaras][]

+ Response 400

        {
            "Error"
        }

# Lista de camaras [/version2/camaras]

+ Model (application/hal+json)

    + Body

      {
           "camaras":[
              {
                "id": 1,
                "marca_Camara":"Camara x HD Pro 1",
                "ip_Camara":"192.100.1.2",
                "configuración":{
                    "brillo": 10,
                    "calidad": "720p",
                    "color":"rgba(0,0,0)",
                    "contraste":"30"
                }
              },
              {
                "id": 2,
                "marca_Camara":"Camara x HD Pro 1",
                "ip_Camara":"192.168.1.101",
                "configuración":{
                    "brillo": 10,
                    "calidad": "720p",
                    "color":"rgba(0,0,0)",
                    "contraste":"30"
                }
              }
          ]
      }

## Obtener lista de cámaras [GET]

+ Response 200

    [Lista de camaras][]

# Transmision [/version2/camaras/{id}/transmision]

+ Model (application/hal+json)

    + Body

            {
                "id": 1,
                "marca_Camara":"Camara x HD Pro 1",
                "ip_Camara":"192.168.1.100",
                "configuración":{
                    "brillo": 10,
                    "calidad": "720p",
                    "color":"rgba(0,0,0)",
                    "contraste":"30"
                },
                "Video":{
                    "id": 1
                },
                "broadcast":{
                    "id": 1,
                    "timestamp_inicio":"15-09-2015 15:00"
                }
            }


## Buscar transmisión video [GET]

+ Response 200

    [Transmision][]

##Grabación en Disco [/version2/graba-disco]

+ Parameters
    + id (required, int) ... PK Video

+ Model (application/hal+json)

    + Body

            {
                "id": 1,
                "timestamp_inicio":"15-09-2015 18:00",
                "tipo_fichero":"mpg",
                "video":{
                    "id": 2,
                    "timestamp_inicio": "15-09-2015 00:00",
                    "timestamp_fin": "16-09-2015 00:00",
                    "tamano_video": "2840Mb"
                }
            }

## Estado Grabación [GET /version2/graba-disco/{id}]

+ Response 200 (application/json)

    [Grabación en Disco][]

+ Response 404 (application/json)

        {
            "Error"
        }

## Nueva Grabación en CD [POST /version2/graba-cd]

+ Request (application/json)

        {
            "tipo_fichero":"mpg",
            "id_video":1
        }

+ Response 201

    [Grabación en Disco][]

+ Response 400

        {
            "Error"
        }
