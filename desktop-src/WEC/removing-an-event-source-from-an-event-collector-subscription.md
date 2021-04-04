---
title: Removendo uma origem do evento de uma assinatura iniciada pelo coletor
description: Você pode remover uma origem do evento de uma assinatura iniciada pelo coletor sem excluir a assinatura inteira.
ms.assetid: 6c9e0dbf-59a2-4db9-8fb8-0dbfda5cf38b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303e0a708c2b52225af83475674e5f60d1a8418d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822783"
---
# <a name="removing-an-event-source-from-a-collector-initiated-subscription"></a><span data-ttu-id="ce8e3-103">Removendo uma origem do evento de uma assinatura iniciada pelo coletor</span><span class="sxs-lookup"><span data-stu-id="ce8e3-103">Removing an Event Source from a Collector Initiated Subscription</span></span>

<span data-ttu-id="ce8e3-104">Você pode remover uma origem do evento de uma assinatura iniciada pelo coletor sem excluir a assinatura inteira.</span><span class="sxs-lookup"><span data-stu-id="ce8e3-104">You can remove an event source from a collector initiated subscription without deleting the entire subscription.</span></span> <span data-ttu-id="ce8e3-105">Você deve saber o endereço da origem do evento que deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="ce8e3-105">You must know the address of the event source that you want to delete.</span></span> <span data-ttu-id="ce8e3-106">Você pode encontrar o endereço de uma origem de evento associada a uma assinatura usando o exemplo de C++ mostrado em [exibindo as propriedades de uma assinatura do coletor de eventos](displaying-the-properties-of-an-event-collector-subscription.md)ou pode digitar o seguinte comando no prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="ce8e3-106">You can find the address of an event source that is associated to a subscription by using the C++ example shown in [Displaying the Properties of an Event Collector Subscription](displaying-the-properties-of-an-event-collector-subscription.md), or you can type the following command at the command prompt:</span></span>

<span data-ttu-id="ce8e3-107">a *assinatura* de **wecutil GS**</span><span class="sxs-lookup"><span data-stu-id="ce8e3-107">**wecutil gs** *SubscriptionName*</span></span>

<span data-ttu-id="ce8e3-108">Para listar as assinaturas atuais em um computador local, você pode usar o exemplo de código C++ mostrado em [listando assinaturas do coletor de eventos](listing-event-collector-subscriptions.md)ou pode digitar o seguinte comando no prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="ce8e3-108">To list the current subscriptions on a local computer, you can use the C++ code example shown in [Listing Event Collector Subscriptions](listing-event-collector-subscriptions.md), or you can type the following command at the command prompt:</span></span>

<span data-ttu-id="ce8e3-109">**wecutil es**</span><span class="sxs-lookup"><span data-stu-id="ce8e3-109">**wecutil es**</span></span>

> [!Note]
>
> <span data-ttu-id="ce8e3-110">Você pode usar este exemplo para remover uma origem de evento de uma assinatura iniciada pelo coletor ou pode digitar o seguinte comando no prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="ce8e3-110">You can use this example to remove an event source from a collector initiated subscription or you can type the following command at the command prompt:</span></span>
>
> <span data-ttu-id="ce8e3-111">**wecutil SS** *subscriptionname*  \* */ESA: \* \* \* EventSourceAddress* **/res**</span><span class="sxs-lookup"><span data-stu-id="ce8e3-111">**wecutil ss** *SubscriptionName* \**/esa:\*\*\*EventSourceAddress* **/res**</span></span>
>
> <span data-ttu-id="ce8e3-112">*EventSourceAddress* pode ser localhost para o computador local ou um nome de domínio totalmente qualificado para um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="ce8e3-112">*EventSourceAddress* can be either localhost for the local computer or a fully qualified domain name for a remote computer.</span></span>

 

<span data-ttu-id="ce8e3-113">Este exemplo segue uma série de etapas para remover uma origem de evento de uma assinatura iniciada pelo coletor.</span><span class="sxs-lookup"><span data-stu-id="ce8e3-113">This example follows a series of steps to remove an event source from a collector-initiated subscription.</span></span>

<span data-ttu-id="ce8e3-114">**Para remover uma origem do evento de uma assinatura iniciada pelo coletor**</span><span class="sxs-lookup"><span data-stu-id="ce8e3-114">**To remove an event source from a collector-initiated subscription**</span></span>

1.  <span data-ttu-id="ce8e3-115">Abra a assinatura existente fornecendo o nome da assinatura e os direitos de acesso como parâmetros para a função [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) .</span><span class="sxs-lookup"><span data-stu-id="ce8e3-115">Open the existing subscription by providing the subscription name and access rights as parameters to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function.</span></span> <span data-ttu-id="ce8e3-116">Para obter mais informações sobre direitos de acesso, consulte as [**constantes do coletor de eventos do Windows**](windows-event-collector-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ce8e3-116">For more information about access rights, see [**Windows Event Collector Constants**](windows-event-collector-constants.md).</span></span>
2.  <span data-ttu-id="ce8e3-117">Obtenha a matriz de fontes de eventos da assinatura chamando a função [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) .</span><span class="sxs-lookup"><span data-stu-id="ce8e3-117">Get the event sources array of the subscription by calling the [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) function.</span></span> <span data-ttu-id="ce8e3-118">Para obter mais informações sobre as propriedades de assinatura que podem ser recuperadas, consulte a enumeração de [**ID de propriedade da assinatura do EC \_ \_ \_**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) .</span><span class="sxs-lookup"><span data-stu-id="ce8e3-118">For more information about subscription properties that can be retrieved, see the [**EC\_SUBSCRIPTION\_PROPERTY\_ID**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) enumeration.</span></span>
3.  <span data-ttu-id="ce8e3-119">Pesquise a origem do evento especificado na matriz origens do evento da assinatura chamando a função [**EcGetObjectArrayProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarrayproperty) .</span><span class="sxs-lookup"><span data-stu-id="ce8e3-119">Search for the specified event source in the event sources array of the subscription by calling the [**EcGetObjectArrayProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarrayproperty) function.</span></span> <span data-ttu-id="ce8e3-120">O valor da propriedade **EcSubscriptionEventSourceAddress** será localhost para o computador local ou será um nome de domínio totalmente qualificado para um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="ce8e3-120">The value of the **EcSubscriptionEventSourceAddress** property will be either Localhost for the local computer or will be a fully qualified domain name for a remote computer.</span></span> <span data-ttu-id="ce8e3-121">Para obter mais informações sobre as propriedades de origem do evento que podem ser recuperadas, consulte a enumeração da **ID de propriedade da assinatura do EC \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="ce8e3-121">For more information about event source properties that can be retrieved, see the **EC\_SUBSCRIPTION\_PROPERTY\_ID** enumeration.</span></span>
4.  <span data-ttu-id="ce8e3-122">Exclua a origem do evento da assinatura chamando a função [**EcRemoveObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecremoveobjectarrayelement) .</span><span class="sxs-lookup"><span data-stu-id="ce8e3-122">Delete the event source from the subscription by calling the [**EcRemoveObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecremoveobjectarrayelement) function.</span></span>
5.  <span data-ttu-id="ce8e3-123">Salve a assinatura chamando a função [**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) .</span><span class="sxs-lookup"><span data-stu-id="ce8e3-123">Save the subscription by calling the [**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) function.</span></span>
6.  <span data-ttu-id="ce8e3-124">Feche a assinatura chamando a função [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) .</span><span class="sxs-lookup"><span data-stu-id="ce8e3-124">Close the subscription by calling the [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) function.</span></span>

<span data-ttu-id="ce8e3-125">O exemplo de código C++ a seguir mostra como remover uma origem do evento de uma assinatura do coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="ce8e3-125">The following C++ code example shows how to remove an event source from an Event Collector subscription.</span></span>


```C++
#include <windows.h>
#include <EvColl.h>
#include <vector>
#include <string>
#include <strsafe.h>
#pragma comment(lib, "wecapi.lib")


// Subscription Information
DWORD GetSubscriptionProperty(EC_HANDLE hSubscription,  
    EC_SUBSCRIPTION_PROPERTY_ID propID, 
    DWORD flags, 
    std::vector<BYTE>& buffer, 
    PEC_VARIANT& vProperty);
DWORD GetEventSourceProperty(EC_OBJECT_ARRAY_PROPERTY_HANDLE hArray, 
    EC_SUBSCRIPTION_PROPERTY_ID propID, 
    DWORD arrayIndex, 
    DWORD flags, 
    std::vector<BYTE>& buffer, 
    PEC_VARIANT& vProper);



void __cdecl wmain()
{
    EC_HANDLE hSubscription;
    std::wstring eventSource = L"localhost";
    BOOL foundEventSource = false;
    LPCWSTR lpSubname = L"TestSubscription-CollectorInitiated";
    DWORD dwEventSourceCount;
    DWORD deleteEvent = 0; 
    DWORD dwRetVal = ERROR_SUCCESS;
    PEC_VARIANT vProperty = NULL;
    std::vector<BYTE> buffer;
    LPVOID lpwszBuffer;
    EC_OBJECT_ARRAY_PROPERTY_HANDLE hArray = NULL;

    // Step 1: Open an existing subscription.
    hSubscription = EcOpenSubscription(lpSubname,
        EC_READ_ACCESS | EC_WRITE_ACCESS,
        EC_OPEN_EXISTING);

    if (!hSubscription)
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 2: Get the event sources array to remove an event 
    // source from the subscription.
    dwRetVal = GetSubscriptionProperty(hSubscription, 
        EcSubscriptionEventSources,
        0,
        buffer,
        vProperty);
    if (ERROR_SUCCESS != dwRetVal)
    {
        goto Cleanup;
    }

    // Ensure that a handle to the event sources array has been obtained.
    if (vProperty->Type != EcVarTypeNull  && 
        vProperty->Type != EcVarObjectArrayPropertyHandle)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }

    hArray = (vProperty->Type == EcVarTypeNull)? NULL: 
        vProperty->PropertyHandleVal;
    if (!hArray)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }

    if (!EcGetObjectArraySize(hArray, &dwEventSourceCount))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 3: Search for the specified event source in the event source array.
    for (DWORD I = 0; I < dwEventSourceCount; I++)
    {
        dwRetVal = GetEventSourceProperty(hArray, 
            EcSubscriptionEventSourceAddress, 
            I,
            0,
            buffer,
            vProperty);
        if (ERROR_SUCCESS != dwRetVal)
        {
            goto Cleanup;
        }

        if (vProperty->StringVal == eventSource)
        {
            foundEventSource = true;
            deleteEvent = I;
            break;
        }
    }

    // Step 4: If the event source was found in the array, remove it.
    if (foundEventSource)
    {
        if (!EcRemoveObjectArrayElement(hArray, deleteEvent))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }
    }
    else
    {
        wprintf(L"Could not remove the event source from the subscription.\n");
        goto Cleanup;
    }

    // Step 5: Save the subscription to finalize the removal of the event source.
    if( !EcSaveSubscription(hSubscription, NULL) )
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 6: Close the subscription.
    Cleanup:
        if (hArray)
            EcClose(hArray);
        if (hSubscription)
            EcClose(hSubscription);

        if (dwRetVal != ERROR_SUCCESS)
        {
            FormatMessageW( FORMAT_MESSAGE_ALLOCATE_BUFFER | FORMAT_MESSAGE_FROM_SYSTEM,
                NULL,
                dwRetVal,
                0,
                (LPWSTR) &lpwszBuffer,
                0,
                NULL);
            
            if (!lpwszBuffer)
            {
                wprintf(L"Failed to FormatMessage.  Operation Error Code: %u." \
                    L"Error Code from FormatMessage: %u\n", dwRetVal, GetLastError());
                return;
            }

            wprintf(L"\nFailed to Perform Operation.\nError Code: %u\n" \
                L"Error Message: %s\n", dwRetVal, lpwszBuffer);

            LocalFree(lpwszBuffer);
        }
}

DWORD GetSubscriptionProperty(EC_HANDLE hSubscription, 
    EC_SUBSCRIPTION_PROPERTY_ID propID, 
    DWORD flags, 
    std::vector<BYTE>& buffer, 
    PEC_VARIANT& vProperty)
{
    DWORD  dwBufferSize, dwRetVal = ERROR_SUCCESS;
    buffer.resize(sizeof(EC_VARIANT));

    if (!hSubscription)
    return ERROR_INVALID_PARAMETER;

    // Get the value for the specified property. 
    if (!EcGetSubscriptionProperty(hSubscription,
        propID,
        flags,
        (DWORD) buffer.size(),
        (PEC_VARIANT)&buffer[0],
        &dwBufferSize))
    {
        dwRetVal = GetLastError();

        if (ERROR_INSUFFICIENT_BUFFER == dwRetVal)
        {
            dwRetVal = ERROR_SUCCESS;
            buffer.resize(dwBufferSize);

            if (!EcGetSubscriptionProperty(hSubscription,
                propID,
                flags,
                (DWORD) buffer.size(),
                (PEC_VARIANT)&buffer[0],
                &dwBufferSize))
            {
                dwRetVal = GetLastError();
            }
        }
    }

    if (dwRetVal == ERROR_SUCCESS)
    {
        vProperty = (PEC_VARIANT) &buffer[0];
    }
    else
    {
        vProperty = NULL;
    }

    return dwRetVal;
}

DWORD GetEventSourceProperty(EC_OBJECT_ARRAY_PROPERTY_HANDLE hArray, 
    EC_SUBSCRIPTION_PROPERTY_ID propID,
    DWORD arrayIndex,
    DWORD flags,
    std::vector<BYTE>& buffer,
    PEC_VARIANT& vProperty)
{
    UNREFERENCED_PARAMETER(flags);
    UNREFERENCED_PARAMETER(propID);
    
    DWORD  dwBufferSize, dwRetVal = ERROR_SUCCESS;
    buffer.resize(sizeof(EC_VARIANT));

    if (!hArray)
        return ERROR_INVALID_PARAMETER;

    // Obtain the value for the specified property. 
    if (!EcGetObjectArrayProperty(hArray,
        EcSubscriptionEventSourceAddress, 
        arrayIndex,
        0, 
        (DWORD) buffer.size(), 
        (PEC_VARIANT)&buffer[0],
        &dwBufferSize))
    {
        dwRetVal = GetLastError();

        if (ERROR_INSUFFICIENT_BUFFER == dwRetVal)
        {
            dwRetVal = ERROR_SUCCESS;
            buffer.resize(dwBufferSize);

            if (!EcGetObjectArrayProperty(hArray,
                EcSubscriptionEventSourceAddress,
                arrayIndex,
                0, 
                (DWORD) buffer.size(),
                (PEC_VARIANT)&buffer[0],
                &dwBufferSize))
            {
                dwRetVal = GetLastError();
            }
        }
    }

    if (dwRetVal == ERROR_SUCCESS)
    {
        vProperty = (PEC_VARIANT) &buffer[0];
    }
    else
    {
        vProperty = NULL;
    }

    return dwRetVal;
}
```



## <a name="related-topics"></a><span data-ttu-id="ce8e3-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ce8e3-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce8e3-127">Exibindo as propriedades de uma assinatura do coletor de eventos</span><span class="sxs-lookup"><span data-stu-id="ce8e3-127">Displaying the Properties of an Event Collector Subscription</span></span>](displaying-the-properties-of-an-event-collector-subscription.md)
</dt> <dt>

[<span data-ttu-id="ce8e3-128">Listando assinaturas do coletor de eventos</span><span class="sxs-lookup"><span data-stu-id="ce8e3-128">Listing Event Collector Subscriptions</span></span>](listing-event-collector-subscriptions.md)
</dt> <dt>

[<span data-ttu-id="ce8e3-129">Referência do coletor de eventos do Windows</span><span class="sxs-lookup"><span data-stu-id="ce8e3-129">Windows Event Collector Reference</span></span>](windows-event-collector-reference.md)
</dt> </dl>

 

 




