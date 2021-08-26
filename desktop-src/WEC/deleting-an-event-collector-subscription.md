---
title: Excluindo uma assinatura do coletor de eventos
description: Você pode excluir uma assinatura do coletor de eventos de um computador local.
ms.assetid: d3102149-906d-4286-85c8-e5b1eb6dd382
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9edf2f9dda2b6393ab147d5f58ff8f889952eaeb7f31f82080558697f117f3c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006086"
---
# <a name="deleting-an-event-collector-subscription"></a>Excluindo uma assinatura do coletor de eventos

Você pode excluir uma assinatura do coletor de eventos de um computador local. Você deve saber o nome da assinatura para poder excluí-la. Para obter mais informações sobre como listar as assinaturas atuais em um computador local, consulte [listando assinaturas do coletor de eventos](listing-event-collector-subscriptions.md)ou digite o seguinte comando no prompt de comando:

**wecutil es**

> [!Note]
>
> Você pode usar este exemplo para excluir uma assinatura do coletor de eventos ou pode digitar o seguinte comando no prompt de comando:
>
> **wecutil ds** *subscriptionname*

 

Depois de recuperar o nome da assinatura do coletor de eventos a ser excluída, você pode fornecer o nome da assinatura como um parâmetro para [**EcDeleteSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription).

O exemplo de código C++ a seguir mostra como excluir uma assinatura do coletor de eventos.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Listando assinaturas do coletor de eventos](listing-event-collector-subscriptions.md)
</dt> <dt>

[Windows Referência do coletor de eventos](windows-event-collector-reference.md)
</dt> </dl>

 

 




