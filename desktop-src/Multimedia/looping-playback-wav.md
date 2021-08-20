---
title: Reprodução em loop (áudio waveform)
description: Reprodução em loop (áudio waveform)
ms.assetid: 8411290b-a3c5-4347-bee3-43c35188f736
keywords:
- waveform audio,looping sounds
- interface waveform-audio, looping de sons
- waveform audio,looping playback
- interface waveform-audio, reprodução em loop
- looping waveform-audio sounds
- looping waveform-audio playback
- Função waveOutWrite
- Função waveOutBreakLoop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d98732ccc0a1d75ad13a10dc881b66a3bb634beab03a95a86a9db5689890979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139307"
---
# <a name="looping-playback"></a>Reprodução em loop

O loop de um som é controlado pelos membros **dwLoops** e **dwFlags** nas estruturas [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) passadas para o dispositivo com a [**função waveOutWrite.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) Use os **sinalizadores WHDR \_ BEGINLOOP** e **WHDR \_ ENDLOOP** no membro **dwFlags** para especificar os blocos de dados inicial e final para looping.

Para fazer loop de um único bloco de dados, especifique os dois sinalizadores para o mesmo bloco. Para especificar o número de loops, use o **membro dwLoops** na estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) para o primeiro bloco no loop.

Você pode chamar a [**função waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop) para interromper um som de loop.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como Waveform-Audio arquivos](playing-waveform-audio-files.md)
</dt> </dl>

 

 
