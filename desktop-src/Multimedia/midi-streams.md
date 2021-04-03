---
title: Fluxos de MIDI
description: Fluxos de MIDI
ms.assetid: 622472d9-2888-407f-bdaa-4943896c0bac
keywords:
- MIDI (interface digital de instrumento musical), fluxos
- MIDI (interface digital de instrumentos musicais), fluxos
- buffers de fluxo, fluxos de MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4237e1590f3af2e15a3b0b9fedea2fea4c9c40fc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084521"
---
# <a name="midi-streams"></a>Fluxos de MIDI

Os eventos MIDI ocorrem no contexto de um fluxo de dados MIDI. Embora um aplicativo possa usar vários fluxos para definir dados musicais, o mapeador de MIDI não reconhece vários fluxos. A maioria dos aplicativos que usam fluxos usa um fluxo de MIDI único.

As funções a seguir funcionam com fluxos.



| Valor                                            | Significado                                                                 |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)       | Fecha um fluxo de MIDI.                                                   |
| [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)         | Abre um fluxo de MIDI e recupera um identificador.                             |
| [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)           | Reproduz ou enfileira um fluxo (buffer) de dados MIDI para um dispositivo de saída MIDI. |
| [**midiStreamPause**](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)       | Pausa a reprodução de um fluxo MIDI especificado.                             |
| [**midiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) | Recupera a posição atual em um fluxo de MIDI.                        |
| [**midiStreamProperty**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty) | Define e recupera propriedades de fluxo.                                   |
| [**midiStreamRestart**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)   | Reinicia a reprodução de um fluxo de MIDI em pausa.                              |
| [**midiStreamStop**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)         | Desativa todas as notas em todos os canais MIDI para o fluxo MIDI especificado. |



 

 

 