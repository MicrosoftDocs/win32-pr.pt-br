---
title: Patch Mapas
description: Patch Mapas
ms.assetid: d0c91001-d19d-439c-9773-78d6228a6642
keywords:
- MIDI (Interface Digital do Instrument Instrument), Mapeado MIDI
- MIDI (Interface Digital Instrument Instrument), Mapeado MIDI
- Mapeado MIDI, mapas de patch
- mapas de patch
- Mensagens de alteração de programa MIDI
- Mensagens do controlador de volume MIDI
- mensagens de alteração de programa
- mensagens do controlador de volume
- Mapeado MIDI, mensagens de alteração de programa
- Mapeado MIDI, mensagens do controlador de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb32f60ac486d7e8812b5cf71febe3794ae37d650bc795baa4c06ffb48ce5f42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038256"
---
# <a name="patch-maps"></a>Patch Mapas

Cada entrada de mapa de canal pode ter um mapa de patch associado. Os mapas de patch afetam as mensagens MIDI program-change e volume-controller. Mensagens de alteração de programa dizem a um sintetizador para alterar o som do instrumento (patch) para um canal especificado. As mensagens do controlador de volume configuram o volume de um canal.

Um mapa de patch tem uma tabela de tradução com uma entrada para cada um dos 128 valores de alteração de programa. Cada mapa de patch especifica o seguinte:

-   Um valor de alteração do programa de destino.
-   Um escalar de volume. (Para obter mais informações, consulte [The Volume Scalar](the-volume-scalar.md).)
-   Um mapa de chaves opcional. (Para obter mais informações, consulte [Key Mapas](key-maps.md).)

Quando as mensagens de alteração de programa são recebidas pelo Mapeado MIDI, o valor de alteração do programa de destino é substituído pelo valor program-change na mensagem. Por exemplo, se o valor program-change de destino para program-change 16 for 18, o Mapeado MIDI modificará a mensagem de alteração de programa MIDI, conforme mostrado na ilustração a seguir.

![Imagem do mapeado midi](images/mmap-a03.gif)

 

 




