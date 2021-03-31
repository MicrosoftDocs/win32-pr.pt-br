---
title: Usando o PlaySound para reproduzir arquivos de Waveform-Audio
description: Usando o PlaySound para reproduzir arquivos de Waveform-Audio
ms.assetid: 8b7d191b-6b0c-4dff-84de-cb3a5c314b80
keywords:
- áudio de onda, função PlaySound
- áudio de onda, reproduzindo arquivos
- áudio de onda, extensão de nome de arquivo WAV
- Função PlaySound, tocando em formato de onda-arquivos de áudio
- executando formato de onda-arquivos de áudio, função PlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9d5dde46827b7892217f760c749e75e19f368f5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917297"
---
# <a name="using-playsound-to-play-waveform-audio-files"></a>Usando o PlaySound para reproduzir arquivos de Waveform-Audio

A maioria dos arquivos de som de onda usa o. Extensão de nome de arquivo WAV.

A instrução a seguir desempenha os \\ sinos C: Sounds \\ . Arquivo WAV:


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC); 
```



Se o arquivo especificado não existir, ou se o arquivo não couber na memória disponível, o [**PlaySound**](/previous-versions//dd743680(v=vs.85)) reproduzirá o som do sistema padrão. Se nenhum som do sistema padrão tiver sido definido, o **PlaySound** falhará sem produzir nenhum som. Se você não quiser que o som do sistema padrão seja reproduzido, especifique o \_ sinalizador SND nodefault, conforme mostrado no exemplo a seguir:


```C++
PlaySound("C:\\SOUNDS\\BELLS.WAV", NULL, SND_SYNC | SND_NODEFAULT); 
```



 

 