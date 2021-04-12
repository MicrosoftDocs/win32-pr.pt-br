---
title: Gerenciando a gravação de MIDI
description: Gerenciando a gravação de MIDI
ms.assetid: 48b2d815-72cf-4c96-8d93-247d2426b8f2
keywords:
- MIDI (interface digital de instrumento musical), gravação
- MIDI (interface digital de instrumentos musicais), gravação
- gravando áudio MIDI, gerenciando
- Gravação de MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0edfb81976e1f5333798c9705640e7676281968a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104453979"
---
# <a name="managing-midi-recording"></a>Gerenciando a gravação de MIDI

Depois de abrir um dispositivo MIDI, você pode começar a gravar dados MIDI. O Windows fornece as seguintes funções para gerenciar a gravação de MIDI.



| Valor                                      | Significado                                                                                           |
|--------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) | Envia um buffer para o driver de dispositivo para que ele possa ser preenchido com dados de MIDI exclusivos do sistema gravados. |
| [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)         | Interrompe a gravação de MIDI e marca todos os buffers pendentes como concluído.                                       |
| [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)         | Inicia a gravação de MIDI e redefine o carimbo de data/hora como zero.                                          |
| [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)           | Interrompe a gravação de MIDI.                                                                             |



 

Para enviar buffers para o driver de dispositivo para gravar mensagens exclusivas do sistema, use [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer). O aplicativo é notificado, pois os buffers são preenchidos com dados registrados exclusivos do sistema. Para obter mais informações sobre as técnicas de notificação, consulte [Managing MIDI data Blocks](managing-midi-data-blocks.md).

A função [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) inicia o processo de gravação. Ao registrar mensagens exclusivas do sistema, envie pelo menos um buffer para o driver antes de iniciar a gravação. Para interromper a gravação, use [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop). Antes de fechar o dispositivo usando a função [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) , marque todos os blocos de dados pendentes como sendo feitos chamando [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset).

Os aplicativos que exigem dados com carimbo de data/hora usam uma função de retorno de chamada para receber dados MIDI. Se os requisitos de tempo não forem estritos, você poderá usar uma janela ou um retorno de chamada de thread. No entanto, você não pode usar um retorno de chamada de evento para receber dados MIDI.

Para registrar mensagens exclusivas do sistema com aplicativos que não usam buffers de fluxo, você deve fornecer o driver de dispositivo com buffers. Esses buffers são especificados usando uma estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando áudio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 