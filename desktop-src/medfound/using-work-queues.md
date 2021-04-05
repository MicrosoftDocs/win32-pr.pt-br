---
description: Este tópico descreve como usar as filas de trabalho no Microsoft Media Foundation.
ms.assetid: 6be05df7-e8ff-4110-8f73-a62eb31fd414
title: Usando filas de trabalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7bb41b830742ca871d44cadac9bd26a9967aa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164880"
---
# <a name="using-work-queues"></a>Usando filas de trabalho

Este tópico descreve como usar as filas de trabalho no Microsoft Media Foundation.

-   [Usando filas de trabalho](#using-work-queues)
-   [Desligando filas de trabalho](#shutting-down-work-queues)
-   [Usando itens de trabalho agendados](#using-scheduled-work-items)
-   [Usando retornos de chamada periódicos](#using-periodic-callbacks)
-   [Tópicos relacionados](#related-topics)

## <a name="using-work-queues"></a>Usando filas de trabalho

Uma fila de trabalho é uma maneira eficiente de executar operações assíncronas em outro thread. Conceitualmente, você coloca itens de trabalho na fila e a fila tem um thread que recebe cada item da fila e o despacha. Os itens de trabalho são implementados como retornos de chamada usando a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .

Media Foundation cria várias filas de trabalho padrão, chamadas de *filas de trabalho da plataforma*. Os aplicativos também podem criar suas próprias filas de trabalho, chamadas de *filas de trabalho privadas*. Para obter uma lista das filas de trabalho da plataforma, consulte [identificadores de fila de trabalho](work-queue-identifiers.md). Para criar uma fila de trabalho particular, chame [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue). Essa função retorna um identificador para a nova fila de trabalho. Para colocar um item na fila, chame [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) ou [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex). Em ambos os casos, você deve especificar uma interface de retorno de chamada.

-   [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) usa um ponteiro para a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , além de um objeto de estado opcional que implementa **IUnknown**. Esses são os mesmos parâmetros usados em métodos assíncronos, conforme descrito no tópico [métodos de retorno de chamada assíncronos](asynchronous-callback-methods.md). Internamente, essa função cria um objeto de resultado assíncrono, que é passado para o método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) do retorno de chamada.
-   [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) usa um ponteiro para a interface [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) . Essa interface representa um objeto de resultado assíncrono. Crie esse objeto chamando [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) e especificando sua interface de retorno de chamada e, opcionalmente, um objeto de estado.

Em ambos os casos, o thread da fila de trabalho chama o método [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) . Use o método **Invoke** para executar o item de trabalho.

Se mais de um thread ou componente compartilhar a mesma fila de trabalho, você poderá chamar [**MFLockWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflockworkqueue) para bloquear a fila de trabalho, o que impede que a plataforma a libere. Para cada chamada para [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) ou **MFLockWorkQueue**, você deve chamar [**MFUnlockWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockworkqueue) uma vez para liberar a fila de trabalho. Por exemplo, se você criar uma nova fila de trabalho e, em seguida, bloqueá-la uma vez, deverá chamar **MFUnlockWorkQueue** duas vezes, uma vez para a chamada para **MFAllocateWorkQueue** e uma vez para a chamada para **MFLockWorkQueue**.

O código a seguir mostra como criar uma nova fila de trabalho, colocar um item de trabalho na fila e liberar a fila de trabalho.

Consulte [melhorias na fila de trabalho e threading](media-foundation-work-queue-and-threading-improvements.md) para obter informações adicionais sobre as filas de trabalho no Windows 8.


```C++
DWORD idWorkQueue = 0;
HRESULT hr = S_OK;

// Create a new work queue.
hr = MFAllocateWorkQueue(&idWorkQueue);

// Put an item on the queue.
if (SUCCEEDED(hr))
{
    hr = MFPutWorkItem(idWorkQueue, pCallback, NULL);
}

// Wait for the callback to be invoked.
if (SUCCEEDED(hr))
{
    WaitForSingleObject(hEvent, INFINITE);
}

// Release the work queue.
if (SUCCEEDED(hr))
{
    hr = MFUnlockWorkQueue(idWorkQueue);
}
```



Este exemplo pressupõe que *pCallback* é um ponteiro para a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) do aplicativo. Ele também pressupõe que o retorno de chamada define o identificador de evento *hEvent* . O código aguarda esse evento ser definido antes de chamar [**MFUnlockWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockworkqueue).

Os threads da fila de trabalho são sempre criados no processo do chamador. Em cada fila de trabalho, os retornos de chamada são serializados. Se você chamar [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) duas vezes com a mesma fila de trabalho, o segundo retorno de chamada não será invocado até que o primeiro retorno de chamada seja retornado.

## <a name="shutting-down-work-queues"></a>Desligando filas de trabalho

Antes de chamar [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown), libere todos os recursos que estão sendo usados por threads da fila de trabalho. Para sincronizar esse processo, você pode bloquear a plataforma Media Foundation, o que impede que a função **MFShutdown** feche todos os threads da fila de trabalho. Se **MFShutdown** for chamado enquanto a plataforma estiver bloqueada, o **MFShutdown** aguardará algumas centenas de milissegundos para que a plataforma seja desbloqueada. Se não estiver desbloqueado dentro desse período, o **MFShutdown** fechará os threads da fila de trabalho.

A implementação padrão do [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) bloqueia automaticamente a plataforma Media Foundation quando o objeto de resultado é criado. A liberação da interface desbloqueia a plataforma. Portanto, quase nunca será necessário bloquear a plataforma diretamente. Mas se você escrever sua própria implementação personalizada do **IMFAsyncResult**, deverá bloquear e desbloquear a plataforma manualmente. Para bloquear a plataforma, chame [**MFLockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mflockplatform). Para desbloquear a plataforma, chame [**MFUnlockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform). Para obter um exemplo, consulte [objetos de resultados assíncronos personalizados](custom-asynchronous-result-objects.md).

Depois de chamar o [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown), você precisa garantir que a plataforma seja desbloqueada dentro do período de tempo limite de 5 segundos. Faça isso liberando todos os ponteiros do [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) e chamando [**MFUnlockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform) se você tiver bloqueado a plataforma manualmente. Certifique-se de liberar todos os recursos que estão sendo usados por threads de fila de trabalho, ou seu aplicativo pode vazar memória.

Normalmente, se o aplicativo for desligado e lançar cada objeto de Media Foundation antes de chamar [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown), você não precisará se preocupar com o bloqueio. O mecanismo de bloqueio simplesmente permite que os threads da fila de trabalho saiam normalmente depois de chamar **MFShutdown**.

## <a name="using-scheduled-work-items"></a>Usando itens de trabalho agendados

Você pode agendar um retorno de chamada para ocorrer após um determinado período de tempo chamando [**MFScheduleWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem) ou [**MFScheduleWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex).

-   [**MFScheduleWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem) usa um ponteiro para o retorno de chamada, um objeto de estado opcional e um intervalo de tempo limite.
-   [**MFScheduleWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex) usa um ponteiro para um objeto de resultado assíncrono e um valor de tempo limite.

Especifique o tempo limite como um valor negativo em milissegundos. Por exemplo, para agendar um retorno de chamada a ser invocado em 5 segundos, use o valor − 5000. Ambas as funções retornam um valor de **\_ chave MFWORKITEM** , que pode ser usado para cancelar o retorno de chamada, passando-o para a função [**MFCancelWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfcancelworkitem) .

Os itens de trabalho agendados sempre usam a fila de trabalho do timer da fila de retorno de chamada do MFASYNC \_ \_ \_ .

## <a name="using-periodic-callbacks"></a>Usando retornos de chamada periódicos

A função [**MFAddPeriodicCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback) agenda um retorno de chamada para ser invocado periodicamente até você cancelá-lo. O intervalo de retorno de chamada é fixo; os aplicativos não podem alterá-lo. Para descobrir o intervalo exato, chame [**MFGetTimerPeriodicity**](/windows/desktop/api/mfapi/nf-mfapi-mfgettimerperiodicity). O intervalo está na ordem de 10 milissegundos, portanto, essa função é destinada a situações em que você precisa de um "tique", como a implementação de um relógio de apresentação. Se você quiser agendar a ocorrência de uma operação com menos frequência, use um item de trabalho agendado, conforme descrito anteriormente.

Ao contrário dos outros retornos de chamada descritos neste tópico, o retorno de chamada periódico não usa a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) . Em vez disso, ele usa um ponteiro de função. Para obter mais informações, consulte [**retorno de chamada MFPERIODICCALLBACK**](/windows/win32/api/mfapi/nc-mfapi-mfperiodiccallback).

Para cancelar o retorno de chamada periódico, chame [**MFRemovePeriodicCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfremoveperiodiccallback).

Retornos de chamada periódicos usam a \_ fila de trabalho da plataforma de retorno de chamada MFASYNC \_ \_ .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filas de trabalho](work-queues.md)
</dt> <dt>

[**MFASYNCRESULT**](/windows/win32/api/mfapi/ns-mfapi-mfasyncresult)
</dt> <dt>

[Aprimoramentos na fila de trabalho e threading](media-foundation-work-queue-and-threading-improvements.md)
</dt> </dl>

 

 
