---
title: O mapeador de MIDI
description: O mapeador de MIDI
ms.assetid: 92cffc67-b4a4-4807-94d2-02fbbdba5abf
keywords:
- Multimídia do Windows, mapeador de MIDI
- multimídia, mapeador de MIDI
- áudio de multimídia, mapeador de MIDI
- áudio, mapeador de MIDI
- MIDI (interface digital de instrumento musical), mapeador de MIDI
- MIDI (interface digital de instrumentos musicais), mapeador de MIDI
- Mapeador de MIDI, sobre
- Mapeador de MIDI, origem
- Mapeador de MIDI, destino
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b360148c994c0ee6434fdf097ca5f393b23d49
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005344"
---
# <a name="the-midi-mapper"></a>O mapeador de MIDI

Os serviços de patch padrão do mapeador de MIDI fornecem reprodução de arquivo MIDI independente de dispositivo para aplicativos. O mapeador de MIDI pode ser usado com o sequenciador MIDI MCI ou com serviços de saída MIDI de nível baixo.

A menos que declarado de outra forma, todas as referências a números de canal de MIDI usam os números de canal lógico de 1 a 16. Esses números de canal lógico correspondem aos números de canal físico de 0 a 15 que, na verdade, fazem parte da mensagem MIDI. Todas as referências a valores de chave e alteração de programa MIDI usam os valores físicos de 0 a 127. Todos os números são decimais, a menos que sejam precedidos pelo prefixo "0x"; nesse caso, eles são hexadecimais.

Na discussão do mapeador de MIDI, o termo *origem* se refere ao lado de entrada do mapeador de Midi. O termo *destino* refere-se ao lado de saída do mapeador de Midi. Por exemplo, um canal de origem é o canal MIDI de uma mensagem enviada para o mapeador de MIDI, e um canal de destino é o canal MIDI de uma mensagem enviada do Mapeador MIDI para um dispositivo de saída.

-   [O mapeador de MIDI e o Windows](the-midi-mapper-and-windows.md)
-   [A arquitetura do mapeador de MIDI](the-midi-mapper-architecture.md)
-   [O mapa do canal](the-channel-map.md)
-   [Mapas de patch](patch-maps.md)
-   [O volume escalar](the-volume-scalar.md)
-   [Mapas de chaves](key-maps.md)
-   [Resumo de mensagens de mapas e MIDI](summary-of-maps-and-midi-messages.md)

 

 




