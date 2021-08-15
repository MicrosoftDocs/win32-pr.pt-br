---
title: Recebendo Time-Stamped mensagens MIDI
description: Recebendo Time-Stamped mensagens MIDI
ms.assetid: a91c85fe-f9c4-4cf6-b0bb-49aa8ed45644
keywords:
- MIDI (Interface Digital do Instrument Instrument), mensagens com carimbo de data/hora
- MIDI (Interface Digital do Instrument Instrument), mensagens com carimbo de data/hora
- gravação de áudio MIDI, mensagens com carimbo de data/hora
- mensagens MIDI com carimbo de data/hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ec36628a417c19824e25c7ad013da9c539fe88cb6e58fd829a32205bce35679
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371286"
---
# <a name="receiving-time-stamped-midi-messages"></a>Recebendo Time-Stamped mensagens MIDI

Devido ao atraso entre quando o driver de dispositivo recebe uma mensagem MIDI e a hora em que o aplicativo recebe a mensagem, os drivers de dispositivo de entrada MIDI marcam a mensagem MIDI com a hora em que a mensagem foi recebida. Os carimbos de data/hora MIDI, que são definidos como a hora em que o primeiro byte da mensagem foi recebido, são especificados em milissegundos. A [**função midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) redefine os carimbos de data/hora de um dispositivo para zero.

Conforme mencionado anteriormente, para receber carimbos de data/hora com entrada MIDI, você deve usar uma função de retorno de chamada. O *parâmetro dwParam2* da função de retorno de chamada especifica o carimbo de data/hora para os dados associados às mensagens [**\_ DATA**](mim-data.md) MIM e [**MIM \_ LONGDATA.**](mim-longdata.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravação de áudio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 