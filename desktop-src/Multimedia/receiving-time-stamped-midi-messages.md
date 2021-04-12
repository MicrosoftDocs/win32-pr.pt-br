---
title: Recebendo Time-Stamped mensagens MIDI
description: Recebendo Time-Stamped mensagens MIDI
ms.assetid: a91c85fe-f9c4-4cf6-b0bb-49aa8ed45644
keywords:
- MIDI (interface digital de instrumento musical), mensagens com carimbo de data/hora
- MIDI (interface digital de instrumentos musicais), mensagens com carimbo de data/hora
- gravando áudio MIDI, mensagens com carimbo de data/hora
- mensagens de MIDI com carimbo de data/hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7ead268c6d022f67a3607bb8a43a3d773bd7325
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293969"
---
# <a name="receiving-time-stamped-midi-messages"></a>Recebendo Time-Stamped mensagens MIDI

Devido ao atraso entre o momento em que o driver de dispositivo recebe uma mensagem MIDI e a hora em que o aplicativo recebe a mensagem, os drivers de dispositivo de entrada MIDI carimbam a mensagem MIDI com a hora em que a mensagem foi recebida. Os carimbos de data/hora MIDI, que são definidos como a hora em que o primeiro byte da mensagem foi recebido, são especificados em milissegundos. A função [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) redefine os carimbos de data/hora de um dispositivo para zero.

Conforme mencionado anteriormente, para receber carimbos de data/hora com entrada MIDI, você deve usar uma função de retorno de chamada. O parâmetro *dwParam2* da função de retorno de chamada especifica o carimbo de data/hora dos dados associados aos [**\_ dados do mim**](mim-data.md) e às mensagens do [**mim \_ LONGDATA**](mim-longdata.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando áudio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 