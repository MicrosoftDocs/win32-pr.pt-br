---
description: Este artigo descreve como responder a eventos que ocorrem em um grafo de filtro.
ms.assetid: 1c09149b-7f34-4296-bd32-dbbae5e1d62b
title: Respondendo a eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a51481371501c05733e5f637885a71001c1f996
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500387"
---
# <a name="responding-to-events"></a>Respondendo a eventos

Este artigo descreve como responder a eventos que ocorrem em um grafo de filtro.

## <a name="how-event-notification-works"></a>Como a notificação de eventos funciona

Enquanto um aplicativo do DirectShow está em execução, os eventos podem ocorrer no gráfico de filtro. Por exemplo, um filtro pode encontrar um erro de streaming. Os filtros alertam o Gerenciador de gráfico de filtro enviando eventos, que consistem em um código de evento e dois parâmetros de evento. O código do evento indica o tipo de evento e os parâmetros de evento fornecem informações adicionais. O significado dos parâmetros depende do código do evento. Para obter uma lista completa de códigos de eventos, consulte [códigos de notificação de eventos](event-notification-codes.md).

Alguns eventos são tratados silenciosamente pelo Gerenciador do grafo de filtro, sem que o aplicativo seja notificado. Outros eventos são colocados em uma fila para o aplicativo. Dependendo do aplicativo, há vários eventos que talvez você precise manipular. Este artigo se concentra em três eventos que são muito comuns:

-   O evento [**EC \_ Complete**](ec-complete.md) indica que a reprodução foi concluída normalmente.
-   O evento [**EC \_ userabort**](ec-userabort.md) indica que o usuário interrompeu a reprodução. Os renderizadores de vídeo enviam esse evento se o usuário fechar a janela de vídeo.
-   O [**evento \_ ERRORABORT do EC**](ec-errorabort.md) indica que um erro causou a interrupção da reprodução.

## <a name="using-event-notification"></a>Usando a notificação de eventos

Um aplicativo pode instruir o Gerenciador de gráficos de filtro a enviar uma mensagem do Windows para uma janela designada sempre que um novo evento ocorrer. Isso permite que o aplicativo responda dentro do loop de mensagem da janela. Primeiro, defina a mensagem que será enviada para a janela do aplicativo. Os aplicativos podem usar números de mensagem no intervalo do \_ aplicativo do WM por meio do 0xBFFF como mensagens particulares:


```C++
#define WM_GRAPHNOTIFY  WM_APP + 1
```



Em seguida, consulte o Gerenciador do grafo de filtro para a interface [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) e chame o método [**IMediaEventEx:: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) :


```C++
IMediaEventEx *g_pEvent = NULL;
g_pGraph->QueryInterface(IID_IMediaEventEx, (void **)&g_pEvent);
g_pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



Esse método designa a janela especificada (g \_ HWND) como o destinatário da mensagem. Chame o método depois de criar o gráfico de filtro, mas antes de executar o grafo.

\_O WM GRAPHNOTIFY é uma mensagem comum do Windows. Sempre que o Gerenciador de gráfico de filtro coloca um novo evento na fila de eventos, ele posta uma \_ mensagem do WM GRAPHNOTIFY na janela do aplicativo designada. O parâmetro *lParam* da mensagem é igual ao terceiro parâmetro em [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow). Esse parâmetro permite que você envie dados de instância com a mensagem. O parâmetro *wParam* da mensagem da janela é sempre zero.

Na função **WindowProc** do seu aplicativo, adicione uma instrução Case para a mensagem do WM \_ GRAPHNOTIFY:


```C++
case WM_GRAPHNOTIFY:
    HandleGraphEvent();
    break;
```



Na função do manipulador de eventos, chame o método [**IMediaEvent:: getuniforme**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) para recuperar eventos da fila:


```C++
void HandleGraphEvent()
{
    // Disregard if we don't have an IMediaEventEx pointer.
    if (g_pEvent == NULL)
    {
        return;
    }
    // Get all the events
    long evCode;
    LONG_PTR param1, param2;
    HRESULT hr;
    while (SUCCEEDED(g_pEvent->GetEvent(&evCode, &param1, &param2, 0)))
    {
        g_pEvent->FreeEventParams(evCode, param1, param2);
        switch (evCode)
        {
        case EC_COMPLETE:  // Fall through.
        case EC_USERABORT: // Fall through.
        case EC_ERRORABORT:
            CleanUp();
            PostQuitMessage(0);
            return;
        }
    } 
}
```



O método [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) recupera o código do evento e os dois parâmetros de evento. O quarto parâmetro **GetEvent** especifica o período de tempo a aguardar por um evento, em milissegundos. Como o aplicativo chama esse método em resposta a uma \_ mensagem do WM GRAPHNOTIFY, o evento já está na fila. Portanto, definimos o valor de tempo limite como zero.

A notificação de eventos e o loop de mensagem são assíncronas, portanto, a fila pode conter mais de um evento no momento em que seu aplicativo responde à mensagem. Além disso, o Gerenciador de gráfico de filtro pode remover determinados eventos da fila, se eles se tornarem inválidos. Portanto, você deve chamar [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) até que ele retorne um código de falha, indicando que a fila está vazia.

Neste exemplo, o aplicativo responde ao [**EC \_ concluído**](ec-complete.md), ao [**EC \_ userabort**](ec-userabort.md)e ao [**EC \_ ERRORABORT**](ec-errorabort.md) invocando a função de limpeza definida pelo aplicativo, o que faz com que o aplicativo saia normalmente. O exemplo ignora os dois parâmetros de evento. Depois de recuperar um evento, chame [**IMediaEvent:: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) para todos os recursos gratuitos associados aos parâmetros do evento.

Observe que um evento de [**\_ conclusão de EC**](ec-complete.md) não faz com que o grafo de filtro pare. O aplicativo pode parar ou pausar o grafo. Se você parar o grafo, os filtros liberarão todos os recursos que estiverem mantendo. Se você pausar o grafo, os filtros continuarão a manter os recursos. Além disso, quando um processador de vídeo é pausado, ele exibe uma imagem estática do quadro mais recente.

Antes de liberar o ponteiro [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) , cancele a notificação de eventos chamando [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) com um identificador de janela **nulo** :


```C++
// Disable event notification before releasing the graph.
g_pEvent->SetNotifyWindow(NULL, 0, 0);
g_pEvent->Release();
g_pEvent = NULL;
```



No manipulador de \_ mensagens GRAPHNOTIFY do WM, verifique o ponteiro [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) antes de chamar [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent):


```C++
if (g_pEvent == NULL) return;
```



Isso impede um possível erro que pode ocorrer se o aplicativo receber a notificação de eventos depois de liberar o ponteiro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tarefas básicas do DirectShow](basic-directshow-tasks.md)
</dt> <dt>

[Notificação de eventos no DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



