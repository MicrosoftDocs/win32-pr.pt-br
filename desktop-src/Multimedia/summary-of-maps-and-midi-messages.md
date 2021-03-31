---
title: Resumo de mensagens de mapas e MIDI
description: Resumo de mensagens de mapas e MIDI
ms.assetid: cd0ec7b0-2ba1-4e75-b85c-f5b95ac9dfeb
keywords:
- MIDI (interface digital de instrumento musical), mapeador de MIDI
- MIDI (interface digital de instrumentos musicais), mapeador de MIDI
- Mapeador de MIDI, mapa de canal
- Mapeador de MIDI, mapas de patch
- Mapeador de MIDI, mapas de chave
- mapa de canal
- mapas de patch
- mapas de chaves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd962f848343ea493204d494943a99eedcc56a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636836"
---
# <a name="summary-of-maps-and-midi-messages"></a>Resumo de mensagens de mapas e MIDI

A seguir estão os bytes de status para mensagens MIDI e os tipos de mapa que afetam cada mensagem.



| Status de MIDI | Description               | Tipos de mapa                |
|-------------|---------------------------|--------------------------|
| 0x80-0x8F   | Anotação desativada                  | Mapas de canal, mapas de chaves   |
| 0x90-0x9F   | Observe o                    | Mapas de canal, mapas de chaves   |
| 0xA0-0xAF   | Aftertouch de chave de telefonia | Mapas de canal, mapas de chaves   |
| 0xB0-0xBF   | Alteração de controle            | Mapas de canal, mapas de patch |
| 0xC0-0xCF   | Alteração do programa            | Mapas de canal, mapas de patch |
| 0xD0-0xDF   | Aftertouch de canal        | Mapas de canal             |
| 0xE0-0xEF   | Alteração de curvatura de densidade         | Mapas de canal             |
| 0xF0-0xFF   | Sistema                    | Não mapeado               |



 

-   Os quatro bits de ordem superior representam o valor de status. Os quatro bits de ordem inferior representam as informações do canal.
-   Mapas de patch afetam apenas o controlador 7 (volume principal).
-   As mensagens do sistema são enviadas para todos os dispositivos listados em um mapa de canal.

 

 




