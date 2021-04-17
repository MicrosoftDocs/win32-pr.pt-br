---
description: Capturando áudio de TV
ms.assetid: c0c62a8e-ab16-4617-936c-b64e6e3865b4
title: Capturando áudio de TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 138ce631aedf12ddfb52be92d08ffb47da0cbdec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105811767"
---
# <a name="capturing-tv-audio"></a>Capturando áudio de TV

Para capturar áudio de televisão analógica para um arquivo, use o [filtro de captura de áudio](audio-capture-filter.md). Use o enumerador de dispositivo do sistema para criar o filtro de captura de áudio. Pode haver vários dispositivos de captura de áudio no sistema do usuário; o usuário deve selecionar o dispositivo que representa a placa de som.

Conecte o PIN de saída da captura de áudio ao filtro Mux:


```C++
hr = pBuild->RenderStream(
   &PIN_CATEGORY_CAPTURE, // Capture pin.
   &MEDIATYPE_Audio,      // Audio media type.
   pAudioCap,             // Pointer to the audio capture filter.
   NULL,                  // Optional audio compressor filter.
   pMux);                 // Pointer to the mux filter.
```



Os Pins de entrada não precisam estar conectados a nada. Cada pino de entrada representa uma entrada física no dispositivo de captura de áudio. Use a interface [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) para habilitar a entrada que recebe o fluxo de áudio do sintonizador. Os Pins de entrada são identificados por nome, como "linha em" ou "áudio de CD". Infelizmente, os nomes podem mudar de um dispositivo para o outro. Além disso, placas de sintonizador de TV diferentes usam entradas diferentes para a placa de som. Portanto, cabe ao usuário identificar qual entrada usar.


```C++
IEnumPins *pEnum = NULL;
hr = pAudioCap->EnumPins(&pEnum);
if (SUCCEEDED(hr))
{
    IPin *pPin = NULL;
    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        IAMAudioInputMixer *pMix;
        hr = pPin->QueryInterface(IID_IAMAudioInputMixer, (void**)&pMix);
        if (SUCCEEDED(hr))
        {
            // Use IPin::QueryPinInfo to get the pin name.
            pPin->Release();
            if (...) // If the user selects this pin:
            {
                pMix->put_Enable(TRUE);
                pMix->put_MixLevel(1.0);
                pMix->Release();
                break;
            }
            pMix->Release();
        }
    }
}
pEnum->Release();
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Áudio de televisão analógica](analog-television-audio.md)
</dt> <dt>

[Captura de áudio](audio-capture.md)
</dt> </dl>

 

 



