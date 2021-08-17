---
description: Veja a seguir dicas e dicas a serem consideradas ao escrever um aplicativo para a TAPI 3
ms.assetid: 55aae46a-af5c-4b6d-89fc-9063f078bcd6
title: dicas e Dicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57d51e8c7e3f8c6e4a9e38b27fa5cfe4c10e45d37cfa67af095d573eea319614
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762926"
---
# <a name="hints-and-tips"></a>dicas e Dicas

Veja a seguir dicas e dicas a serem consideradas ao escrever um aplicativo para a TAPI 3:

1.  O [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) com indiretamente cria o Windows; Isso é especialmente importante para Threading de apartamento. Se um thread criar qualquer Windows, ele deverá processar mensagens. Se seus threads chamarem o **CoInitialize**, execute uma bomba de mensagem para evitar problemas. Por exemplo, COM pode parar de empacotar corretamente, ou métodos em interfaces COM, como **IGlobalInterfaceTable** podem travar.

    No Threading Apartment, você deve ter um bombeamento de mensagens, independentemente de você esperar por objetos de sincronização. Isso é particularmente importante se você tiver um aplicativo de console ou se você gravar um objeto de servidor local/remoto COM Apartment Threaded (em que você não tem um console ou uma GUI, mas o controle simplesmente "executa" no sistema).

    > [!Caution]  
    > Ao chamar as funções Wait e Synchronization, como [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep), [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects), [**WaitForMultipleObjectsEx**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)e assim por diante. Em vez disso, use [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) e processe as mensagens, ou use [**CoWaitForMultipleHandles**](/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles), que detectará automaticamente o tipo de apartamento em que o thread está (STA ou MTA) e aguardará em um loop modal com (se STA) ou em um bloco em **WaitForMultipleObjects** (se MTA). **MsgWaitForMultipleObjects** e **CoWaitForMultipleHandles** também processam mensagens do Windows de acordo com as regras com.

     

    Por exemplo, em vez de:

    `Sleep (5000);`

    Use:

    ``` syntax
     {
       DWORD dwSignalled;
       HANDLE heventDone = CreateEvent(0, FALSE, FALSE, 0);

       CoWaitForMultipleHandles (COWAIT_ALERTABLE,
                             5000,
                             1,
                             &heventDone,
                             &dwSignalled);

       CloseHandle(heventDone);
     }
    ```

2.  **ITTAPIEventNotification:: Event** é a função de evento apps chamada em um thread de retorno de chamada TAPI 3.

    Faça o mínimo na rotina de evento; em vez disso, use seu próprio thread sempre que possível.

    Lembre-se de que o exemplo de código a seguir é fornecido, mas não é um requisito.

    ```syntax
    #include <windows.h>

    HRESULT
    STDMETHODCALLTYPE
    CTAPIEventNotification::Event(
        TAPI_EVENT TapiEvent,
        IDispatch *pEvent)
    {
        //
        // Addref the event so that it does not go away.
        //
        pEvent->AddRef();

        //
        // Post a message for reference.
        //
        BOOL RetVal = PostMessage(
                                  ghDlg,
                                  WM_PRIVATETAPIEVENT,
                                  (WPARAM) TapiEvent,
                                  (LPARAM) pEvent
                                  );

        // If (RetVal == 0 ) process error here.

        return S_OK;
    }     
    ```

3.  Não manipule objetos COM depois de chamar [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize). Os resultados são imprevisíveis e prejudiciais a um aplicativo íntegro. Alguns exemplos em que isso pode ocorrer são threads de trabalho e destruidores de C++ que podem ser executados depois que um aplicativo chama **CoUninitialize**.

 

 
