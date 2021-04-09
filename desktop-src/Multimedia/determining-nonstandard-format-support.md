---
title: Determinando o suporte a formato não padrão
description: Determinando o suporte a formato não padrão
ms.assetid: a795aa7d-704b-4f03-9815-7a298907bd3d
keywords:
- áudio de forma de onda, suporte a formato não padrão
- áudio auxiliar, suporte a formato não padrão
- áudio de forma de onda, suporte a formato padrão
- áudio auxiliar, suporte a formato padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d0933a82ca8da53c89e1cb8b7d32b40dc89ae0c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007460"
---
# <a name="determining-nonstandard-format-support"></a><span data-ttu-id="1b372-107">Determinando o suporte a formato não padrão</span><span class="sxs-lookup"><span data-stu-id="1b372-107">Determining Nonstandard Format Support</span></span>

<span data-ttu-id="1b372-108">Para ver se um dispositivo dá suporte a um formato específico (padrão ou não padrão), você pode chamar a função [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) com o \_ sinalizador de consulta de formato Wave \_ .</span><span class="sxs-lookup"><span data-stu-id="1b372-108">To see whether a device supports a particular format (standard or nonstandard), you can call the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function with the WAVE\_FORMAT\_QUERY flag.</span></span> <span data-ttu-id="1b372-109">O exemplo a seguir usa essa técnica para determinar se um dispositivo de onda de áudio dá suporte a um formato especificado.</span><span class="sxs-lookup"><span data-stu-id="1b372-109">The following example uses this technique to determine whether a waveform-audio device supports a specified format.</span></span>


```C++
// Determines whether the specified waveform-audio output device 
// supports a specified waveform-audio format. Returns 
// MMSYSERR_NOERROR if the format is supported, WAVEERR_BADFORMAT if 
// the format is not supported, and one of the other MMSYSERR_ error 
// codes if there are other errors encountered in opening the 
// specified waveform-audio device. 
 
MMRESULT IsFormatSupported(LPWAVEFORMATEX pwfx, UINT uDeviceID) 
{ 
    return (waveOutOpen( 
        NULL,                 // ptr can be NULL for query 
        uDeviceID,            // the device identifier 
        pwfx,                 // defines requested format 
        NULL,                 // no callback 
        NULL,                 // no instance data 
        WAVE_FORMAT_QUERY));  // query only, do not open device 
} 
```



<span data-ttu-id="1b372-110">Essa técnica para determinar o suporte a formato não padrão também se aplica a dispositivos de entrada de forma de onda-áudio.</span><span class="sxs-lookup"><span data-stu-id="1b372-110">This technique for determining nonstandard format support also applies to waveform-audio input devices.</span></span> <span data-ttu-id="1b372-111">A única diferença é que a função [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) é usada no lugar de [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) para consultar o suporte de formato.</span><span class="sxs-lookup"><span data-stu-id="1b372-111">The only difference is that the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function is used in place of [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) to query for format support.</span></span>

<span data-ttu-id="1b372-112">Para determinar se um formato de dados de wave-áudio específico é suportado por qualquer um dos dispositivos de wave-áudio em um sistema, use a técnica ilustrada no exemplo anterior, mas especifique a \_ constante do mapeador de ondas para o parâmetro *uDeviceID* .</span><span class="sxs-lookup"><span data-stu-id="1b372-112">To determine whether a particular waveform-audio data format is supported by any of the waveform-audio devices in a system, use the technique illustrated in the previous example, but specify the WAVE\_MAPPER constant for the *uDeviceID* parameter.</span></span>

 

 