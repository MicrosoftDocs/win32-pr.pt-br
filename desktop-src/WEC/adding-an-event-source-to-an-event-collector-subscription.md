---
title: Adicionando uma origem do evento a uma assinatura iniciada pelo coletor
description: Para receber um evento encaminhado de uma assinatura de evento, você pode criar uma assinatura iniciada pelo coletor no computador local.
ms.assetid: f0100938-1702-4ef7-b20e-a0e8df224d18
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 905dd9b5a250f9ab12397f851f79a8374c6847235acb34013972dea445f3622b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344207"
---
# <a name="adding-an-event-source-to-a-collector-initiated-subscription"></a>Adicionando uma origem do evento a uma assinatura iniciada pelo coletor

Para receber um evento encaminhado de uma assinatura de evento, você pode criar uma assinatura iniciada pelo coletor no computador local. Para obter mais informações sobre como criar uma assinatura iniciada pelo coletor, consulte o exemplo de código C++ mostrado em [criando uma assinatura do coletor de eventos](creating-an-event-collector-subscription.md).

Depois que uma assinatura iniciada pelo coletor tiver sido criada, você poderá adicionar origens do evento à assinatura. Você deve adicionar pelo menos uma origem de evento a uma assinatura para coletar eventos.

> [!Note]
>
> Você pode usar este exemplo de código para adicionar uma origem de evento a uma assinatura ou pode digitar o seguinte comando no prompt de comando:
>
> **wecutil SS** *subscriptionname* **/ESA:**_EventSourceAddress_ **/AES/ESE**
>
> *EventSourceAddress* pode ser localhost para o computador local ou um nome de domínio totalmente qualificado para um computador remoto.

 

Para obter mais informações sobre como adicionar fontes de eventos a uma assinatura de origem iniciada, consulte [Configurando uma assinatura iniciada por origem](setting-up-a-source-initiated-subscription.md).

Este exemplo segue uma série de etapas para adicionar uma origem de evento a uma assinatura iniciada pelo coletor.

**Para adicionar uma origem do evento a uma assinatura iniciada pelo coletor**

1.  Abra a assinatura existente fornecendo o nome da assinatura e os direitos de acesso como parâmetros para a função [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) . para obter mais informações sobre direitos de acesso, consulte [**Windows constantes do coletor de eventos**](windows-event-collector-constants.md).
2.  Obtenha a matriz de fontes de eventos da assinatura chamando a função [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) . Para obter mais informações sobre as propriedades de assinatura que podem ser recuperadas, consulte a enumeração de [**ID de propriedade da assinatura do EC \_ \_ \_**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) .
3.  Adicione uma nova origem de evento à matriz de origens de eventos da assinatura chamando a função [**EcInsertObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecinsertobjectarrayelement) .
4.  Defina as propriedades de origem do evento chamando a função [**EcSetObjectArrayProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetobjectarrayproperty) . A propriedade **EcSubscriptionEventSourceAddress** é definida como um endereço para o computador local (localhost) ou para um nome de domínio totalmente qualificado para um computador remoto. Para obter mais informações sobre as propriedades de origem do evento que podem ser definidas, consulte a enumeração da **ID de propriedade da assinatura do EC \_ \_ \_** .
5.  Salve a assinatura chamando a função [**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) .
6.  Feche a assinatura chamando a função [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) .

O exemplo de código C++ a seguir mostra como adicionar uma origem do evento a uma assinatura iniciada pelo coletor:


```C++
#include <windows.h>
#include <iostream>
using namespace std;
#include <EvColl.h>
#include <vector>
#include <string>
#include <strsafe.h>

#pragma comment(lib, "wecapi.lib")

DWORD GetProperty(EC_HANDLE hSubscription,  
                  EC_SUBSCRIPTION_PROPERTY_ID propID, 
                  DWORD flags, 
                  std::vector<BYTE>& buffer, 
                  PEC_VARIANT& vProperty);

void __cdecl wmain()
{
    EC_HANDLE hSubscription;
    std::wstring eventSource = L"localhost"; 
    BOOL status = true;
    std::wstring eventSourceUserName;
    std::wstring eventSourcePassword;
    LPCWSTR lpSubname = L"TestSubscription-CollectorInitiated";
    DWORD dwEventSourceCount;
    DWORD dwRetVal = ERROR_SUCCESS;
    PEC_VARIANT vEventSource = NULL;
    std::vector<BYTE> buffer;
    LPVOID lpwszBuffer;
    EC_VARIANT vProperty;

    // Create a handle to access the event sources array.
    EC_OBJECT_ARRAY_PROPERTY_HANDLE hArray = NULL;

    // Step 1: Open an existing subscription.
    hSubscription = EcOpenSubscription( lpSubname,
        EC_READ_ACCESS | EC_WRITE_ACCESS, 
        EC_OPEN_EXISTING);
    if (!hSubscription)
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 2: Get the event sources array to add a new event 
    // source to the subscription.
    dwRetVal = GetProperty(hSubscription, 
        EcSubscriptionEventSources,
        0,
        buffer,
        vEventSource);
    if (ERROR_SUCCESS != dwRetVal)
    {
        goto Cleanup;
    }

    // Ensure that a handle to the event sources array has been obtained. 
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

    // Step 4: Set the properties of the event source
    // Set the EventSourceAddress property that specifies the address
    // of the event forwarding computer, this property can be localhost 
    // or a fully-qualified domain name.
    vProperty.Type = EcVarTypeString;
    vProperty.StringVal = eventSource.c_str();
    if (!EcSetObjectArrayProperty( hArray,
        EcSubscriptionEventSourceAddress,
        dwEventSourceCount,
        0,
        &vProperty))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Get the credentials.
    wcout << "Enter credentials used to connect to the event source " <<
        eventSource << ". " << endl <<
        "Enter user name: " << endl;
    wcin >> eventSourceUserName;
    cout << "Enter password: " << endl;

    wchar_t c;
    while( (c = _getwch()) && c != '\n' && c != '\r' && eventSourcePassword.length() < 512)
    {eventSourcePassword.append(1, c);}

    // Set the EventSourceUserName property that specifies the user
    // that can retrieve events from the event source.
    if (eventSourceUserName.length() > 0)
    {
        vProperty.Type = EcVarTypeString;
        vProperty.StringVal = eventSourceUserName.c_str();
        if (!EcSetObjectArrayProperty(hArray,
            EcSubscriptionEventSourceUserName,
            dwEventSourceCount,
            0,
            &vProperty))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }

        // Set the EventSourcePassword property that defines the password
        // for the previously-defined user.
        vProperty.StringVal = (eventSourcePassword.length() > 0) ? 
            eventSourcePassword.c_str() : L"";
        if (!EcSetObjectArrayProperty(hArray,
            EcSubscriptionEventSourcePassword, 
            dwEventSourceCount,
            0,
            &vProperty))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }
    }

    // When you have finished using the credentials,
    // erase them.
    eventSourceUserName.erase();
    eventSourcePassword.erase();


    // Set the EventSourceEnabled property that enables the event source
    // to forward events.
    vProperty.Type = EcVarTypeBoolean;
    vProperty.BooleanVal = status;
    if (!EcSetObjectArrayProperty(hArray,
        EcSubscriptionEventSourceEnabled,
        dwEventSourceCount,
        0,
        &vProperty))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 5: Save the subscription to enable the event source.
    if (!EcSaveSubscription(hSubscription, NULL))
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
            wprintf(L"Failed to FormatMessage.  Operation Error Code: %u\n  Error Code from FormatMessage: %u\n", dwRetVal, GetLastError());
            return;
        }
        wprintf(L"\nFailed to Perform Operation. Error Code: %u\n Error Message: %s\n", dwRetVal, lpwszBuffer);
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
                &dwBufferSize) )
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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurar computadores para encaminhar e coletar eventos](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11))
</dt> <dt>

[Criando uma assinatura do coletor de eventos](creating-an-event-collector-subscription.md)
</dt> <dt>

[Windows Referência do coletor de eventos](windows-event-collector-reference.md)
</dt> </dl>

 

 