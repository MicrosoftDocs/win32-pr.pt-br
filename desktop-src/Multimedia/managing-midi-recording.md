---
title: Gerenciando a gravação MIDI
description: Gerenciando a gravação MIDI
ms.assetid: 48b2d815-72cf-4c96-8d93-247d2426b8f2
keywords:
- MIDI (Instrument Digital Interface Instrument), gravação
- MIDI (Interface Digital do Instrument Instrument), gravação
- gravando áudio MIDI, gerenciando
- Gravação MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29bf4ac85ad0cc9735a08bab3ee07d744eecb0d75308ee323ec93c1c69b1a9e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139057"
---
# <a name="managing-midi-recording"></a>Gerenciando a gravação MIDI

Depois de abrir um dispositivo MIDI, você pode começar a gravar dados MIDI. Windows fornece as seguintes funções para gerenciar a gravação MIDI.



| Valor                                      | Significado                                                                                           |
|--------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) | Envia um buffer para o driver de dispositivo para que ele possa ser preenchido com dados MIDI exclusivos do sistema registrados. |
| [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)         | Interrompe a gravação MIDI e marca todos os buffers pendentes conforme feito.                                       |
| [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)         | Inicia a gravação MIDI e redefine o carimbo de data/hora como zero.                                          |
| [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)           | Interrompe a gravação MIDI.                                                                             |



 

Para enviar buffers para o driver de dispositivo para gravar mensagens exclusivas do sistema, use [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer). O aplicativo é notificado à medida que os buffers são preenchidos com dados gravados exclusivos do sistema. Para obter mais informações sobre as técnicas de notificação, consulte [Gerenciando blocos de dados MIDI](managing-midi-data-blocks.md).

A [**função midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) inicia o processo de gravação. Ao gravar mensagens exclusivas do sistema, envie pelo menos um buffer para o driver antes de iniciar a gravação. Para interromper a gravação, use [**midiInStop.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop) Antes de fechar o dispositivo usando a [**função midiInClose,**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) marque os blocos de dados pendentes como sendo feitos chamando [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset).

Aplicativos que exigem dados com carimbo de data/hora usam uma função de retorno de chamada para receber dados MIDI. Se seus requisitos de tempo não são estritos, você pode usar uma janela ou retorno de chamada de thread. No entanto, você não pode usar um retorno de chamada de evento para receber dados MIDI.

Para registrar mensagens exclusivas do sistema com aplicativos que não usam buffers de fluxo, você deve fornecer buffers ao driver de dispositivo. Esses buffers são especificados usando uma [**estrutura MIDIHDR.**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravação de áudio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 