---
title: Usando PlaySound para reproduzir Waveform-Audio arquivos
description: Usando PlaySound para reproduzir Waveform-Audio arquivos
ms.assetid: 8b7d191b-6b0c-4dff-84de-cb3a5c314b80
keywords:
- waveform audio, função PlaySound
- waveform audio, reprodução de arquivos
- waveform audio, extensão de nome de arquivo WAV
- Função PlaySound, reproduzindo arquivos waveform-audio
- reproduzindo arquivos waveform-audio, função PlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa83125665e2a99cc0f47da0893cbc113c0be7a251d62eb66a91e7a1218dac5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687846"
---
# <a name="using-playsound-to-play-waveform-audio-files"></a>Usando PlaySound para reproduzir Waveform-Audio arquivos

A maioria dos arquivos waveform-audio usa o . Extensão de nome de arquivo WAV.

A instrução a seguir reproduz o C: \\ SOUNDS \\ BELLS. Arquivo WAV:


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC); 
```



Se o arquivo especificado não existir ou se o arquivo não se ajustar à memória disponível, [**o PlaySound**](/previous-versions//dd743680(v=vs.85)) reproduzirá o som padrão do sistema. Se nenhum som padrão do sistema tiver sido definido, **PlaySound** falhará sem produzir nenhum som. Se você não quiser que o som padrão do sistema seja reproduzir, especifique o sinalizador NODEFAULT do SND, conforme \_ mostrado no exemplo a seguir:


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC | SND_NODEFAULT); 
```



 

 