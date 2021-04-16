---
description: Veja a seguir dicas e dicas a serem consideradas ao escrever um aplicativo para a TAPI 3
ms.assetid: 55aae46a-af5c-4b6d-89fc-9063f078bcd6
title: Dicas e dicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9202bdef97fb87b9f0736ed032b298af56917d8c
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105758120"
---
# <a name="hints-and-tips"></a><span data-ttu-id="36ab6-103">Dicas e dicas</span><span class="sxs-lookup"><span data-stu-id="36ab6-103">Hints and Tips</span></span>

<span data-ttu-id="36ab6-104">Veja a seguir dicas e dicas a serem consideradas ao escrever um aplicativo para a TAPI 3:</span><span class="sxs-lookup"><span data-stu-id="36ab6-104">The following are hints and tips to consider when writing an application for TAPI 3:</span></span>

1.  <span data-ttu-id="36ab6-105">O [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) com indiretamente cria o Windows; Isso é especialmente importante para Threading de apartamento.</span><span class="sxs-lookup"><span data-stu-id="36ab6-105">COM [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) indirectly creates windows; this is especially important for apartment threading.</span></span> <span data-ttu-id="36ab6-106">Se um thread criar qualquer Windows, ele deverá processar mensagens.</span><span class="sxs-lookup"><span data-stu-id="36ab6-106">If a thread creates any windows, it must process messages.</span></span> <span data-ttu-id="36ab6-107">Se seus threads chamarem o **CoInitialize**, execute uma bomba de mensagem para evitar problemas.</span><span class="sxs-lookup"><span data-stu-id="36ab6-107">If your threads call **CoInitialize**, run a message pump to prevent problems.</span></span> <span data-ttu-id="36ab6-108">Por exemplo, COM pode parar de empacotar corretamente, ou métodos em interfaces COM, como **IGlobalInterfaceTable** podem travar.</span><span class="sxs-lookup"><span data-stu-id="36ab6-108">For example, COM might stop marshalling properly, or methods on COM interfaces, such as **IGlobalInterfaceTable** might hang.</span></span>

    <span data-ttu-id="36ab6-109">No Threading Apartment, você deve ter um bombeamento de mensagens, independentemente de você esperar por objetos de sincronização.</span><span class="sxs-lookup"><span data-stu-id="36ab6-109">In apartment threading you must have a message pump regardless of whether you wait for synchronization objects.</span></span> <span data-ttu-id="36ab6-110">Isso é particularmente importante se você tiver um aplicativo de console ou se você gravar um objeto de servidor local/remoto COM Apartment Threaded (em que você não tem um console ou uma GUI, mas o controle simplesmente "executa" no sistema).</span><span class="sxs-lookup"><span data-stu-id="36ab6-110">This is particularly important if you have a console application or you write a COM local/remote server object that is apartment threaded (where you do not have a console or a GUI, but the control just "runs" in the system).</span></span>

    > [!Caution]  
    > <span data-ttu-id="36ab6-111">Ao chamar as funções Wait e Synchronization, como [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep), [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects), [**WaitForMultipleObjectsEx**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="36ab6-111">When calling the wait and synchronization functions, such as [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep), [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects), [**WaitForMultipleObjectsEx**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex), and so on.</span></span> <span data-ttu-id="36ab6-112">Em vez disso, use [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) e processe as mensagens, ou use [**CoWaitForMultipleHandles**](/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles), que detectará automaticamente o tipo de apartamento em que o thread está (STA ou MTA) e aguardará em um loop modal com (se STA) ou em um bloco em **WaitForMultipleObjects** (se MTA).</span><span class="sxs-lookup"><span data-stu-id="36ab6-112">Instead, use [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) and process the messages, or use [**CoWaitForMultipleHandles**](/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles), which will automatically detect what type of apartment the thread is in (STA or MTA) and will wait either in a COM modal loop (if STA) or block on **WaitForMultipleObjects** (if MTA).</span></span> <span data-ttu-id="36ab6-113">**MsgWaitForMultipleObjects** e **CoWaitForMultipleHandles** também processam mensagens do Windows de acordo com as regras com.</span><span class="sxs-lookup"><span data-stu-id="36ab6-113">**MsgWaitForMultipleObjects** and **CoWaitForMultipleHandles** also process windows messages according to the COM rules.</span></span>

     

    <span data-ttu-id="36ab6-114">Por exemplo, em vez de:</span><span class="sxs-lookup"><span data-stu-id="36ab6-114">For example, instead of:</span></span>

    `Sleep (5000);`

    <span data-ttu-id="36ab6-115">Use:</span><span class="sxs-lookup"><span data-stu-id="36ab6-115">Use:</span></span>

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

2.  <span data-ttu-id="36ab6-116">**ITTAPIEventNotification:: Event** é a função de evento apps chamada em um thread de retorno de chamada TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="36ab6-116">**ITTAPIEventNotification::Event** is the apps Event function called on a TAPI 3 callback thread.</span></span>

    <span data-ttu-id="36ab6-117">Faça o mínimo na rotina de evento; em vez disso, use seu próprio thread sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="36ab6-117">Do the minimum in the Event routine; instead, use your own thread where possible.</span></span>

    <span data-ttu-id="36ab6-118">Lembre-se de que o exemplo de código a seguir é fornecido, mas não é um requisito.</span><span class="sxs-lookup"><span data-stu-id="36ab6-118">Be aware that the following code example is provided, but is not a requirement.</span></span>

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

3.  <span data-ttu-id="36ab6-119">Não manipule objetos COM depois de chamar [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize).</span><span class="sxs-lookup"><span data-stu-id="36ab6-119">Do not manipulate COM objects after calling [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize).</span></span> <span data-ttu-id="36ab6-120">Os resultados são imprevisíveis e prejudiciais a um aplicativo íntegro.</span><span class="sxs-lookup"><span data-stu-id="36ab6-120">The results are unpredictable and detrimental to a healthy application.</span></span> <span data-ttu-id="36ab6-121">Alguns exemplos em que isso pode ocorrer são threads de trabalho e destruidores de C++ que podem ser executados depois que um aplicativo chama **CoUninitialize**.</span><span class="sxs-lookup"><span data-stu-id="36ab6-121">Some examples in which this can happen are worker threads and C++ destructors that may execute after an application calls **CoUninitialize**.</span></span>

 

 
