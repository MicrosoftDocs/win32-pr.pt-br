---
title: O mapa do canal
description: O mapa do canal
ms.assetid: f35d8b76-dfbf-4453-baec-9c0b22f5278a
keywords:
- MIDI (interface digital de instrumento musical), mapeador de MIDI
- MIDI (interface digital de instrumentos musicais), mapeador de MIDI
- Mapeador de MIDI, mapa de canal
- mapa de canal
- Mapeador de MIDI, mensagens de canal
- Mensagens do canal MIDI
- mensagens do canal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d514b5af6df6426db7cc5a313d1c6a52070a49c22a8a04e8cd2a9c34f49d80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688277"
---
# <a name="the-channel-map"></a>O mapa do canal

O mapa de canal afeta todas as mensagens de canal MIDI. As mensagens do canal MIDI incluem observação-em, nota-aftertouch, chave de telefonia, controle de alterações de programa, alteração de programas, canal-AfterTouch e mensagens de alteração de curvatura de densidade. O mapeador de MIDI usa um único mapa de canal com uma entrada para cada um dos 16 canais MIDI. Cada entrada de mapa de canal especifica o seguinte:

-   Um canal de destino para a mensagem MIDI
-   Um dispositivo de saída de destino para a mensagem MIDI
-   Um mapa de patch opcional especificando outras possíveis modificações para a mensagem MIDI

O canal de destino é definido como um dos 16 canais MIDI. As mensagens MIDI são modificadas para refletir cada nova atribuição de canal. Por exemplo, se a entrada canal de destino para MIDI Channel 4 estiver definida como 6, todas as mensagens MIDI enviadas para o canal 4 serão mapeadas para o canal 6, conforme mostrado na ilustração a seguir.

![imagem MIDI mapeada](images/mmap-a05.gif)

Neste exemplo, o byte de status de MIDI 0x93 é mapeado para 0x95. A ordem baixa de um byte de status de MIDI especifica o número do canal. Os canais de origem são definidos como ativo ou inativo. As mensagens enviadas a canais de origem inativos são ignoradas, portanto, um canal inativo está em vigor sem áudio ou desligado.

O dispositivo de saída de destino é definido como um dos dispositivos de saída MIDI disponíveis. Um dispositivo de saída de MIDI pode ser um sintetizador interno ou uma porta de saída de MIDI física.

Mensagens do sistema MIDI são mensagens de MIDI (com bytes de status) de 0xF0 a 0xFF. Não há canal associado às mensagens do sistema MIDI, portanto, eles não podem ser mapeados. As mensagens do sistema MIDI são enviadas para todos os dispositivos de saída MIDI listados em um mapa de canal.

 

 




