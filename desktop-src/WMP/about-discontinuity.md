---
title: Sobre a descontinuidade
description: Sobre a descontinuidade
ms.assetid: 29210758-a1e6-47f2-9428-38f79623fbca
keywords:
- plug-ins Windows Media Player, DSP de áudio
- plug-ins, DSP de áudio
- plug-ins de processamento de sinal digital, descontinuidade de áudio
- Plug-ins do DSP, descontinuidade de áudio
- plug-ins do DSP de áudio, descontinuidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40de4c75c2d17699f0c72416873d64177e47d81761b27e5ffd465d89c9ecb9c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903566"
---
# <a name="about-discontinuity"></a>Sobre a descontinuidade

a qualquer momento, Windows Media Player pode sinalizar uma interrupção no fluxo de entrada chamando o método **IMediaObject::D iscontinuity** . Isso ocorre rotineiramente no início e no final de um fluxo e também antes de cada operação de busca ou quando o conteúdo de streaming é interrompido por qualquer motivo. o plug-in DSP de exemplo que o assistente de plug-in do Windows Media Player gera não precisa lidar com descontinuidades pelos seguintes motivos:

-   As amostras de PCM são atômicas, o que significa que elas podem ser processadas sem considerar os outros exemplos no fluxo. Alguns formatos de vídeo contêm dados que dependem de quadros-chave e amostras compactadas.
-   O código de exemplo é escrito para sempre forçar o cliente a processar toda a saída antes que o plug-in aceite mais entradas.

A implementação padrão de **IMediaObject::D iscontinuity** simplesmente retorna S \_ OK.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando um plug-in do DSP de áudio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




