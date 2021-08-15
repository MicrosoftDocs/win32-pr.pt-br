---
title: Usando um retorno de chamada de evento para gerenciar a reprodução em buffer
description: Usando um retorno de chamada de evento para gerenciar a reprodução em buffer
ms.assetid: 3b60daea-574d-430b-b14e-1fefceb69dfb
keywords:
- MIDI (Instrument Digital Interface Instrument), reprodução em buffer
- MIDI (Interface Digital do Instrument Instrument), reprodução em buffer
- reproduzindo arquivos MIDI, reprodução em buffer
- reprodução em buffer
- Função CreateEvent
- MIDI (Interface Digital do Instrument Instrument), retorno de chamada de evento
- MIDI (Interface Digital do Instrument Instrument), retorno de chamada de evento
- reprodução de arquivos MIDI, retorno de chamada de evento
- retorno de chamada de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 747652c10471662daacfe433a8fc22d5248bf2fe2365b6b314e76d0b91ced127
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370262"
---
# <a name="using-an-event-callback-to-manage-buffered-playback"></a>Usando um retorno de chamada de evento para gerenciar a reprodução em buffer

Para usar um retorno de chamada de evento, use a [função CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) para recuperar o handle de um evento. Em uma chamada para a [**função midiOutOpen,**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) especifique CALLBACK \_ EVENT para o parâmetro *dwFlags.* Depois de usar a função [**midiOutPrepareHeader,**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) mas antes de enviar eventos MIDI para o dispositivo, crie um evento sem sinal chamando a função [ResetEvent,](/windows/win32/api/synchapi/nf-synchapi-resetevent) especificando o handle de evento recuperado por **CreateEvent**. Em seguida, dentro de um loop que verifica se o bit MHDR DONE está definido no membro \_ **dwFlags** da estrutura [**MIDIHDR,**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) use a [função WaitForSingleObject,](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) especificando o handle de evento e um valor de tempo-out infinite como parâmetros.

Um retorno de chamada de evento é definido por qualquer coisa que possa causar um retorno de chamada de função.

Como os retornos de chamada de evento não recebem notificações específicas próximas, feitas ou abertas, um aplicativo pode precisar verificar o status do processo que está aguardando após o evento ocorrer. É possível que várias tarefas sejam concluídas pelo tempo **que WaitForSingleObject** retornar.

 

 