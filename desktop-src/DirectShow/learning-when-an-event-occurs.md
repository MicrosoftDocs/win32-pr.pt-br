---
description: Learning Quando ocorre um evento
ms.assetid: 4e44089b-676b-4220-9721-54ddf56bf760
title: Learning Quando ocorre um evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58696055bdf1e3cbf3cf36c4db4ae2258bda334956fcaa14f33eda96db249773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397212"
---
# <a name="learning-when-an-event-occurs"></a>Learning Quando ocorre um evento

para processar DirectShow eventos, um aplicativo precisa de uma maneira de descobrir quando os eventos estão aguardando na fila. o filtro Graph Manager fornece duas maneiras de fazer isso:

-   **Notificação de janela:** o filtro Graph Manager envia uma mensagem de Windows definida pelo usuário para uma janela de aplicativo sempre que houver um novo evento.
-   **Sinalização de evento:** o filtro Graph Manager sinaliza um evento de Windows se houver eventos de DirectShow na fila e redefinir o evento se a fila estiver vazia.

Um aplicativo pode usar qualquer técnica. A notificação de janela é geralmente mais simples.

**Notificação de janela**

Para configurar a notificação de janela, chame o método [**IMediaEventEx:: SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) e especifique uma mensagem privada. Os aplicativos podem usar números de mensagem no intervalo do \_ aplicativo do WM por meio do 0xBFFF como mensagens particulares. sempre que o filtro Graph Manager coloca uma nova notificação de evento na fila, ele posta essa mensagem na janela designada. O aplicativo responde à mensagem de dentro do loop de mensagem da janela.

O exemplo de código a seguir mostra como definir a janela de notificação.


```C++
#define WM_GRAPHNOTIFY WM_APP + 1   // Private message.
pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



a mensagem é uma mensagem de Windows comum e é postada separadamente da fila de notificação de eventos de DirectShow. A vantagem dessa abordagem é que a maioria dos aplicativos já implementa um loop de mensagem. portanto, você pode incorporar DirectShow manipulação de eventos sem muito trabalho adicional.

O exemplo de código a seguir mostra uma estrutura de tópicos de como responder à mensagem de notificação. Para obter um exemplo completo, consulte [respondendo a eventos](responding-to-events.md).


```C++
LRESULT CALLBACK WindowProc( HWND hwnd, UINT msg, UINT wParam, LONG lParam)
{
    switch (msg)
    {
        case WM_GRAPHNOTIFY:
            HandleEvent();  // Application-defined function.
            break;
        // Handle other Windows messages here too.
    }
    return (DefWindowProc(hwnd, msg, wParam, lParam));
}
```



Como a notificação de eventos e o loop de mensagem são assíncronas, a fila pode conter mais de um evento no momento em que seu aplicativo responde à mensagem. Além disso, os eventos podem, às vezes, ser limpos da fila se se tornarem inválidos. Portanto, no código de manipulação de eventos, chame [**IAMMediaEvent:: getregular**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) até que ele retorne um código de falha, indicando que a fila está vazia.

Antes de liberar o ponteiro [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) , cancele a notificação de eventos chamando [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) com um ponteiro **nulo** . Em seu código de processamento de eventos, verifique se o ponteiro **IMediaEventEx** é válido antes de chamar [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent). Essas etapas impedem um possível erro, no qual o aplicativo recebe a notificação de eventos depois de liberar o ponteiro **IMediaEventEx** .

**Sinalização de evento**

o filtro Graph Manager mantém um evento de redefinição manual que reflete o estado da fila de eventos. se a fila contiver notificações de eventos pendentes, o filtro Graph Manager sinalizará o evento de redefinição manual. Se a fila estiver vazia, uma chamada para o método [**IMediaEvent:: Getuniforme**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) redefinirá o evento. Um aplicativo pode usar esse evento para determinar o estado da fila.

> [!Note]  
> A terminologia pode ser confusa aqui. o evento de redefinição manual é o tipo de evento criado pela função Windows [**createevent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) ; Ele não tem nada a ver com os eventos definidos por DirectShow.

 

Chame o método [**IMediaEvent:: GetEventHandle**](/windows/desktop/api/Control/nf-control-imediaevent-geteventhandle) para obter um identificador para o evento de redefinição manual. Aguarde até que o evento seja sinalizado chamando uma função como [**WaitForMultipleObjects**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects). depois que o evento for sinalizado, chame [**IMediaEvent:: getevent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) para obter o evento DirectShow.

O código de exemplo a seguir ilustra essa abordagem. Ele obtém o identificador de evento e aguarda em intervalos de 100 milissegundos para que o evento seja sinalizado. Se o evento for sinalizado, **ele chamará GetEvent e** imprime o código do evento e os parâmetros do evento na janela do console. O loop termina quando o evento [**EC \_ Complete**](ec-complete.md) ocorre, indicando que a reprodução foi concluída.


```C++
HANDLE  hEvent; 
long    evCode, param1, param2;
BOOLEAN bDone = FALSE;
HRESULT hr = S_OK;
hr = pEvent->GetEventHandle((OAEVENT*)&hEvent);
if (FAILED(hr))
{
    /* Insert failure-handling code here. */
}

while(!bDone) 
{
    if (WAIT_OBJECT_0 == WaitForSingleObject(hEvent, 100))
    { 
        while (S_OK == pEvent->GetEvent(&evCode, &param1, &param2, 0)) 
        {
            printf("Event code: %#04x\n Params: %d, %d\n", evCode, param1, param2);
            pEvent->FreeEventParams(evCode, param1, param2);
            bDone = (EC_COMPLETE == evCode);
        }
    }
} 
```



Como o grafo de filtro define ou redefine automaticamente o evento quando apropriado, o aplicativo não deve fazer isso. Além disso, quando você libera o gráfico de filtro, o grafo de filtro fecha o identificador de evento, portanto, não use o identificador de evento após esse ponto.

 

 
