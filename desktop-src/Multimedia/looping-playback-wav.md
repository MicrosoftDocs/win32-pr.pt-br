---
title: Reprodução de loops (áudio de onda)
description: Reprodução de loops (áudio de onda)
ms.assetid: 8411290b-a3c5-4347-bee3-43c35188f736
keywords:
- áudio de onda, sons de loop
- Wave-interface de áudio, looping de sons
- áudio de onda, reprodução em loop
- Wave-interface de áudio, reprodução em loop
- executar loop de Wave-sons de áudio
- execução em loop de Wave-reprodução de áudio
- função waveOutWrite
- função waveOutBreakLoop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c233799e2d4faf8107b4a2a68a261b544ec1274
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "105747733"
---
# <a name="looping-playback"></a>Reprodução de loop

O loop de um som é controlado pelos membros **dwLoops** e **dwFlags** nas estruturas [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) passadas para o dispositivo com a função [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) . Use os sinalizadores **WHDR \_ BEGINLOOP** e **WHDR \_ ENDLOOP** no membro **dwFlags** para especificar os blocos de dados inicial e final para looping.

Para repetir um único bloco de dados, especifique os dois sinalizadores para o mesmo bloco. Para especificar o número de loops, use o membro **dwLoops** na estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) para o primeiro bloco no loop.

Você pode chamar a função [**waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop) para interromper um som de loop.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Executando Waveform-Audio arquivos](playing-waveform-audio-files.md)
</dt> </dl>

 

 
