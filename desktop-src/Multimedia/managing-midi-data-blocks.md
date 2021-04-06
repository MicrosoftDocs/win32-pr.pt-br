---
title: Gerenciando blocos de dados MIDI
description: Gerenciando blocos de dados MIDI
ms.assetid: f29fbc08-ef67-489c-aedf-5a2bc65233f7
keywords:
- MIDI (interface digital de instrumento musical), gerenciando blocos de dados
- MIDI (interface digital de instrumentos musicais), gerenciando blocos de dados
- Serviços de MIDI, gerenciando blocos de dados
- Gerenciando blocos de dados MIDI
- MIDI (interface digital de instrumento musical), mensagens do driver de processamento
- MIDI (interface digital de instrumentos musicais), processamento de mensagens do driver
- Serviços de MIDI, processando mensagens de driver
- Processando mensagens do driver
- MIDI (interface digital de instrumento musical), blocos de dados
- MIDI (interface digital de instrumentos musicais), blocos de dados
- Serviços de MIDI, blocos de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af348d6c53d2944bf22c026674704baa1fe74e07
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917197"
---
# <a name="managing-midi-data-blocks"></a>Gerenciando blocos de dados MIDI

Aplicativos que usam blocos de dados para passar mensagens exclusivas do sistema (usando as funções [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) e [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) ) e buffers de fluxo (usando a função [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) ) devem fornecer continuamente o driver de dispositivo com blocos de dados até que a reprodução ou gravação seja concluída.

Mesmo que um único bloco de dados seja usado, um aplicativo deve ser capaz de determinar quando um driver de dispositivo é concluído com o bloco de dados para que ele possa liberar a memória associada ao bloco de dados e à estrutura de cabeçalho. Três métodos podem ser usados para determinar quando um driver de dispositivo é concluído com um bloco de dados:

-   Especifique uma função de retorno de chamada para receber uma mensagem enviada pelo driver quando ela for concluída com um bloco de dados. Para obter dados de entrada MIDI com carimbo de data/hora, você deve usar uma função de retorno de chamada.
-   Use um retorno de chamada de evento (somente para saída).
-   Use uma janela ou um retorno de chamada de thread para receber uma mensagem enviada pelo driver quando ele for concluído com um bloco de dados.

Se um aplicativo não obtiver um bloco de dados para o driver de dispositivo quando for necessário, uma lacuna audível na reprodução ou uma perda de informações registradas de entrada poderá ocorrer. No mínimo, um aplicativo deve usar um esquema de buffer duplo para manter pelo menos um bloco de dados à frente do driver de dispositivo.

## <a name="using-a-callback-function-to-process-driver-messages"></a>Usando uma função de retorno de chamada para processar mensagens de driver

Você pode escrever sua própria função de retorno de chamada para processar mensagens enviadas pelo driver de dispositivo. Para usar uma função de retorno de chamada, especifique o sinalizador da função de retorno de chamada \_ no parâmetro *dwFlags* e o endereço da função de retorno de chamada no parâmetro *dwCallback* da função [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) ou [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .

As mensagens enviadas a uma função de retorno de chamada são semelhantes às mensagens enviadas a uma janela, exceto que têm dois parâmetros doubleword em vez de um parâmetro inteiro não assinado e um parâmetro doubleword. Para obter mais informações sobre essas mensagens, consulte [enviando mensagens System-Exclusive](sending-system-exclusive-messages.md) e [Gerenciando a gravação de Midi](managing-midi-recording.md).

Use uma das técnicas a seguir para passar dados de instância de um aplicativo para uma função de retorno de chamada:

-   Use o parâmetro *dwCallBackInstance* da função que abre o driver de dispositivo.
-   Use o membro **dwUser** da estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica um bloco de dados que está sendo enviado a um driver de dispositivo MIDI.

Se você precisar de mais de 32 bits de dados de instância, passe um endereço de uma estrutura que contém as informações adicionais.

## <a name="using-an-event-callback-to-process-driver-messages"></a>Usando um retorno de chamada de evento para processar mensagens de driver

Para usar um retorno de chamada de evento, use a função [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) para recuperar o identificador de um evento e especifique o evento de retorno \_ de chamada na chamadas para a função [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .

Um retorno de chamada de evento é definido por qualquer coisa que possa causar um retorno de chamada de função. Ao contrário das funções de retorno de chamada e de retornos de chamada de janela ou thread, os retornos de chamada de evento não recebem notificações específicas de fechamento, conclusão ou abertura. Portanto, um aplicativo pode precisar verificar o status do processo que está aguardando depois que o evento ocorrer.

Para obter mais informações sobre retornos de chamada de evento, consulte [usando um retorno de chamada de evento para gerenciar a reprodução em buffer](using-an-callback-to-manage-buffered-playback.md).

## <a name="using-a-window-or-thread-callback-to-process-driver-messages"></a>Usando uma janela ou um retorno de chamada de thread para processar mensagens de driver

Para usar um retorno de chamada de janela, especifique o sinalizador de janela de retorno de chamada \_ no parâmetro *dwFlags* e um identificador de janela na palavra de ordem inferior do parâmetro *dwCallback* da função [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) ou [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) . As mensagens de driver serão enviadas para a função de procedimento de janela para a janela identificada pelo identificador em *dwCallback*.

Da mesma forma, para usar um retorno de chamada de thread, especifique o sinalizador de thread de retorno de chamada \_ e um identificador de thread na chamada para **MidiInOpen** ou **midiOutOpen**. Nesse caso, as mensagens serão postadas no thread especificado em vez de em uma janela.

As mensagens enviadas para uma janela ou retorno de chamada de thread são específicas para o dispositivo MIDI usado. Para obter mais informações sobre essas mensagens, consulte [enviando mensagens System-Exclusive](sending-system-exclusive-messages.md) e [Gerenciando a gravação de Midi](managing-midi-recording.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Serviços MIDI](midi-services.md)
</dt> </dl>

 

 