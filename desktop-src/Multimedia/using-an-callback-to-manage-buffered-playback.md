---
title: Usando um retorno de chamada de evento para gerenciar a reprodução em buffer
description: Usando um retorno de chamada de evento para gerenciar a reprodução em buffer
ms.assetid: 3b60daea-574d-430b-b14e-1fefceb69dfb
keywords:
- MIDI (interface digital de instrumento musical), reprodução em buffer
- MIDI (interface digital de instrumentos musicais), reprodução em buffer
- executando arquivos MIDI, reprodução em buffer
- reprodução em buffer
- Função CreateEvent
- MIDI (interface digital de instrumento musical), retorno de chamada de evento
- MIDI (interface digital de instrumento musical), retorno de chamada de evento
- executando arquivos MIDI, retorno de chamada de evento
- retorno de chamada do evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc6f6cc7bec7971c117cb81b2f823d7184bc2fd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640629"
---
# <a name="using-an-event-callback-to-manage-buffered-playback"></a>Usando um retorno de chamada de evento para gerenciar a reprodução em buffer

Para usar um retorno de chamada de evento, use a função [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) para recuperar o identificador de um evento. Em uma chamada para a função [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) , especifique \_ o evento de retorno de chamada para o parâmetro *dwFlags* . Depois de usar a função [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) , mas antes de enviar eventos de MIDI para o dispositivo, crie um evento não sinalizado chamando a função [ResetEvent](/windows/win32/api/synchapi/nf-synchapi-resetevent) , especificando o identificador de evento recuperado por **CreateEvent**. Em seguida, dentro de um loop que verifica se o \_ bit MHDR feito está definido no membro **dwFlags** da estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , use a função [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) , especificando o identificador de evento e um valor de tempo limite de infinito como parâmetros.

Um retorno de chamada de evento é definido por qualquer coisa que possa causar um retorno de chamada de função.

Como os retornos de chamada de evento não recebem notificações específicas de fechamento, conclusão ou abertura, um aplicativo pode precisar verificar o status do processo que está aguardando depois que o evento ocorre. É possível que várias tarefas possam ser concluídas no momento em que **WaitForSingleObject** retorna.

 

 