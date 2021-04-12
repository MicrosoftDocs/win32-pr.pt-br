---
title: Mapas de patch
description: Mapas de patch
ms.assetid: d0c91001-d19d-439c-9773-78d6228a6642
keywords:
- MIDI (interface digital de instrumento musical), mapeador de MIDI
- MIDI (interface digital de instrumentos musicais), mapeador de MIDI
- Mapeador de MIDI, mapas de patch
- mapas de patch
- Programa MIDI – alterar mensagens
- Mensagens de controlador de volume de MIDI
- programa-alterar mensagens
- mensagens do controlador de volume
- Mapeador de MIDI, mensagens de alteração de programa
- Mapeador de MIDI, mensagens de controlador de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e418b0616d9ba9d2c2bcd05ebcb312ba0176ef5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292094"
---
# <a name="patch-maps"></a>Mapas de patch

Cada entrada de mapa de canal pode ter um mapa de patch associado. Mapas de patch afetam as mensagens de alteração de programa MIDI e controlador de volume. Mensagens de alteração de programa informam um sintetizador para alterar o som do instrumento (patch) para um canal especificado. As mensagens do controlador de volume definem o volume para um canal.

Um mapa de patch tem uma tabela de conversão com uma entrada para cada um dos valores de alteração de programa 128. Cada mapa de patch especifica o seguinte:

-   Um programa de destino-alterar valor.
-   Um volume escalar. (Para obter mais informações, consulte [o volume escalar](the-volume-scalar.md).)
-   Um mapa de chave opcional. (Para obter mais informações, consulte [mapas de chaves](key-maps.md).)

Quando as mensagens de alteração de programa são recebidas pelo mapeador de MIDI, o valor de alteração do programa de destino é substituído pelo valor de alteração de programa na mensagem. Por exemplo, se o programa de destino-alterar o valor da alteração de programa 16 for 18, o mapeador de MIDI modificará a mensagem de alteração do programa MIDI, conforme mostrado na ilustração a seguir.

![imagem do Mapeador MIDI](images/mmap-a03.gif)

 

 




