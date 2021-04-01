---
title: Criando uma assinatura iniciada pelo código-fonte
description: As assinaturas iniciadas pela origem permitem que você defina uma assinatura em um computador do coletor de eventos sem definir os computadores de origem do evento e, em seguida, vários computadores remotos de origem do evento podem ser configurados (usando uma configuração de política de grupo) para encaminhar eventos para o computador do coletor de eventos. Antes que um computador local possa assinar eventos e um computador remoto possa encaminhar eventos, ambos os computadores devem ser configurados para coleta de eventos e encaminhamento de eventos. Para obter mais informações sobre como configurar os computadores, consulte Configurando uma assinatura iniciada por origem.
ms.assetid: 489d3613-177f-4045-a055-2c1577ef2191
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e0e6d4aa7c94afcdbe6458c2c23c214d935db2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641533"
---
# <a name="creating-a-source-initiated-subscription"></a><span data-ttu-id="60053-105">Criando uma assinatura iniciada pelo código-fonte</span><span class="sxs-lookup"><span data-stu-id="60053-105">Creating a Source Initiated Subscription</span></span>

<span data-ttu-id="60053-106">As assinaturas iniciadas pela origem permitem que você defina uma assinatura em um computador do coletor de eventos sem definir os computadores de origem do evento e, em seguida, vários computadores remotos de origem do evento podem ser configurados (usando uma configuração de política de grupo) para encaminhar eventos para o computador do coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="60053-106">Source-initiated subscriptions allow you to define a subscription on an event collector computer without defining the event source computers, and then multiple remote event source computers can be set up (using a group policy setting) to forward events to the event collector computer.</span></span> <span data-ttu-id="60053-107">Antes que um computador local possa assinar eventos e um computador remoto possa encaminhar eventos, ambos os computadores devem ser configurados para coleta de eventos e encaminhamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="60053-107">Before a local computer can subscribe to events and a remote computer can forward events, both computers must be set up for event collecting and event forwarding.</span></span> <span data-ttu-id="60053-108">Para obter mais informações sobre como configurar os computadores, consulte [Configurando uma assinatura iniciada por origem](setting-up-a-source-initiated-subscription.md).</span><span class="sxs-lookup"><span data-stu-id="60053-108">For more information about how to configure the computers, see [Setting up a Source Initiated Subscription](setting-up-a-source-initiated-subscription.md).</span></span>

<span data-ttu-id="60053-109">O exemplo de código a seguir segue uma série de etapas para criar uma assinatura iniciada pela fonte em que as origens do evento estão no mesmo domínio que o computador do coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="60053-109">The following code example follows a series of steps to create a source initiated subscription where the event sources are in the same domain as the event collector computer.</span></span>

<span data-ttu-id="60053-110">**Para criar programaticamente uma assinatura iniciada pela fonte**</span><span class="sxs-lookup"><span data-stu-id="60053-110">**To programmatically create a source-initiated subscription**</span></span>

1.  <span data-ttu-id="60053-111">Abra a assinatura fornecendo o nome da assinatura e os direitos de acesso como parâmetros para a função [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) .</span><span class="sxs-lookup"><span data-stu-id="60053-111">Open the subscription by providing the subscription name and access rights as parameters to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function.</span></span> <span data-ttu-id="60053-112">Para obter mais informações sobre direitos de acesso, consulte as [**constantes do coletor de eventos do Windows**](windows-event-collector-constants.md).</span><span class="sxs-lookup"><span data-stu-id="60053-112">For more information about access rights, see [**Windows Event Collector Constants**](windows-event-collector-constants.md).</span></span>
2.  <span data-ttu-id="60053-113">Defina as propriedades da assinatura chamando a função [**EcSetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetsubscriptionproperty) .</span><span class="sxs-lookup"><span data-stu-id="60053-113">Set the properties of the subscription by calling the [**EcSetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetsubscriptionproperty) function.</span></span> <span data-ttu-id="60053-114">Para obter mais informações sobre as propriedades de assinatura que podem ser definidas, consulte a enumeração de [**ID de propriedade da assinatura do EC \_ \_ \_**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) .</span><span class="sxs-lookup"><span data-stu-id="60053-114">For more information about subscription properties that can be set, see the [**EC\_SUBSCRIPTION\_PROPERTY\_ID**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) enumeration.</span></span>
3.  <span data-ttu-id="60053-115">Salve a assinatura chamando a função [**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) .</span><span class="sxs-lookup"><span data-stu-id="60053-115">Save the subscription by calling the [**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) function.</span></span>
4.  <span data-ttu-id="60053-116">Feche a assinatura chamando a função [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) .</span><span class="sxs-lookup"><span data-stu-id="60053-116">Close the subscription by calling the [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) function.</span></span>

<span data-ttu-id="60053-117">O exemplo de C++ a seguir mostra como criar uma assinatura de origem iniciada:</span><span class="sxs-lookup"><span data-stu-id="60053-117">The following C++ example shows how to create a source initiated subscription:</span></span>


```C++
#include <windows.h>
#include <iostream>
using namespace std;
#include <string>
#include <xstring>
#include <conio.h>
#include <EvColl.h>
#include <vector>
#include <wincred.h>
#pragma comment(lib, "credui.lib")
#pragma comment(lib, "wecapi.lib")

// Track properties of the Subscription.
typedef struct _SUBSCRIPTION_SOURCE_INITIATED
{
    std::wstring Name;
    EC_SUBSCRIPTION_TYPE SubscriptionType;
    std::wstring Description;
    BOOL SubscriptionStatus;
    std::wstring URI;
    EC_SUBSCRIPTION_CONFIGURATION_MODE ConfigMode;
    EC_SUBSCRIPTION_DELIVERY_MODE DeliveryMode;
    DWORD MaxItems;
    DWORD MaxLatencyTime;
    DWORD HeartbeatInerval;
    time_t Expires;
    std::wstring Query;
    BOOL ReadExistingEvents;
    std::wstring TransportName;
    EC_SUBSCRIPTION_CONTENT_FORMAT ContentFormat;
    std::wstring DestinationLog;
    std::wstring AllowedSourceNonDomainComputers;
    std::wstring AllowedSourceDomainComputers;

} SUBSCRIPTION_SOURCE_INITIATED;

// Subscription Information
DWORD GetProperty(EC_HANDLE hSubscription,  
                  EC_SUBSCRIPTION_PROPERTY_ID propID, 
                  DWORD flags, 
                  std::vector<BYTE>& buffer, 
                  PEC_VARIANT& vProperty);


void __cdecl wmain()
{
    LPVOID lpwszBuffer;
    DWORD dwRetVal = ERROR_SUCCESS;
    EC_HANDLE hSubscription;
    EC_VARIANT vPropertyValue;
    std::vector<BYTE> buffer;
    PEC_VARIANT vProperty = NULL;
    SUBSCRIPTION_SOURCE_INITIATED sub;

    sub.Name = L"TestSubscription-SourceInitiated";
    sub.SubscriptionType = EcSubscriptionTypeSourceInitiated;
    sub.Description = L"A subscription that collects events that are published in\n" \
        L"the Microsoft-Windows-TaskScheduler/Operational log and forwards them \n" \
        L"to the ForwardedEvents log.";
    sub.URI = L"http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog";
    sub.Query = L"<QueryList>" \
        L"<Query Path=\"Microsoft-Windows-TaskScheduler/Operational\">" \
        L"<Select>*</Select>" \
        L"</Query>" \
        L"</QueryList>";
    sub.DestinationLog = L"ForwardedEvents";
    sub.ConfigMode = EcConfigurationModeCustom;
    sub.MaxItems = 5;
    sub.MaxLatencyTime = 1000;
    sub.HeartbeatInerval = 60000;
    sub.DeliveryMode = EcDeliveryModePush;
    sub.ContentFormat = EcContentFormatRenderedText;
    sub.ReadExistingEvents = true;
    sub.SubscriptionStatus = true;
    sub.TransportName = L"http";

    // This SDDL grants members of the Domain Computers domain group as well
    // as members of the Network Service group (for the local forwarder),
    // the ability to raise events for this subscription.
    sub.AllowedSourceDomainComputers = L"O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)";


    // Step 1: Open the Event Collector subscription.
    hSubscription = EcOpenSubscription(sub.Name.c_str(),
        EC_READ_ACCESS | EC_WRITE_ACCESS, 
        EC_CREATE_NEW);
    if ( !hSubscription)
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 2: Define the subscription properties.
    // Set the subscription type property (collector initiated).
    vPropertyValue.Type = EcVarTypeUInt32;
    vPropertyValue.UInt32Val = sub.SubscriptionType;
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionType,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the Description property that contains a description
    // of the subscription.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.Description.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionDescription,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }    

    // Set the URI property that specifies the URI of all the event sources.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.URI.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionURI,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the Query property that defines the query used by the event
    // source to select events that are forwarded to the event collector.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.Query.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionQuery,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the Log File property that specifies where the forwarded events
    // will be stored.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.DestinationLog.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionLogFile,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the ConfigurationMode property that specifies the mode in which events 
    // are delivered.
    vPropertyValue.Type = EcVarTypeUInt32;
    vPropertyValue.UInt32Val = sub.ConfigMode;
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionConfigurationMode,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // If the Configuration Mode is Custom, set the DeliveryMode, DeliveryMaxItems,
    // HeartbeatInterval, and DeliveryMaxLatencyTime properties.
    if ( sub.ConfigMode == EcConfigurationModeCustom)
    {
        // Set the DeliveryMode property that defines how events are delivered. 
        // Events can be delivered through either a push or pull model.
        vPropertyValue.Type = EcVarTypeUInt32;
        vPropertyValue.UInt32Val = sub.DeliveryMode;
        if (!EcSetSubscriptionProperty(hSubscription,
            EcSubscriptionDeliveryMode,
            NULL,
            &vPropertyValue))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }

        // Set the DeliveryMaxItems property that specifies the maximum number of 
        // events that can be batched when forwarded from the event sources.
        vPropertyValue.Type = EcVarTypeUInt32;
        vPropertyValue.UInt32Val = sub.MaxItems;
        if (!EcSetSubscriptionProperty(hSubscription,
            EcSubscriptionDeliveryMaxItems,
            NULL,
            &vPropertyValue))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }

        // Set the HeartbeatInterval property that defines the time interval, in 
        // seconds, that is observed between the heartbeat messages.
        vPropertyValue.Type = EcVarTypeUInt32;
        vPropertyValue.UInt32Val = sub.HeartbeatInerval;
        if (!EcSetSubscriptionProperty(hSubscription,
            EcSubscriptionHeartbeatInterval,
            NULL,
            &vPropertyValue))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }

        // Set the DeliveryMaxLatencyTime property that specifies how long, in 
        // seconds, the event source should wait before forwarding events.
        vPropertyValue.Type = EcVarTypeUInt32;
        vPropertyValue.UInt32Val = sub.MaxLatencyTime;
        if (!EcSetSubscriptionProperty(hSubscription,
            EcSubscriptionDeliveryMaxLatencyTime,
            NULL,
            &vPropertyValue))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }
    }

    // Set the ContentFormat property that specifies the format for the event content.
    vPropertyValue.Type = EcVarTypeUInt32;
    vPropertyValue.UInt32Val = sub.ContentFormat;
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionContentFormat,
        0,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the ReadExistingEvents property that is used to enable or disable whether
    // existing events are forwarded.
    vPropertyValue.Type = EcVarTypeBoolean;
    vPropertyValue.BooleanVal = sub.ReadExistingEvents;
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionReadExistingEvents,
        0,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the Enabled property that is used to enable or disable the subscription
    // or to obtain the current status of a subscription.
    vPropertyValue.Type = EcVarTypeBoolean;
    vPropertyValue.BooleanVal = sub.SubscriptionStatus;
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionEnabled,
        0,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the TransportName property that determines the type of 
    // transport used by the subscription.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.TransportName.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionTransportName,
        0,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Required:
    // Set the AllowedSourceDomainComputers property to the specified SDDL.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.AllowedSourceDomainComputers.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionAllowedSourceDomainComputers,
        0,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    //----------------------------------------------
    // Step 3: Save the subscription.
    // Save the subscription with the associated properties
    // This will create the subscription and store it in the 
    // subscription repository 
    if( !EcSaveSubscription(hSubscription, NULL) )
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 4: Close the subscription.
Cleanup:
    if(hSubscription)
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
            L" Error Message: %s\n", dwRetVal, lpwszBuffer);

        LocalFree(lpwszBuffer);
    }
}

DWORD GetProperty(EC_HANDLE hSubscription, 
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
        &dwBufferSize) )
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
```



<span data-ttu-id="60053-118">**Validar se a assinatura funciona corretamente**</span><span class="sxs-lookup"><span data-stu-id="60053-118">**Validate that the subscription works correctly**</span></span>

1.  <span data-ttu-id="60053-119">No computador do coletor de eventos, conclua o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="60053-119">On the event collector computer complete the following procedure:</span></span>

    1.  <span data-ttu-id="60053-120">Execute o comando a seguir em um prompt de comando de privilégio elevado para obter o status de tempo de execução da assinatura:</span><span class="sxs-lookup"><span data-stu-id="60053-120">Run the following command from an elevated privilege command prompt to get the runtime status of the subscription:</span></span>

        <span data-ttu-id="60053-121">\**wecutil gr\*\*\*<subscriptionID>*</span><span class="sxs-lookup"><span data-stu-id="60053-121">**wecutil gr** *<subscriptionID>*</span></span>

    2.  <span data-ttu-id="60053-122">Verifique se a origem do evento está conectada.</span><span class="sxs-lookup"><span data-stu-id="60053-122">Verify that the event source has connected.</span></span> <span data-ttu-id="60053-123">Talvez seja necessário aguardar até que o intervalo de atualização especificado na política fique acima depois que você criar a assinatura para a origem do evento ser conectada.</span><span class="sxs-lookup"><span data-stu-id="60053-123">You might need to wait until the refresh interval specified in the policy is over after you create the subscription for the event source to be connected.</span></span>
    3.  <span data-ttu-id="60053-124">Execute o seguinte comando para obter as informações de assinatura:</span><span class="sxs-lookup"><span data-stu-id="60053-124">Run the following command to get the subscription information:</span></span>

        <span data-ttu-id="60053-125">\**wecutil GS\*\*\*<subscriptionID>*</span><span class="sxs-lookup"><span data-stu-id="60053-125">**wecutil gs** *<subscriptionID>*</span></span>

    4.  <span data-ttu-id="60053-126">Obtenha o valor de DeliveryMaxItems das informações de assinatura.</span><span class="sxs-lookup"><span data-stu-id="60053-126">Get the DeliveryMaxItems value from the subscription information.</span></span>

2.  <span data-ttu-id="60053-127">No computador de origem do evento, gere os eventos que correspondem à consulta da assinatura do evento.</span><span class="sxs-lookup"><span data-stu-id="60053-127">On the event source computer, raise the events that match the query from the event subscription.</span></span> <span data-ttu-id="60053-128">O número DeliveryMaxItems de eventos deve ser gerado para que os eventos sejam encaminhados.</span><span class="sxs-lookup"><span data-stu-id="60053-128">The DeliveryMaxItems number of events must be raised for the events to be forwarded.</span></span>
3.  <span data-ttu-id="60053-129">No computador do coletor de eventos, valide se os eventos foram encaminhados para o log ForwardedEvents ou para o log especificado na assinatura.</span><span class="sxs-lookup"><span data-stu-id="60053-129">On the event collector computer, validate that the events have been forwarded to the ForwardedEvents log or to the log specified in the subscription.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60053-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="60053-130">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="60053-131">[Configurar computadores para encaminhar e coletar eventos](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="60053-131">[Configure Computers to Forward and Collect Events](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11))</span></span>
</dt> <dt>

[<span data-ttu-id="60053-132">Configurando uma assinatura iniciada pela origem</span><span class="sxs-lookup"><span data-stu-id="60053-132">Setting up a Source Initiated Subscription</span></span>](setting-up-a-source-initiated-subscription.md)
</dt> <dt>

[<span data-ttu-id="60053-133">Referência do coletor de eventos do Windows</span><span class="sxs-lookup"><span data-stu-id="60053-133">Windows Event Collector Reference</span></span>](windows-event-collector-reference.md)
</dt> </dl>

 

 