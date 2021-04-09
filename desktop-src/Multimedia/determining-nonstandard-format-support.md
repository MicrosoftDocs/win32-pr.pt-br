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
# <a name="determining-nonstandard-format-support"></a>Determinando o suporte a formato não padrão

Para ver se um dispositivo dá suporte a um formato específico (padrão ou não padrão), você pode chamar a função [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) com o \_ sinalizador de consulta de formato Wave \_ . O exemplo a seguir usa essa técnica para determinar se um dispositivo de onda de áudio dá suporte a um formato especificado.


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



Essa técnica para determinar o suporte a formato não padrão também se aplica a dispositivos de entrada de forma de onda-áudio. A única diferença é que a função [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) é usada no lugar de [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) para consultar o suporte de formato.

Para determinar se um formato de dados de wave-áudio específico é suportado por qualquer um dos dispositivos de wave-áudio em um sistema, use a técnica ilustrada no exemplo anterior, mas especifique a \_ constante do mapeador de ondas para o parâmetro *uDeviceID* .

 

 