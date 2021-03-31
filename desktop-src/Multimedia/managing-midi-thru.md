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
ms.openlocfilehash: 24214dd3f6cd13ca034b2555398f6055e4ce2da1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917196"
---
# <a name="managing-midi-thru"></a>Gerenciando MIDI por

Você pode conectar um dispositivo de entrada MIDI diretamente a um dispositivo de saída de MIDI para que, quando o dispositivo de entrada receber uma mensagem de [**\_ dados do mim**](mim-data.md) , o sistema envie uma mensagem com os mesmos dados de evento MIDI para o driver de dispositivo de saída. Para conectar um dispositivo de saída MIDI a um dispositivo de entrada MIDI, use a função [**midiConnect**](/windows/win32/api/mmeapi/nf-mmeapi-midiconnect) .

Para obter o melhor desempenho possível com várias saídas, um aplicativo pode optar por fornecer uma forma especial de driver de saída de MIDI, chamada por *meio de driver*. Embora o sistema permita que apenas um dispositivo de saída MIDI seja conectado a um dispositivo de entrada MIDI, vários dispositivos de saída MIDI podem ser conectados a um driver por meio do. Um aplicativo em um sistema desse tipo poderia conectar o dispositivo de entrada MIDI a esse dispositivo por meio dele e conectar o dispositivo MIDI via a tantos dispositivos de saída MIDI quantos forem necessários. Para obter mais informações sobre drivers, consulte a documentação do driver de dispositivo do Windows.

## <a name="using-messages-to-manage-midi-recording"></a>Usando mensagens para gerenciar a gravação de MIDI

As mensagens a seguir podem ser enviadas para um procedimento de retorno de chamada de thread ou de janela para gerenciar a gravação de MIDI.



| Valor                                          | Significado                                                                                                                                |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Eu \_ fechar do mim \_**](mm-mim-close.md)         | Enviado quando um dispositivo de entrada MIDI é fechado usando a função [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) .                                      |
| [**\_dados do mim mm \_**](mm-mim-data.md)           | Enviado quando uma mensagem MIDI completa é recebida. (Essa mensagem é usada para todas as mensagens MIDI, exceto mensagens exclusivas do sistema.)          |
| [**\_erro do mim mm \_**](mm-mim-error.md)         | Enviado quando uma mensagem MIDI inválida é recebida. (Essa mensagem é usada para todas as mensagens MIDI, exceto mensagens exclusivas do sistema.)          |
| [**\_LONGDATA do mim mm \_**](mm-mim-longdata.md)   | Enviado quando uma mensagem exclusiva do sistema MIDI é recebida ou quando um buffer é preenchido com dados exclusivos do sistema.     |
| [**\_LONGERROR do mim mm \_**](mm-mim-longerror.md) | Enviado quando uma mensagem exclusiva do sistema MIDI é recebida.                                                                        |
| [**\_MOREDATA do mim mm \_**](mm-mim-moredata.md)   | Enviado quando um aplicativo não está processando mensagens de [**\_ dados do mim**](mim-data.md) com rapidez suficiente para acompanhar o driver de dispositivo de entrada. |
| [**MIM de MM \_ \_ aberto**](mm-mim-open.md)           | Enviado quando um dispositivo de entrada MIDI é aberto usando a função [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .                                        |



 

Um parâmetro *wParam* e um parâmetro *lParam* são associados a cada uma dessas mensagens. O parâmetro *wParam* sempre especifica o identificador de um dispositivo MIDI aberto. O parâmetro *lParam* não é usado para as mensagens de [**\_ \_ abertura**](mm-mim-open.md) do mim de DD e mm de mm [**\_ \_**](mm-mim-close.md) .

Para a mensagem [**mm do \_ mim \_ LONGDATA**](mm-mim-longdata.md) , *lpMidiHdr* especifica um endereço de uma estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica o buffer para mensagens exclusivas do sistema. O buffer pode não estar completamente cheio, pois o tamanho das mensagens exclusivas do sistema geralmente não é conhecido antes de ser gravado e porque os buffers cujo tamanho total pode conter a maior mensagem esperada devem ser alocados. Para determinar a quantidade de dados válidos presentes no buffer, use o membro **dwBytesRecorded** da estrutura **MIDIHDR** .

## <a name="using-a-callback-function-to-manage-midi-recording"></a>Usando uma função de retorno de chamada para gerenciar a gravação de MIDI

Você pode definir sua própria função de retorno de chamada para gerenciar a gravação de dispositivos de entrada MIDI. A função de retorno de chamada está documentada como [**MidiInProc**](/previous-versions//dd798460(v=vs.85)).

As mensagens a seguir podem ser enviadas para o parâmetro *wMsg* da função de retorno de chamada **MidiInProc** .



| Valor                                   | Significado                                                                                                                                |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**próximo a MIM \_**](mim-close.md)         | Enviado quando o dispositivo é fechado usando a função [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) .                                               |
| [**dados do MIM \_**](mim-data.md)           | Enviado quando uma mensagem MIDI completa é recebida (essa mensagem é usada para todas as mensagens MIDI, exceto para mensagens exclusivas do sistema).           |
| [**erro do MIM \_**](mim-error.md)         | Enviado quando uma mensagem MIDI inválida é recebida (essa mensagem é usada para todas as mensagens MIDI, exceto para mensagens exclusivas do sistema).           |
| [**\_LONGDATA mim**](mim-longdata.md)   | Enviado quando uma mensagem exclusiva do sistema MIDI é recebida ou quando um buffer é preenchido com dados exclusivos do sistema.     |
| [**\_LONGERROR mim**](mim-longerror.md) | Enviado quando uma mensagem exclusiva do sistema MIDI é recebida.                                                                        |
| [**\_MOREDATA mim**](mim-moredata.md)   | Enviado quando um aplicativo não está processando mensagens de [**\_ dados do mim**](mim-data.md) com rapidez suficiente para acompanhar o driver de dispositivo de entrada. |
| [**MIM \_ aberto**](mim-open.md)           | Enviado quando o dispositivo de entrada MIDI é aberto usando a função [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .                                      |



 

Essas mensagens são semelhantes àquelas enviadas para funções de procedimento de janela, mas os parâmetros são diferentes. Um identificador do dispositivo MIDI aberto é passado como um parâmetro para a função de retorno de chamada, junto com o doubleword de dados de instância que foi passado usando **midiInOpen**.

Para a mensagem do [**mim \_ LONGDATA**](mim-longdata.md) , *lpMidiHdr* especifica um endereço de uma estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica o buffer para mensagens exclusivas do sistema. O buffer pode não estar completamente cheio. Para determinar a quantidade de dados válidos presentes no buffer, use o membro **dwBytesRecorded** da estrutura **MIDIHDR** .

Depois que o driver de dispositivo for concluído com um bloco de dados, você poderá limpar e liberar o bloco de dados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando áudio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 