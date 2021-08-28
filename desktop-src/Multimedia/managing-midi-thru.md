---
title: Gerenciando MIDI por
description: Gerenciando MIDI por
ms.assetid: ba03a2a1-d998-498d-ad53-027ba2b6e276
keywords:
- MIDI (interface digital de instrumento musical), por meio do driver
- MIDI (interface digital de instrumento musical), por meio do driver
- gravando áudio MIDI, por meio do driver
- Driver MIDI por
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c108ac13fbbfb80d1f7c41960984c904374db31e3a790f14c326cf9e7946dac9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138939"
---
# <a name="managing-midi-thru"></a>Gerenciando MIDI por

você pode conectar um dispositivo de entrada midi diretamente a um dispositivo de saída de midi para que, quando o dispositivo de entrada receber uma mensagem de [**\_ dados de MIM**](mim-data.md) , o sistema envie uma mensagem com os mesmos dados de evento MIDI para o driver de dispositivo de saída. Para conectar um dispositivo de saída MIDI a um dispositivo de entrada MIDI, use a função [**midiConnect**](/windows/win32/api/mmeapi/nf-mmeapi-midiconnect) .

Para obter o melhor desempenho possível com várias saídas, um aplicativo pode optar por fornecer uma forma especial de driver de saída de MIDI, chamada por *meio de driver*. Embora o sistema permita que apenas um dispositivo de saída MIDI seja conectado a um dispositivo de entrada MIDI, vários dispositivos de saída MIDI podem ser conectados a um driver por meio do. Um aplicativo em um sistema desse tipo poderia conectar o dispositivo de entrada MIDI a esse dispositivo por meio dele e conectar o dispositivo MIDI via a tantos dispositivos de saída MIDI quantos forem necessários. para obter mais informações sobre drivers, consulte a documentação do driver de dispositivo Windows.

## <a name="using-messages-to-manage-midi-recording"></a>Usando mensagens para gerenciar a gravação de MIDI

As mensagens a seguir podem ser enviadas para um procedimento de retorno de chamada de thread ou de janela para gerenciar a gravação de MIDI.



| Valor                                          | Significado                                                                                                                                |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ MIM \_ fechar**](mm-mim-close.md)         | Enviado quando um dispositivo de entrada MIDI é fechado usando a função [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) .                                      |
| [**\_dados de MIM MM \_**](mm-mim-data.md)           | Enviado quando uma mensagem MIDI completa é recebida. (Essa mensagem é usada para todas as mensagens MIDI, exceto mensagens exclusivas do sistema.)          |
| [**\_erro de MIM MM \_**](mm-mim-error.md)         | Enviado quando uma mensagem MIDI inválida é recebida. (Essa mensagem é usada para todas as mensagens MIDI, exceto mensagens exclusivas do sistema.)          |
| [**MM \_ MIM \_ LONGDATA**](mm-mim-longdata.md)   | Enviado quando uma mensagem exclusiva do sistema MIDI é recebida ou quando um buffer é preenchido com dados exclusivos do sistema.     |
| [**MM \_ MIM \_ LONGERROR**](mm-mim-longerror.md) | Enviado quando uma mensagem exclusiva do sistema MIDI é recebida.                                                                        |
| [**MM \_ MIM \_ MOREDATA**](mm-mim-moredata.md)   | enviado quando um aplicativo não está processando MIM mensagens de [**\_ dados**](mim-data.md) com rapidez suficiente para acompanhar o driver de dispositivo de entrada. |
| [**MM \_ MIM \_ abrir**](mm-mim-open.md)           | Enviado quando um dispositivo de entrada MIDI é aberto usando a função [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .                                        |



 

Um parâmetro *wParam* e um parâmetro *lParam* são associados a cada uma dessas mensagens. O parâmetro *wParam* sempre especifica o identificador de um dispositivo MIDI aberto. o parâmetro *lParam* não é usado para [**mm \_ MIM \_ fechar**](mm-mim-close.md) e [**mm MIM mensagens \_ \_ abertas**](mm-mim-open.md) .

para a mensagem [**MM \_ MIM \_ LONGDATA**](mm-mim-longdata.md) , *lpMidiHdr* especifica um endereço de uma estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica o buffer para mensagens exclusivas do sistema. O buffer pode não estar completamente cheio, pois o tamanho das mensagens exclusivas do sistema geralmente não é conhecido antes de ser gravado e porque os buffers cujo tamanho total pode conter a maior mensagem esperada devem ser alocados. Para determinar a quantidade de dados válidos presentes no buffer, use o membro **dwBytesRecorded** da estrutura **MIDIHDR** .

## <a name="using-a-callback-function-to-manage-midi-recording"></a>Usando uma função de retorno de chamada para gerenciar a gravação de MIDI

Você pode definir sua própria função de retorno de chamada para gerenciar a gravação de dispositivos de entrada MIDI. A função de retorno de chamada está documentada como [**MidiInProc**](/previous-versions//dd798460(v=vs.85)).

As mensagens a seguir podem ser enviadas para o parâmetro *wMsg* da função de retorno de chamada **MidiInProc** .



| Valor                                   | Significado                                                                                                                                |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**MIM \_ INCLUI**](mim-close.md)         | Enviado quando o dispositivo é fechado usando a função [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) .                                               |
| [**MIM \_ DADO**](mim-data.md)           | Enviado quando uma mensagem MIDI completa é recebida (essa mensagem é usada para todas as mensagens MIDI, exceto para mensagens exclusivas do sistema).           |
| [**MIM \_ AO**](mim-error.md)         | Enviado quando uma mensagem MIDI inválida é recebida (essa mensagem é usada para todas as mensagens MIDI, exceto para mensagens exclusivas do sistema).           |
| [**MIM \_ LONGDATA**](mim-longdata.md)   | Enviado quando uma mensagem exclusiva do sistema MIDI é recebida ou quando um buffer é preenchido com dados exclusivos do sistema.     |
| [**MIM \_ LONGERROR**](mim-longerror.md) | Enviado quando uma mensagem exclusiva do sistema MIDI é recebida.                                                                        |
| [**MIM \_ MOREDATA**](mim-moredata.md)   | enviado quando um aplicativo não está processando MIM mensagens de [**\_ dados**](mim-data.md) com rapidez suficiente para acompanhar o driver de dispositivo de entrada. |
| [**MIM \_ ABRIR**](mim-open.md)           | Enviado quando o dispositivo de entrada MIDI é aberto usando a função [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .                                      |



 

Essas mensagens são semelhantes àquelas enviadas para funções de procedimento de janela, mas os parâmetros são diferentes. Um identificador do dispositivo MIDI aberto é passado como um parâmetro para a função de retorno de chamada, junto com o doubleword de dados de instância que foi passado usando **midiInOpen**.

para a [**MIM mensagem \_ LONGDATA**](mim-longdata.md) , *lpMidiHdr* especifica um endereço de uma estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica o buffer para mensagens exclusivas do sistema. O buffer pode não estar completamente cheio. Para determinar a quantidade de dados válidos presentes no buffer, use o membro **dwBytesRecorded** da estrutura **MIDIHDR** .

Depois que o driver de dispositivo for concluído com um bloco de dados, você poderá limpar e liberar o bloco de dados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando áudio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 