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
# <a name="handling-dvd-event-notifications"></a>Manipulando notificações de eventos de DVD

O navegador de DVD envia notificações para uma janela especificada pelo aplicativo quando determinados eventos ocorrem, como quando o domínio do DVD é alterado, quando um novo nível de gerenciamento pai é encontrado e quando o navegador de DVD está prestes a entrar em um bloco de ângulo. Os parâmetros de evento podem conter informações adicionais relacionadas ao evento. Mensagens de erro e avisos também são enviados dessa maneira. O aplicativo especifica a janela que manipulará as notificações de eventos usando o ponteiro [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) para chamar [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow), da seguinte maneira:


```C++
const DWORD WM_DVD_EVENT = WM_USER + 100;
hr = m_pIME->SetNotifyWindow(reinterpret_cast<OAHWND>(m_hWnd), WM_DVD_EVENT, 0);
```



No exemplo anterior, m \_ HWND é o HWND da janela para receber as mensagens e o evento de \_ DVD \_ do WM é a mensagem definida pelo aplicativo (maior que o usuário do WM \_ ) que irá sinalizar que um evento de DVD ocorreu. O evento em si é recuperado pelo aplicativo por meio de uma chamada para [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent). Como mais de um evento pode estar na fila de eventos em um determinado momento, o aplicativo deve chamar **GetEvent** dentro de um loop que se repete até que todos os eventos na fila tenham sido recuperados, como mostrado no exemplo de código a seguir.


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



Os eventos de DVD podem conter informações adicionais nos parâmetros *lParam1* ou *lParam2* , conforme ilustrado acima, onde a hora atual está contida em *lParam1*. O exemplo de código anterior é do aplicativo de exemplo de DVD em Dvdcore. cpp. Para obter uma lista completa de todos os eventos de DVD e seus parâmetros, consulte [códigos de notificação de eventos de DVD](dvd-notification-codes.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> </dl>

 

 



