---
title: Informações de tempo
description: Informações de tempo
ms.assetid: ff9d6fb2-1387-49ce-a4de-1b2f67353628
keywords:
- MIDI (Instrument Digital Interface Instrument), informações de tempo
- MIDI (Interface Digital do Instrument Instrument), informações de tempo
- buffers de fluxo, informações de tempo
- Estrutura MIDIEVENT
- buffers de fluxo, formato SMPTE
- buffers de fluxo, hora de anotação do trimestre
- buffers de fluxo, tiques
- Formato SMPTE
- hora de anotação do trimestre
- ticks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a75be9964457c64c7c1da59cb93aab2e423f72e861ba496494a5007025461c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804736"
---
# <a name="timing-information"></a>Informações de tempo

As informações de tempo de um evento MIDI são armazenadas no **membro dwDeltaTime** da [**estrutura MIDIEVENT.**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) O tempo é determinado em tiques, conforme definido na *especificação Standard MIDI Files 1.0.* O comprimento de um tique é definido pelo formato de hora e, possivelmente, pelo tempo associado ao fluxo. Para obter mais informações sobre fluxos, consulte [MIDI Fluxos](midi-streams.md).

Um tique é expresso como microssegundos por trimestre ou como tiques do tempo de SMPTE (Sociedade de Imagens de Movimento e Engenheiros de Tv). Aplicativos que enviam mensagens MIDI individualmente ou usam mensagens MIDI não processadas usam informações de tempo e hora de anotação trimestral para determinar a duração de um tique. Aplicativos que pré-processam mensagens MIDI podem armazenar o tempo decorrido como uma contagem das unidades SMPTE que estão sendo usadas.

O tempo de anotação do trimestre é indicado com um zero no bit de palavra alta (bit 15) da palavra de divisão de tempo. O restante da palavra contém os tiques por trimestre. Um tempo associado a um fluxo de dados MIDI é mantido em unidades (microssegundos por nota de trimestre) consistente com a especificação de Arquivos *MIDI Padrão 1.0.* Por exemplo, uma nota de trimestre em tempo de 4/4 que usa um tempo de 500.000 microssegundos por trimestre é reproduz a uma taxa de 120 tempos por minuto.

Formatos de divisão de tempo SMPTE especificam completamente o comprimento de um tique sem a necessidade de informações de tempo. Ao usar formatos de tempo SMPTE, as sequências MIDI podem ser sincronizadas com outros eventos SMPTE, como vídeo ou áudio em faixa. O tempo SMPTE é indicado com um 1 no bit de ordem alta (bit 15) da palavra de divisão de tempo. O restante do byte mais significativo especifica o formato SMPTE em uso como valores negativos. Os formatos SMPTE com suporte e seus valores correspondentes (entre parênteses) são 24 (-24), 25 (-25), 30 (-30) e 30 soltar (-29). O byte baixo da palavra de divisão de tempo especifica o número de tiques por quadro SMPTE.

 

 