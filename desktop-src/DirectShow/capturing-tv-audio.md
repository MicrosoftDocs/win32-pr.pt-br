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
# <a name="capturing-tv-audio"></a><span data-ttu-id="e1489-103">Capturando áudio de TV</span><span class="sxs-lookup"><span data-stu-id="e1489-103">Capturing TV Audio</span></span>

<span data-ttu-id="e1489-104">Para capturar áudio de televisão analógica para um arquivo, use o [filtro de captura de áudio](audio-capture-filter.md).</span><span class="sxs-lookup"><span data-stu-id="e1489-104">To capture audio from analog television to a file, use the [Audio Capture Filter](audio-capture-filter.md).</span></span> <span data-ttu-id="e1489-105">Use o enumerador de dispositivo do sistema para criar o filtro de captura de áudio.</span><span class="sxs-lookup"><span data-stu-id="e1489-105">Use the System Device Enumerator to create the Audio Capture Filter.</span></span> <span data-ttu-id="e1489-106">Pode haver vários dispositivos de captura de áudio no sistema do usuário; o usuário deve selecionar o dispositivo que representa a placa de som.</span><span class="sxs-lookup"><span data-stu-id="e1489-106">There may be several audio capture devices on the user's system; the user must select the device that represents the sound card.</span></span>

<span data-ttu-id="e1489-107">Conecte o PIN de saída da captura de áudio ao filtro Mux:</span><span class="sxs-lookup"><span data-stu-id="e1489-107">Connect the audio capture output pin to the mux filter:</span></span>


```C++
hr = pBuild->RenderStream(
   &PIN_CATEGORY_CAPTURE, // Capture pin.
   &MEDIATYPE_Audio,      // Audio media type.
   pAudioCap,             // Pointer to the audio capture filter.
   NULL,                  // Optional audio compressor filter.
   pMux);                 // Pointer to the mux filter.
```



<span data-ttu-id="e1489-108">Os Pins de entrada não precisam estar conectados a nada.</span><span class="sxs-lookup"><span data-stu-id="e1489-108">The input pins do not have to be connected to anything.</span></span> <span data-ttu-id="e1489-109">Cada pino de entrada representa uma entrada física no dispositivo de captura de áudio.</span><span class="sxs-lookup"><span data-stu-id="e1489-109">Each input pin represents a physical input on the audio capture device.</span></span> <span data-ttu-id="e1489-110">Use a interface [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) para habilitar a entrada que recebe o fluxo de áudio do sintonizador.</span><span class="sxs-lookup"><span data-stu-id="e1489-110">Use the [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) interface to enable the input that receives the audio stream from the tuner.</span></span> <span data-ttu-id="e1489-111">Os Pins de entrada são identificados por nome, como "linha em" ou "áudio de CD".</span><span class="sxs-lookup"><span data-stu-id="e1489-111">The input pins are identified by name, such as "Line In" or "CD Audio."</span></span> <span data-ttu-id="e1489-112">Infelizmente, os nomes podem mudar de um dispositivo para o outro.</span><span class="sxs-lookup"><span data-stu-id="e1489-112">Unfortunately, the names can change from one device to the next.</span></span> <span data-ttu-id="e1489-113">Além disso, placas de sintonizador de TV diferentes usam entradas diferentes para a placa de som.</span><span class="sxs-lookup"><span data-stu-id="e1489-113">Also, different TV tuner cards use different inputs to the sound card.</span></span> <span data-ttu-id="e1489-114">Portanto, cabe ao usuário identificar qual entrada usar.</span><span class="sxs-lookup"><span data-stu-id="e1489-114">Therefore, it is up to the user to identify which input to use.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e1489-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e1489-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1489-116">Áudio de televisão analógica</span><span class="sxs-lookup"><span data-stu-id="e1489-116">Analog Television Audio</span></span>](analog-television-audio.md)
</dt> <dt>

[<span data-ttu-id="e1489-117">Captura de áudio</span><span class="sxs-lookup"><span data-stu-id="e1489-117">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 



