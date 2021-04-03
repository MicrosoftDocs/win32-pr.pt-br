---
title: Informações de tempo
description: Informações de tempo
ms.assetid: ff9d6fb2-1387-49ce-a4de-1b2f67353628
keywords:
- MIDI (interface digital de instrumento musical), informações de tempo
- MIDI (interface digital de instrumentos musicais), informações de tempo
- buffers de fluxo, informações de tempo
- Estrutura MIDIEVENT
- buffers de fluxo, formato SMPTE
- buffers de fluxo, tempo de nota do trimestre
- buffers de fluxo, tiques
- Formato SMPTE
- hora da nota do trimestre
- ticks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2daf5b1847456e8fb518665521e484118fead79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084468"
---
# <a name="timing-information"></a>Informações de tempo

As informações de tempo para um evento MIDI são armazenadas no membro **dwDeltaTime** da estrutura [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) . O tempo é fornecido em tiques, conforme definido na especificação *padrão de arquivos MIDI 1,0* . O comprimento de um tique é definido pelo formato de hora e possivelmente pelo tempo associado ao fluxo. Para obter mais informações sobre fluxos, consulte [fluxos de Midi](midi-streams.md).

Uma escala é expressa como microssegundos por trimestre ou como tiques de hora SMPTE (sociedade de imagem de movimento e engenheiros de televisão). Os aplicativos que enviam mensagens de MIDI individualmente ou usam mensagens MIDI não processadas usam informações de hora do trimestre e tempo para determinar a duração de um tique. Aplicativos que processam mensagens MIDI podem armazenar o tempo decorrido como uma contagem das unidades SMPTE que estão sendo usadas.

O tempo de nota de trimestre é indicado com um zero no bit de palavra alta (bit 15) da palavra de divisão de tempo. O restante da palavra contém as marcações por trimestre. Um tempo associado a um fluxo de dados MIDI é mantido em unidades (microssegundos por trimestre) consistentes com a especificação *1,0 de arquivos MIDI padrão* . Por exemplo, um quarto de nota em 4/4 tempo que usa um tempo de 500.000 microssegundos por trimestre de observação é reproduzido à taxa de 120 batidas por minuto.

Os formatos de divisão de tempo SMPTE especificam completamente o comprimento de um tique sem a necessidade de informações de tempo. No uso de formatos de hora SMPTE, as sequências MIDI podem ser sincronizadas com outros eventos SMPTE, como vídeo ou áudio distribuído. O horário SMPTE é indicado com um 1 no bit de ordem superior (bit 15) da palavra de divisão de tempo. O restante do byte mais significativo especifica o formato SMPTE em uso como valores negativos. Os formatos SMPTE com suporte e seus valores correspondentes (entre parênteses) são 24 (-24), 25 (-25), 30 (-30) e 30 Drop (-29). O byte inferior da palavra de divisão de tempo especifica o número de tiques por quadro SMPTE.

 

 