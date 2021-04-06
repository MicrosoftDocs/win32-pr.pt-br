---
description: Manipulando notificações de eventos de DVD
ms.assetid: 7a12aa36-f709-4ee2-aac6-45ab273ad3f9
title: Manipulando notificações de eventos de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8212f3eb9f868c494aa008602713c1750a6c6dc9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103920048"
---
# <a name="handling-dvd-event-notifications"></a><span data-ttu-id="f6996-103">Manipulando notificações de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="f6996-103">Handling DVD Event Notifications</span></span>

<span data-ttu-id="f6996-104">O navegador de DVD envia notificações para uma janela especificada pelo aplicativo quando determinados eventos ocorrem, como quando o domínio do DVD é alterado, quando um novo nível de gerenciamento pai é encontrado e quando o navegador de DVD está prestes a entrar em um bloco de ângulo.</span><span class="sxs-lookup"><span data-stu-id="f6996-104">The DVD Navigator sends notifications to an application-specified window when certain events take place, such as when the DVD domain changes, when a new parental management level is encountered, and when the DVD Navigator is about to enter an angle block.</span></span> <span data-ttu-id="f6996-105">Os parâmetros de evento podem conter informações adicionais relacionadas ao evento.</span><span class="sxs-lookup"><span data-stu-id="f6996-105">The event parameters can contain additional information related to the event.</span></span> <span data-ttu-id="f6996-106">Mensagens de erro e avisos também são enviados dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="f6996-106">Error messages and warnings are also sent in this way.</span></span> <span data-ttu-id="f6996-107">O aplicativo especifica a janela que manipulará as notificações de eventos usando o ponteiro [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) para chamar [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow), da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="f6996-107">The application specifies the window that will handle the event notifications by using the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pointer to call [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow), as follows:</span></span>


```C++
const DWORD WM_DVD_EVENT = WM_USER + 100;
hr = m_pIME->SetNotifyWindow(reinterpret_cast<OAHWND>(m_hWnd), WM_DVD_EVENT, 0);
```



<span data-ttu-id="f6996-108">No exemplo anterior, m \_ HWND é o HWND da janela para receber as mensagens e o evento de \_ DVD \_ do WM é a mensagem definida pelo aplicativo (maior que o usuário do WM \_ ) que irá sinalizar que um evento de DVD ocorreu.</span><span class="sxs-lookup"><span data-stu-id="f6996-108">In the preceding example, m\_hWnd is the HWND of the window to receive the messages and WM\_DVD\_EVENT is the application-defined message (greater than WM\_USER) that will signal that a DVD event has taken place.</span></span> <span data-ttu-id="f6996-109">O evento em si é recuperado pelo aplicativo por meio de uma chamada para [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent).</span><span class="sxs-lookup"><span data-stu-id="f6996-109">The event itself is retrieved by the application through a call to [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent).</span></span> <span data-ttu-id="f6996-110">Como mais de um evento pode estar na fila de eventos em um determinado momento, o aplicativo deve chamar **GetEvent** dentro de um loop que se repete até que todos os eventos na fila tenham sido recuperados, como mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="f6996-110">Because more than one event might be in the event queue at any given time, the application must call **GetEvent** within a loop that repeats until all queued events have been retrieved, as shown in the following code example.</span></span>


```C++
while (SUCCEEDED(m_pIME->GetEvent(&lEvent, &lParam1, &lParam2, lTimeOut)))
{
    HRESULT hr;
    switch (lEvent)
    {

    case EC_DVD_CURRENT_HMSF_TIME:
        {
            DVD_HMSF_TIMECODE *pTC = reinterpret_cast<DVD_HMSF_TIMECODE *>(&lParam1);
            m_CurTime = *pTC;
            ...
        }
        break;
        ...
    } // switch
}
```



<span data-ttu-id="f6996-111">Os eventos de DVD podem conter informações adicionais nos parâmetros *lParam1* ou *lParam2* , conforme ilustrado acima, onde a hora atual está contida em *lParam1*.</span><span class="sxs-lookup"><span data-stu-id="f6996-111">DVD events might contain additional information in the *lParam1* or *lParam2* parameters, as illustrated above where the current time is contained in *lParam1*.</span></span> <span data-ttu-id="f6996-112">O exemplo de código anterior é do aplicativo de exemplo de DVD em Dvdcore. cpp.</span><span class="sxs-lookup"><span data-stu-id="f6996-112">The preceding code example is from the DVD sample application in Dvdcore.cpp.</span></span> <span data-ttu-id="f6996-113">Para obter uma lista completa de todos os eventos de DVD e seus parâmetros, consulte [códigos de notificação de eventos de DVD](dvd-notification-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f6996-113">For a complete list of all DVD events and their parameters, see [DVD Event Notification Codes](dvd-notification-codes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6996-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f6996-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6996-115">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="f6996-115">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



