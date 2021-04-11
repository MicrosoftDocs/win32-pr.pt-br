---
title: Criando uma assinatura iniciada pelo coletor
description: Você pode assinar para receber eventos em um computador local (o coletor de eventos) que são encaminhados de computadores remotos (as origens do evento) usando uma assinatura iniciada pelo coletor.
ms.assetid: 76f14e01-7a84-4c94-aea6-91189573eb89
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1359033b61d419f1147ca930f30d924b8429e31
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162362"
---
# <a name="creating-a-collector-initiated-subscription"></a><span data-ttu-id="abf07-103">Criando uma assinatura iniciada pelo coletor</span><span class="sxs-lookup"><span data-stu-id="abf07-103">Creating a Collector Initiated Subscription</span></span>

<span data-ttu-id="abf07-104">Você pode assinar para receber eventos em um computador local (o coletor de eventos) que são encaminhados de computadores remotos (as origens do evento) usando uma assinatura iniciada pelo coletor.</span><span class="sxs-lookup"><span data-stu-id="abf07-104">You can subscribe to receive events on a local computer (the event collector) that are forwarded from remote computers (the event sources) by using a collector-initiated subscription.</span></span> <span data-ttu-id="abf07-105">Em uma assinatura iniciada pelo coletor, a assinatura deve conter uma lista de todas as origens do evento.</span><span class="sxs-lookup"><span data-stu-id="abf07-105">In a collector-initiated subscription, the subscription must contain a list of all the event sources.</span></span> <span data-ttu-id="abf07-106">Antes que um computador coletor possa assinar eventos e uma fonte de evento remoto possa encaminhar eventos, ambos os computadores devem ser configurados para coleta e encaminhamento de eventos.</span><span class="sxs-lookup"><span data-stu-id="abf07-106">Before a collector computer can subscribe to events and a remote event source can forward events, both computers must be configured for event collecting and forwarding.</span></span> <span data-ttu-id="abf07-107">Para obter mais informações sobre como configurar os computadores, consulte [configurar computadores para encaminhar e coletar eventos](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="abf07-107">For more information about how to configure the computers, see [Configure Computers to Forward and Collect Events](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11)).</span></span>

<span data-ttu-id="abf07-108">O exemplo de código a seguir segue uma série de etapas para criar uma assinatura iniciada pelo coletor:</span><span class="sxs-lookup"><span data-stu-id="abf07-108">The following code example follows a series of steps to create a collector initiated subscription:</span></span>

<span data-ttu-id="abf07-109">**Para criar uma assinatura iniciada pelo coletor**</span><span class="sxs-lookup"><span data-stu-id="abf07-109">**To create a collector initiated subscription**</span></span>

1.  <span data-ttu-id="abf07-110">Abra a assinatura fornecendo o nome da assinatura e os direitos de acesso como parâmetros para a função [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) .</span><span class="sxs-lookup"><span data-stu-id="abf07-110">Open the subscription by providing the subscription name and access rights as parameters to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function.</span></span> <span data-ttu-id="abf07-111">Para obter mais informações sobre direitos de acesso, consulte as [**constantes do coletor de eventos do Windows**](windows-event-collector-constants.md).</span><span class="sxs-lookup"><span data-stu-id="abf07-111">For more information about access rights, see [**Windows Event Collector Constants**](windows-event-collector-constants.md).</span></span>
2.  <span data-ttu-id="abf07-112">Defina as propriedades da assinatura chamando a função [**EcSetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetsubscriptionproperty) .</span><span class="sxs-lookup"><span data-stu-id="abf07-112">Set the properties of the subscription by calling the [**EcSetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetsubscriptionproperty) function.</span></span> <span data-ttu-id="abf07-113">Para obter mais informações sobre as propriedades de assinatura que podem ser definidas, consulte a enumeração de [**ID de propriedade da assinatura do EC \_ \_ \_**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) .</span><span class="sxs-lookup"><span data-stu-id="abf07-113">For more information about subscription properties that can be set, see the [**EC\_SUBSCRIPTION\_PROPERTY\_ID**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) enumeration.</span></span>
3.  <span data-ttu-id="abf07-114">Salve a assinatura chamando a função [**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) .</span><span class="sxs-lookup"><span data-stu-id="abf07-114">Save the subscription by calling the [**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) function.</span></span>
4.  <span data-ttu-id="abf07-115">Feche a assinatura chamando a função [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) .</span><span class="sxs-lookup"><span data-stu-id="abf07-115">Close the subscription by calling the [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) function.</span></span>

<span data-ttu-id="abf07-116">Para obter mais informações sobre como adicionar uma origem do evento, consulte [adicionando uma origem do evento a uma assinatura do coletor de eventos](adding-an-event-source-to-an-event-collector-subscription.md).</span><span class="sxs-lookup"><span data-stu-id="abf07-116">For more information about adding an event source, see [Adding an Event Source to an Event Collector Subscription](adding-an-event-source-to-an-event-collector-subscription.md).</span></span>

<span data-ttu-id="abf07-117">O exemplo de código C++ a seguir mostra como criar uma assinatura iniciada pelo coletor:</span><span class="sxs-lookup"><span data-stu-id="abf07-117">The following C++ code example shows how to create a collector-initiated subscription:</span></span>


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
typedef struct _SUBSCRIPTION_COLLECTOR_INITIATED
{
    std::wstring Name;
    std::wstring Description;
    std::wstring URI;
    std::wstring Query;
    std::wstring DestinationLog;
    std::wstring Password;
    std::wstring UserName;
    EC_SUBSCRIPTION_CONFIGURATION_MODE ConfigMode;
    EC_SUBSCRIPTION_DELIVERY_MODE DeliveryMode;
    EC_SUBSCRIPTION_TYPE SubscriptionType;
    DWORD MaxItems;
    DWORD MaxLatencyTime;
    DWORD HeartbeatInerval;
    EC_SUBSCRIPTION_CONTENT_FORMAT ContentFormat;
    EC_SUBSCRIPTION_CREDENTIALS_TYPE CredentialsType;
    BOOL SubscriptionStatus;
} SUBSCRIPTION_COLLECTOR_INITIATED;

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
    EC_HANDLE hSubscription = 0;
    EC_VARIANT vPropertyValue;
    std::vector<BYTE> buffer;
    PEC_VARIANT vProperty = NULL;
    SUBSCRIPTION_COLLECTOR_INITIATED sub;

    sub.Name = L"TestSubscription-CollectorInitiated";
    sub.Description = L"A subscription that collects events that are published in\n" \
        L"the Microsoft-Windows-TaskScheduler/Operational log and forwards them\n" \
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
    sub.MaxLatencyTime = 10000;
    sub.HeartbeatInerval = 10000;
    sub.DeliveryMode = EcDeliveryModePull;
    sub.ContentFormat = EcContentFormatRenderedText;
    sub.CredentialsType = EcSubscriptionCredDefault;
    sub.SubscriptionStatus = true;
    sub.SubscriptionType = EcSubscriptionTypeCollectorInitiated;

    std::wstring eventSource = L"localhost"; 
    BOOL status = true;
    PEC_VARIANT vEventSource = NULL;
    DWORD dwEventSourceCount;
    EC_VARIANT vSourceProperty;

    // Create a handle to access the event sources array.
    EC_OBJECT_ARRAY_PROPERTY_HANDLE hArray = NULL;

    // The subscription name, URI, and query string must be defined to create 
    // the subscription.
    if ( sub.Name.empty() || sub.URI.empty() || sub.Query.empty() )
    {
        dwRetVal = ERROR_INVALID_PARAMETER;
        goto Cleanup;
    }

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

    // Set the CredentialsType property that specifies the type of credentials 
    // used in the event subscription.
    vPropertyValue.Type = EcVarTypeUInt32;
    vPropertyValue.UInt32Val = sub.CredentialsType;
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionCredentialsType,
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

    // Get the user name and password used to connect to the event sources    
    wcout << "Enter credentials used to connect to the event sources. " << endl <<
        "Enter user name: " << endl;
    wcin >> sub.UserName;
    cout << "Enter password: " << endl;

    wchar_t c;
    while( (c = _getwch()) && c != '\n' && c != '\r' && sub.Password.length() < 512)
    {sub.Password.append(1, c);}

    // Set the CommonUserName property that is used by the local and remote 
    // computers to authenticate the user with the source of the events. This 
    // property is used across all the event sources available for this subscription.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.UserName.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionCommonUserName,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the CommonPassword property that is used by the local and remote 
    // computers to authenticate the user with the source of the events.
    // Use Credential Manager Functions to handle Password information.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.Password.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionCommonPassword,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }    

    //  When you have finished using the credentials,
    //  erase them from memory.
    sub.UserName.erase();
    sub.Password.erase();


    //----------------------------------------------
    // Add event sources.
    // Ensure that a handle to the event sources array has been obtained.

    //Initialize the Event Sources Array
    dwRetVal = GetProperty( hSubscription, 
        EcSubscriptionEventSources, 
        0, 
        buffer, 
        vEventSource);

    if (vEventSource->Type != EcVarTypeNull  && 
        vEventSource->Type != EcVarObjectArrayPropertyHandle)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }

    hArray = (vEventSource->Type == EcVarTypeNull)? NULL: 
        vEventSource->PropertyHandleVal;
    if(!hArray)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }
    if (!EcGetObjectArraySize(hArray, &dwEventSourceCount))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 3: Add a new event source to the event source array.
    if (!EcInsertObjectArrayElement(hArray,
        dwEventSourceCount))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the properties of the event source
    // Set the EventSourceAddress property that specifies the address
    // of the event forwarding computer, this property can be localhost 
    // or a fully-qualified domain name.
    vSourceProperty.Type = EcVarTypeString;
    vSourceProperty.StringVal = eventSource.c_str();
    if (!EcSetObjectArrayProperty( hArray,
        EcSubscriptionEventSourceAddress,
        dwEventSourceCount,
        0,
        &vSourceProperty))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }    

    // Set the EventSourceEnabled property that enables the event source
    // to forward events.
    vSourceProperty.Type = EcVarTypeBoolean;
    vSourceProperty.BooleanVal = status;
    if (!EcSetObjectArrayProperty(hArray,
        EcSubscriptionEventSourceEnabled,
        dwEventSourceCount,
        0,
        &vSourceProperty))
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
    if(hArray)
        EcClose(hArray);

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



<span data-ttu-id="abf07-118">**Validar se a assinatura funciona corretamente**</span><span class="sxs-lookup"><span data-stu-id="abf07-118">**Validate that the subscription works correctly**</span></span>

1.  <span data-ttu-id="abf07-119">No computador do coletor de eventos, conclua o seguinte procedimento:</span><span class="sxs-lookup"><span data-stu-id="abf07-119">On the event collector computer complete the following procedure:</span></span>

    1.  <span data-ttu-id="abf07-120">Execute o comando a seguir em um prompt de comando de privilégio elevado para obter o status de tempo de execução da assinatura:</span><span class="sxs-lookup"><span data-stu-id="abf07-120">Run the following command from an elevated privilege command prompt to get the runtime status of the subscription:</span></span>

        <span data-ttu-id="abf07-121">\**wecutil gr\*\*\*<subscriptionID>*</span><span class="sxs-lookup"><span data-stu-id="abf07-121">**wecutil gr** *<subscriptionID>*</span></span>

    2.  <span data-ttu-id="abf07-122">Verifique se a origem do evento está conectada.</span><span class="sxs-lookup"><span data-stu-id="abf07-122">Verify that the event source has connected.</span></span> <span data-ttu-id="abf07-123">Talvez seja necessário aguardar até que o intervalo de atualização especificado na política fique acima depois que você criar a assinatura para a origem do evento ser conectada.</span><span class="sxs-lookup"><span data-stu-id="abf07-123">You might need to wait until the refresh interval specified in the policy is over after you create the subscription for the event source to be connected.</span></span>
    3.  <span data-ttu-id="abf07-124">Execute o seguinte comando para obter as informações de assinatura:</span><span class="sxs-lookup"><span data-stu-id="abf07-124">Run the following command to get the subscription information:</span></span>

        <span data-ttu-id="abf07-125">\**wecutil GS\*\*\*<subscriptionID>*</span><span class="sxs-lookup"><span data-stu-id="abf07-125">**wecutil gs** *<subscriptionID>*</span></span>

    4.  <span data-ttu-id="abf07-126">Obtenha o valor de DeliveryMaxItems das informações de assinatura.</span><span class="sxs-lookup"><span data-stu-id="abf07-126">Get the DeliveryMaxItems value from the subscription information.</span></span>

2.  <span data-ttu-id="abf07-127">No computador de origem do evento, gere os eventos que correspondem à consulta da assinatura do evento.</span><span class="sxs-lookup"><span data-stu-id="abf07-127">On the event source computer, raise the events that match the query from the event subscription.</span></span> <span data-ttu-id="abf07-128">O número DeliveryMaxItems de eventos deve ser gerado para que os eventos sejam encaminhados.</span><span class="sxs-lookup"><span data-stu-id="abf07-128">The DeliveryMaxItems number of events must be raised for the events to be forwarded.</span></span>
3.  <span data-ttu-id="abf07-129">No computador do coletor de eventos, valide se os eventos foram encaminhados para o log ForwardedEvents ou para o log especificado na assinatura.</span><span class="sxs-lookup"><span data-stu-id="abf07-129">On the event collector computer, validate that the events have been forwarded to the ForwardedEvents log or to the log specified in the subscription.</span></span>

## <a name="related-topics"></a><span data-ttu-id="abf07-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="abf07-130">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="abf07-131">[Configurar computadores para encaminhar e coletar eventos](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="abf07-131">[Configure Computers to Forward and Collect Events](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11))</span></span>
</dt> <dt>

[<span data-ttu-id="abf07-132">Adicionando uma origem do evento a uma assinatura do coletor de eventos</span><span class="sxs-lookup"><span data-stu-id="abf07-132">Adding an Event Source to an Event Collector Subscription</span></span>](adding-an-event-source-to-an-event-collector-subscription.md)
</dt> <dt>

[<span data-ttu-id="abf07-133">Referência do coletor de eventos do Windows</span><span class="sxs-lookup"><span data-stu-id="abf07-133">Windows Event Collector Reference</span></span>](windows-event-collector-reference.md)
</dt> </dl>

 

 