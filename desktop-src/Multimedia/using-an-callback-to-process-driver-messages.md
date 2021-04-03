---
title: Usando um retorno de chamada de evento para processar mensagens de driver
description: Usando um retorno de chamada de evento para processar mensagens de driver
ms.assetid: 5b17ff93-ed00-46ee-828c-baf716c9257c
keywords:
- áudio de onda, retorno de chamada de evento
- blocos de dados de áudio, retorno de chamada de evento
- áudio de onda, mensagens de driver de processamento
- blocos de dados de áudio, processando mensagens de driver
- Processando mensagens do driver
- Função CreateEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cbfeb95fcf0e5d83f9a54fc0cf3cd223ac6ce19
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640628"
---
# <a name="using-an-event-callback-to-process-driver-messages"></a><span data-ttu-id="def7e-109">Usando um retorno de chamada de evento para processar mensagens de driver</span><span class="sxs-lookup"><span data-stu-id="def7e-109">Using an Event Callback to Process Driver Messages</span></span>

<span data-ttu-id="def7e-110">Para usar um retorno de chamada de evento, use a função [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) para criar um evento de redefinição manual.</span><span class="sxs-lookup"><span data-stu-id="def7e-110">To use an event callback, use the [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) function to create a manual-reset event.</span></span> <span data-ttu-id="def7e-111">Na chamada para a função [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) , especifique o **\_ evento de retorno de chamada** para o parâmetro *fdwOpen* .</span><span class="sxs-lookup"><span data-stu-id="def7e-111">In the call to the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function, specify **CALLBACK\_EVENT** for the *fdwOpen* parameter.</span></span> <span data-ttu-id="def7e-112">Depois de chamar a função [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) , mas antes de enviar dados de formato de onda-áudio para o dispositivo, coloque o evento em um estado não sinalizado chamando a função [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent) .</span><span class="sxs-lookup"><span data-stu-id="def7e-112">After you call the [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) function, but before sending waveform-audio data to the device, put the event into a nonsignaled state by calling the [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent) function.</span></span> <span data-ttu-id="def7e-113">Em seguida, dentro de um loop que verifica se o sinalizador **WHDR \_ concluído** está definido no membro **dwFlags** da estrutura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) , chame a função [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) , especificando como parâmetros o identificador de evento e um valor de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="def7e-113">Then, inside a loop that checks whether the **WHDR\_DONE** flag is set in the **dwFlags** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure, call the [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) function, specifying as parameters the event handle and a time-out value.</span></span>

<span data-ttu-id="def7e-114">Como os retornos de chamada de evento não recebem notificações específicas de fechamento, conclusão ou abertura, um aplicativo pode ter que verificar o status do processo que está aguardando após o evento ocorrer.</span><span class="sxs-lookup"><span data-stu-id="def7e-114">Because event callbacks do not receive specific close, done, or open notifications, an application might have to check the status of the process it is waiting for after the event occurs.</span></span> <span data-ttu-id="def7e-115">É possível que várias tarefas tenham sido concluídas no momento em que [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) retorna.</span><span class="sxs-lookup"><span data-stu-id="def7e-115">It is possible that a number of tasks could have been completed by the time [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) returns.</span></span>

## <a name="related-topics"></a><span data-ttu-id="def7e-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="def7e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="def7e-117">Blocos de dados de áudio</span><span class="sxs-lookup"><span data-stu-id="def7e-117">Audio Data Blocks</span></span>](audio-data-blocks.md)
</dt> </dl>

 

 