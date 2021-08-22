---
description: Capturando áudio de TV
ms.assetid: c0c62a8e-ab16-4617-936c-b64e6e3865b4
title: Capturando áudio de TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d699533480bdeaaa528e362c0773e9df8100fda3dc2195a65c055ae7f7d5bb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641006"
---
# <a name="capturing-tv-audio"></a>Capturando áudio de TV

Para capturar áudio da tv analoga para um arquivo, use o [Filtro de Captura de Áudio](audio-capture-filter.md). Use o Enumerador de Dispositivo do Sistema para criar o Filtro de Captura de Áudio. Pode haver vários dispositivos de captura de áudio no sistema do usuário; o usuário deve selecionar o dispositivo que representa a placa de som.

Conexão o pino de saída da captura de áudio para o filtro mux:


```C++
hr = pBuild->RenderStream(
   &PIN_CATEGORY_CAPTURE, // Capture pin.
   &MEDIATYPE_Audio,      // Audio media type.
   pAudioCap,             // Pointer to the audio capture filter.
   NULL,                  // Optional audio compressor filter.
   pMux);                 // Pointer to the mux filter.
```



Os pinos de entrada não devem ser conectados a nada. Cada pino de entrada representa uma entrada física no dispositivo de captura de áudio. Use a interface [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) para habilitar a entrada que recebe o fluxo de áudio do ajuste. Os pinos de entrada são identificados por nome, como "Line In" ou "CD Audio". Infelizmente, os nomes podem mudar de um dispositivo para outro. Além disso, diferentes cartões de ajuste de TV usam entradas diferentes para a placa de som. Portanto, é responsabilidade do usuário identificar qual entrada usar.


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

[Áudio de tv análogo](analog-television-audio.md)
</dt> <dt>

[Captura de áudio](audio-capture.md)
</dt> </dl>

 

 



