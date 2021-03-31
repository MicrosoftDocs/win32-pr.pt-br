---
title: Excluindo uma assinatura do coletor de eventos
description: Você pode excluir uma assinatura do coletor de eventos de um computador local.
ms.assetid: d3102149-906d-4286-85c8-e5b1eb6dd382
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47cec036625bbb94e33e71af0f1d9808ad9252a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635779"
---
# <a name="deleting-an-event-collector-subscription"></a><span data-ttu-id="473f8-103">Excluindo uma assinatura do coletor de eventos</span><span class="sxs-lookup"><span data-stu-id="473f8-103">Deleting an Event Collector Subscription</span></span>

<span data-ttu-id="473f8-104">Você pode excluir uma assinatura do coletor de eventos de um computador local.</span><span class="sxs-lookup"><span data-stu-id="473f8-104">You can delete an Event Collector subscription from a local computer.</span></span> <span data-ttu-id="473f8-105">Você deve saber o nome da assinatura para poder excluí-la.</span><span class="sxs-lookup"><span data-stu-id="473f8-105">You must know the name of the subscription before you can delete it.</span></span> <span data-ttu-id="473f8-106">Para obter mais informações sobre como listar as assinaturas atuais em um computador local, consulte [listando assinaturas do coletor de eventos](listing-event-collector-subscriptions.md)ou digite o seguinte comando no prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="473f8-106">For more information about how to list the current subscriptions on a local computer, see [Listing Event Collector Subscriptions](listing-event-collector-subscriptions.md), or type the following command at the command prompt:</span></span>

<span data-ttu-id="473f8-107">**wecutil es**</span><span class="sxs-lookup"><span data-stu-id="473f8-107">**wecutil es**</span></span>

> [!Note]
>
> <span data-ttu-id="473f8-108">Você pode usar este exemplo para excluir uma assinatura do coletor de eventos ou pode digitar o seguinte comando no prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="473f8-108">You can use this example to delete an Event Collector subscription or you can type the following command at the command prompt:</span></span>
>
> <span data-ttu-id="473f8-109">**wecutil ds** *subscriptionname*</span><span class="sxs-lookup"><span data-stu-id="473f8-109">**wecutil ds** *SubscriptionName*</span></span>

 

<span data-ttu-id="473f8-110">Depois de recuperar o nome da assinatura do coletor de eventos a ser excluída, você pode fornecer o nome da assinatura como um parâmetro para [**EcDeleteSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription).</span><span class="sxs-lookup"><span data-stu-id="473f8-110">After you retrieve the name of the Event Collector subscription to delete, you can provide the name of the subscription as a parameter to [**EcDeleteSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription).</span></span>

<span data-ttu-id="473f8-111">O exemplo de código C++ a seguir mostra como excluir uma assinatura do coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="473f8-111">The following C++ code example shows how to delete an Event Collector subscription.</span></span>


```C++
#include <windows.h>
#include <EvColl.h>
#include <strsafe.h>

#pragma comment(lib, "wecapi.lib")

void __cdecl wmain()
{
    DWORD dwRetVal;
    LPWSTR lpSubname = L"MyTestSubscription";

    // Delete the specified Event Collector subscription.
    if (!EcDeleteSubscription(lpSubname, 0))
    {
        dwRetVal = GetLastError();
        LPVOID lpwszBuffer;

        FormatMessageW( FORMAT_MESSAGE_ALLOCATE_BUFFER | FORMAT_MESSAGE_FROM_SYSTEM,
            NULL,
            dwRetVal,
            0,
            (LPWSTR) &lpwszBuffer,
            0,
            NULL);

        if (!lpwszBuffer)
        {
            wprintf(L"Failed to FormatMessage.  Operation Error Code: %u." 
                L"Error Code from FormatMessage: %u\n", dwRetVal, GetLastError());
            return;
        }

        wprintf(L"\nFailed to Perform Operation.\nError Code: %u\n"
            L"Error Message: %s\n", dwRetVal, lpwszBuffer);

        LocalFree(lpwszBuffer);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="473f8-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="473f8-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="473f8-113">Listando assinaturas do coletor de eventos</span><span class="sxs-lookup"><span data-stu-id="473f8-113">Listing Event Collector Subscriptions</span></span>](listing-event-collector-subscriptions.md)
</dt> <dt>

[<span data-ttu-id="473f8-114">Referência do coletor de eventos do Windows</span><span class="sxs-lookup"><span data-stu-id="473f8-114">Windows Event Collector Reference</span></span>](windows-event-collector-reference.md)
</dt> </dl>

 

 




