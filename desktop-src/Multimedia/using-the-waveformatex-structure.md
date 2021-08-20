---
title: Usando a estrutura WAVEFORMATEX
description: Usando a estrutura WAVEFORMATEX
ms.assetid: 9b668e1e-cb5f-4065-802b-23974925eacf
keywords:
- áudio waveform, estrutura WAVEFORMATEX
- áudio auxiliar, estrutura WAVEFORMATEX
- Estrutura WAVEFORMATEX
- Dados de áudio do PCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3831d9760580f294573a4bc1bec3aef1d42cf345b2d714a897b22940a89a0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136050"
---
# <a name="using-the-waveformatex-structure"></a>Usando a estrutura WAVEFORMATEX

Para dados de áudio PCM em não mais de dois canais e com exemplos de 8 ou 16 bits, use a estrutura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) para especificar o formato de dados.

O exemplo a seguir mostra como configurar uma estrutura **WAVEFORMATEX** para 11,025 quilohertz (kHz) mono de 8 bits e para estéreo de 44,1 kHz de 16 bits. Depois de configurar **WAVEFORMATEX**, o exemplo chama a função IsFormatSupported para verificar se o dispositivo de saída de forma de onda PCM dá suporte ao formato . O código-fonte para IsFormatSupported é mostrado em um exemplo em Determinando o [suporte ao formato não padrão.](determining-nonstandard-format-support.md)


```C++
UINT wReturn; 
WAVEFORMATEX pcmWaveFormat; 
 
// Set up WAVEFORMATEX for 11 kHz 8-bit mono. 
 
pcmWaveFormat.wFormatTag = WAVE_FORMAT_PCM; 
pcmWaveFormat.nChannels = 1; 
pcmWaveFormat.nSamplesPerSec = 11025L; 
pcmWaveFormat.nAvgBytesPerSec = 11025L; 
pcmWaveFormat.nBlockAlign = 1; 
pcmWaveFormat.wBitsPerSample = 8; 
pcmWaveFormat.cbSize = 0;
 
// See if format is supported by any device in system. 
 
wReturn = IsFormatSupported(&pcmWaveFormat, WAVE_MAPPER); 
 
// Report results. 
 
if (wReturn == 0) 
     MessageBox(hMainWnd, "11 kHz 8-bit mono is supported.", 
       "", MB_ICONINFORMATION); 
else if (wReturn == WAVERR_BADFORMAT) 
     MessageBox(hMainWnd, "11 kHz 8-bit mono NOT supported.", 
       "", MB_ICONINFORMATION); 
else 
     MessageBox(hMainWnd, "Error opening waveform device.", 
       "Error", MB_ICONEXCLAMATION); 
 
// Set up WAVEFORMATEX for 44.1 kHz 16-bit stereo. 
 
pcmWaveFormat.wFormatTag = WAVE_FORMAT_PCM; 
pcmWaveFormat.nChannels = 2; 
pcmWaveFormat.nSamplesPerSec = 44100L; 
pcmWaveFormat.nAvgBytesPerSec = 176400L; 
pcmWaveFormat.nBlockAlign = 4; 
pcmWaveFormat.wBitsPerSample = 16; 
pcmWaveFormat.cbSize = 0;
 
// See if format is supported by any device in the system. 
 
wReturn = IsFormatSupported(&pcmWaveFormat, WAVE_MAPPER); 
 
// Report results. 
 
if (wReturn == 0) 
    MessageBox(hMainWnd, "44.1 kHz 16-bit stereo is supported.", 
      "", MB_ICONINFORMATION); 
else if (wReturn == WAVERR_BADFORMAT) 
    MessageBox(hMainWnd, "44.1 kHz 16-bit stereo NOT supported.", 
      "", MB_ICONINFORMATION); 
else 
    MessageBox(hMainWnd, "Error opening waveform device.", 
      "Error", MB_ICONEXCLAMATION); 

```



 

 