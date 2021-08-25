---
title: O mapeado MIDI
description: O mapeado MIDI
ms.assetid: 92cffc67-b4a4-4807-94d2-02fbbdba5abf
keywords:
- Windows multimídia, Mapeado MIDI
- multimídia, Mapeado MIDI
- áudio multimídia, Mapeado MIDI
- audio, Mapeado MIDI
- MIDI (Interface Digital do Instrument Instrument), Mapeado MIDI
- MIDI (Interface Digital Instrument Instrument), Mapeado MIDI
- Mapeado MIDI, sobre
- Mapeado MIDI, origem
- Mapeado MIDI, destino
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a5becc117668964a584f29c311c3e3ac477f672085e837e28d7eecc595658d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805096"
---
# <a name="the-midi-mapper"></a>O mapeado MIDI

Os serviços de patch padrão do Mapeado MIDI fornecem reprodução de arquivo MIDI independente do dispositivo para aplicativos. O Mapeador MIDI pode ser usado com o sequenciador MCI MIDI ou com serviços de saída MIDI de baixo nível.

A menos que indicado de outra forma, todas as referências aos números de canal MIDI usam os números de canal lógico de 1 a 16. Esses números de canal lógico correspondem aos números de canal físico de 0 a 15 que, na verdade, fazem parte da mensagem MIDI. Todas as referências a alteração de programa MIDI e valores de chave usam os valores físicos de 0 a 127. Todos os números são decimais, a menos que precedam pelo prefixo "0x", caso em que eles são hexadecimais.

Na discussão do Mapeado MIDI, o termo *fonte* refere-se ao lado de entrada do Mapeado MIDI. O termo *destino* refere-se ao lado de saída do Mapeado MIDI. Por exemplo, um canal de origem é o canal MIDI de uma mensagem enviada ao Mapeado MIDI e um canal de destino é o canal MIDI de uma mensagem enviada do Mapeado MIDI para um dispositivo de saída.

-   [O mapeado MIDI e Windows](the-midi-mapper-and-windows.md)
-   [A arquitetura do mapeado MIDI](the-midi-mapper-architecture.md)
-   [O mapa do canal](the-channel-map.md)
-   [Patch Mapas](patch-maps.md)
-   [O escalar de volume](the-volume-scalar.md)
-   [Chave Mapas](key-maps.md)
-   [Resumo de mensagens Mapas e MIDI](summary-of-maps-and-midi-messages.md)

 

 




