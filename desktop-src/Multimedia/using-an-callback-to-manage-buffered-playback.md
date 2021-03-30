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
# <a name="using-an-event-callback-to-manage-buffered-playback"></a><span data-ttu-id="6a646-112">Usando um retorno de chamada de evento para gerenciar a reprodução em buffer</span><span class="sxs-lookup"><span data-stu-id="6a646-112">Using an Event Callback to Manage Buffered Playback</span></span>

<span data-ttu-id="6a646-113">Para usar um retorno de chamada de evento, use a função [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) para recuperar o identificador de um evento.</span><span class="sxs-lookup"><span data-stu-id="6a646-113">To use an event callback, use the [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to retrieve the handle of an event.</span></span> <span data-ttu-id="6a646-114">Em uma chamada para a função [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) , especifique \_ o evento de retorno de chamada para o parâmetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="6a646-114">In a call to the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function, specify CALLBACK\_EVENT for the *dwFlags* parameter.</span></span> <span data-ttu-id="6a646-115">Depois de usar a função [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) , mas antes de enviar eventos de MIDI para o dispositivo, crie um evento não sinalizado chamando a função [ResetEvent](/windows/win32/api/synchapi/nf-synchapi-resetevent) , especificando o identificador de evento recuperado por **CreateEvent**.</span><span class="sxs-lookup"><span data-stu-id="6a646-115">After using the [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) function but before sending MIDI events to the device, create a nonsignaled event by calling the [ResetEvent](/windows/win32/api/synchapi/nf-synchapi-resetevent) function, specifying the event handle retrieved by **CreateEvent**.</span></span> <span data-ttu-id="6a646-116">Em seguida, dentro de um loop que verifica se o \_ bit MHDR feito está definido no membro **dwFlags** da estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , use a função [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) , especificando o identificador de evento e um valor de tempo limite de infinito como parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6a646-116">Then, inside a loop that checks whether the MHDR\_DONE bit is set in the **dwFlags** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure, use the [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) function, specifying the event handle and a time-out value of INFINITE as parameters.</span></span>

<span data-ttu-id="6a646-117">Um retorno de chamada de evento é definido por qualquer coisa que possa causar um retorno de chamada de função.</span><span class="sxs-lookup"><span data-stu-id="6a646-117">An event callback is set by anything that might cause a function callback.</span></span>

<span data-ttu-id="6a646-118">Como os retornos de chamada de evento não recebem notificações específicas de fechamento, conclusão ou abertura, um aplicativo pode precisar verificar o status do processo que está aguardando depois que o evento ocorre.</span><span class="sxs-lookup"><span data-stu-id="6a646-118">Because event callbacks do not receive specific close, done, or open notifications, an application may need to check the status of the process it is waiting for after the event occurs.</span></span> <span data-ttu-id="6a646-119">É possível que várias tarefas possam ser concluídas no momento em que **WaitForSingleObject** retorna.</span><span class="sxs-lookup"><span data-stu-id="6a646-119">It is possible that a number of tasks could be completed by the time **WaitForSingleObject** returns.</span></span>

 

 