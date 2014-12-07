Trenitalia Frecciargento API
============================

Le API sono accessibili dalla wifi del treno

API Endpoint Reference
======================

* **Realtime GPS data**
  * (GET) http://portalefrecciargento.it/json/infoGPSAction.action
* **Train infos**
  * (GET) http://portalefrecciargento.it/json/headerInfoAction.action
* **Next station name**
  * (GET) http://portalefrecciargento.it/json/m53StationNameAction.action
* **Tabellone orario partenze dalla stazione di destinazione**
  * (GET) http://portalefrecciargento.it/json/m53ListAction.action
* **Informazioni meteo presso le stazioni di fermata**
  * (GET) http://portalefrecciargento.it/json/meteoFermateAction.action
* **Informazioni meteo presso le stazioni di fermata (JPEG)**
  * (GET) http://portalefrecciargento.it/Dove6OndeWeb/meteoAction.action?type=detail

Example
=======

**Realtime GPS data**

http://portalefrecciargento.it/json/infoGPSAction.action

```json
{

    "updateMap": true,
    "lon": 14.45336,
    "dir": 223.74554837740197,
    "speed": 138,
    "alt": 66,
    "lat": 41.11923

}
```


**Train infos**

http://portalefrecciargento.it/json/headerInfoAction.action

```json
{

    "date": "07/12/2014",
    "time": "21:00",
    "categoria": "F_ARGENTO",
    "codiceCorsa": "9358",
    "origine": "LECCE",
    "destinazione": "ROMA TERMINI"

}
```


**Next station name**

http://portalefrecciargento.it/json/m53StationNameAction.action

```json
{

    "station": "CASERTA"

}
```


**Tabellone orario partenze dalla stazione di destinazione**

http://portalefrecciargento.it/json/m53ListAction.action

```json
{

    "rows": [
        {
            "binario": "",
            "categoria": "REGIO_FAST",
            "numTreno": "3342",
            "destinazione": "FIUMICINO AEROP.",
            "orario": "22:20",
            "ritardo": ""
        },
        {
            "binario": "",
            "categoria": "ICN",
            "numTreno": "1959",
            "destinazione": "SIRACUSA",
            "orario": "22:26",
            "ritardo": ""
        },
        {
            "binario": "",
            "categoria": "REGIONALE",
            "numTreno": "7565",
            "destinazione": "Frosinone",
            "orario": "22:28",
            "ritardo": ""
        },
        {
            "binario": "",
            "categoria": "ICN",
            "numTreno": "774",
            "destinazione": "TRIESTE CENTRALE",
            "orario": "22:35",
            "ritardo": ""
        },
        {
            "binario": "",
            "categoria": "REGIO_FAST",
            "numTreno": "2492",
            "destinazione": "FOLIGNO",
            "orario": "22:50",
            "ritardo": ""
        },
        {
            "binario": "",
            "categoria": "REGIO_FAST",
            "numTreno": "3344",
            "destinazione": "FIUMICINO AEROP.",
            "orario": "22:50",
            "ritardo": ""
        }
    ]

}
```


**Informazioni meteo presso le stazioni di fermata**

http://portalefrecciargento.it/json/meteoFermateAction.action

```json
{

    "rows": [
        {
            "visibilita": "Buona",
            "time": "16:53",
            "descrizione": "LECCE",
            "vento": "Brezza leggera",
            "ccr": "S11145",
            "temperatura": "16",
            "tematismo": "nuvoloso.png",
            "tipoTempo": "Poco nuvoloso"
        },
        {
            "visibilita": "Buona",
            "time": "17:12",
            "descrizione": "BRINDISI",
            "vento": "n/d",
            "ccr": "S11136",
            "temperatura": "15",
            "tematismo": "nuvoloso.png",
            "tipoTempo": "Poco nuvoloso"
        },
        {
            "visibilita": "Buona",
            "time": "18:13",
            "descrizione": "BARI C.LE",
            "vento": "Brezza leggera",
            "ccr": "S11119",
            "temperatura": "13",
            "tematismo": "nuvoloso_luna.png",
            "tipoTempo": "Poco nuvoloso"
        },
        {
            "visibilita": "Buona",
            "time": "18:43",
            "descrizione": "BARLETTA",
            "vento": "Brezza leggera",
            "ccr": "S11108",
            "temperatura": "13",
            "tematismo": "nuvoloso_luna.png",
            "tipoTempo": "Poco nuvoloso"
        },
        {
            "visibilita": "Buona",
            "time": "19:13",
            "descrizione": "FOGGIA",
            "vento": "Brezza leggera",
            "ccr": "S11100",
            "temperatura": "13",
            "tematismo": "nuvoloso_luna.png",
            "tipoTempo": "Nubi sparse"
        },
        {
            "visibilita": "Buona",
            "time": "20:29",
            "descrizione": "BENEVENTO",
            "vento": "n/d",
            "ccr": "S09311",
            "temperatura": "9",
            "tematismo": "nuvoloso_luna.png",
            "tipoTempo": "Poco nuvoloso"
        },
        {
            "visibilita": "Buona",
            "time": "21:08",
            "descrizione": "CASERTA",
            "vento": "Brezza leggera",
            "ccr": "S09211",
            "temperatura": "10",
            "tematismo": "nuvoloso_luna.png",
            "tipoTempo": "Poco nuvoloso"
        },
        {
            "visibilita": "Buona",
            "time": "22:20",
            "descrizione": "ROMA TERMINI",
            "vento": "Brezza leggera",
            "ccr": "S08409",
            "temperatura": "12",
            "tematismo": "pioggia.png",
            "tipoTempo": "Pioggia e schiarite"
        }
    ]

}
```


**Informazioni meteo presso le stazioni di fermata _(base64 encoded JPEG)_**

http://portalefrecciargento.it/Dove6OndeWeb/meteoAction.action?type=detail

```
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SAbX9yK4a8OWV+51UpXRo0UVTvtTtNOi33MoXPRRyx+grE0LlMdFkjZGGVYEEeorkLzxHfXh22a/ZYv77DLn8O1RR67q8IAMsUw/20wf0rRUptXsQ6kU7XKUkBs724syciJvlPselLTEDs0ksxzLIxZjT67aaairnNNpy0CiiirJCiiigAooooAeOlFA6UUANPWkpT1pKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiionuUSYRk/MaTaW4JN7EtFFFMAooooAKa8iRjLMBTq2vC1pbTpPPKge5SQqdwztHbFZVanIrl048zMDz1Y7QGLHgKF5Ndn4et5LbR4kmQo5JYqeoya0hGgYEIoI74p9cc6jnudEYKOw12WNWdjhVGST2FefXFwdS1Ca9cZVjtjB7KK7PWzjRL0g4PlNXEQAC3jx/dFaUIpyuyarsiSiiiu05gooooAKKKKACiiigAooooAeOlFA6UUANPWkpT1pKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACobiJXRn2AsoyD3qaik1dWGnZ3K9uUSR443LoACpJ56c1YqNYI0mMoGGIwcdKkqYRcY2Y5tN3QUUUZGcZGfTvVkhW34ThYvd3OcIzBAPXHesJBJcS+RbRtLKey9B9a7fSbI6fpsUBxvAJcjuTXJiJp+6jejFrVl6iiori4itYGmmcJGoyWNcxuVNc/5Ad7/ANcm/lXEQf6iP/dFXtT1ifWCY490Nlnp0aQe9VAAqgAYA4ArroQa1Zz1ZJ6C0UUV0mIUUUUAFFFFABRRRQAUUUUAPHSigdKKAGnrSUp60lABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFRvMiSrGTgtnHpRPL5ULOOSBwKlyVmxpMkoJx1qO3kaWBXYYJHPatHSNK/taZpJSRaRnGBwXNTOooxuVGDk7GcJ0LhcnB4DY4NSE4BJ7V2l1pFpdaf9j8pUjA+TaPun1Fc/F4Wvmfy5rm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
```

