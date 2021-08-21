---
description: Saiba mais sobre como escrever eventos baseados em manifesto em uma sessão de rastreamento. Comece registrando seu provedor para que ele esteja pronto para gravar eventos em uma sessão de rastreamento.
ms.assetid: 76e7202e-74ce-40a3-a04b-9af5117fe20e
title: Escrevendo eventos baseados em manifesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6963051f65beb652eda04e3d0be6db99925e4eed81032c5687850915a0f1c173
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151075"
---
# <a name="writing-manifest-based-events"></a>Escrevendo eventos baseados em manifesto

Antes de gravar eventos em uma sessão de rastreamento, você deve registrar seu provedor. Registrar um provedor informa ao ETW que seu provedor está pronto para gravar eventos em uma sessão de rastreamento. Um processo pode registrar até 1.024 GUIDs de provedor; No entanto, você deve limitar o número de provedores que seu processo registra a um ou dois.

**Antes do Windows Vista:** Não há nenhum limite para o número de provedores que um processo pode registrar.

Para registrar um provedor baseado em manifesto, chame a [**função EventRegister.**](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) A função registra o GUID do provedor e identifica um retorno de chamada opcional que o ETW chama quando um controlador habilita ou desabilita o provedor.

Antes de o provedor sair, chame [**a função EventUnregister**](/windows/desktop/api/Evntprov/nf-evntprov-eventunregister) para remover o registro do provedor do ETW. A [**função EventRegister**](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) retorna o alça de registro que você passa para a **função EventUnregister.**

[Os provedores baseados](about-event-tracing.md) em manifesto não têm que implementar uma [**função EnableCallback**](/windows/desktop/api/Evntprov/nc-evntprov-penablecallback) para receber notificações quando uma sessão habilita ou desabilita o provedor. O retorno de chamada é opcional e é usado para fins informacionais; você não precisa especificar ou implementar o retorno de chamada ao registrar o provedor. Um provedor baseado em manifesto pode simplesmente gravar eventos e o ETW decidirá se o evento é registrado em uma sessão de rastreamento. Se um evento exigir que você execute um trabalho extensivo para gerar os dados do evento, chame a função [**EventEnabled**](/windows/desktop/api/Evntprov/nf-evntprov-eventenabled) ou [**EventProviderEnabled**](/windows/desktop/api/Evntprov/nf-evntprov-eventproviderenabled) primeiro para verificar se o evento será gravado em uma sessão antes de executar o trabalho.

Normalmente, você implementará o retorno de chamada se o provedor exigir que o controlador passe dados de filtro definidos pelo provedor (consulte o parâmetro *FilterData* de [**EnableCallback**](/windows/desktop/api/Evntprov/nc-evntprov-penablecallback)) para o provedor ou o provedor usa as informações de contexto especificadas quando ele se registrou (consulte o parâmetro *CallbackContext* de [**EventRegister**](/windows/desktop/api/Evntprov/nf-evntprov-eventregister)).

[Os provedores baseados](about-event-tracing.md) em manifesto chamam a [**função EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) ou [**EventWriteString**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritestring) para gravar eventos em uma sessão. Se os dados do evento são uma cadeia de caracteres ou se você não definir um manifesto para seu provedor e seus dados de evento são uma única cadeia de caracteres, chame a [**função EventWriteString**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritestring) para gravar o evento. Para dados de evento que contêm tipos de dados numéricos ou complexos, chame a [**função EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) para registrar o evento.

O exemplo a seguir mostra como preparar os dados de evento a serem gravados usando a [**função EventWrite.**](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) O exemplo faz referência aos eventos definidos [em Publicando seu esquema de evento para um provedor baseado em manifesto.](publishing-your-event-schema-for-a-manifest-base-provider.md)


```C++
#include <windows.h>
#include <stdio.h>
#include <evntprov.h>
#include "provider.h"  // Generated from manifest

#define SUNDAY     0X1
#define MONDAY     0X2
#define TUESDAY    0X4
#define WEDNESDAY  0X8
#define THURSDAY   0X10
#define FRIDAY     0X20
#define SATURDAY   0X40

enum TRANSFER_TYPE {
  Download = 1,
  Upload,
  UploadReply
};

#define MAX_NAMEDVALUES          5  // Maximum array size
#define MAX_PAYLOAD_DESCRIPTORS  9 + (2 * MAX_NAMEDVALUES)

typedef struct _namedvalue {
  LPWSTR name;
  USHORT value;
} NAMEDVALUE, *PNAMEDVALUE;

void wmain(void)
{
    DWORD status = ERROR_SUCCESS;
    REGHANDLE RegistrationHandle = NULL; 
    EVENT_DATA_DESCRIPTOR Descriptors[MAX_PAYLOAD_DESCRIPTORS]; 
    DWORD i = 0;

    // Data to load into event descriptors

    USHORT Scores[3] = {45, 63, 21};
    ULONG pImage = (ULONG)&Scores;
    DWORD TransferType = Upload;
    DWORD Day = MONDAY | TUESDAY;
    LPWSTR Path = L"c:\\path\\folder\\file.ext";
    BYTE Cert[11] = {0x2, 0x4, 0x8, 0x10, 0x20, 0x30, 0x40, 0x50, 0x60, 0x0, 0x1};
    PBYTE Guid = (PBYTE) &ProviderGuid;
    USHORT ArraySize = MAX_NAMEDVALUES;
    BOOL IsLocal = TRUE;
    NAMEDVALUE NamedValues[MAX_NAMEDVALUES] = { 
        {L"Bill", 1},
        {L"Bob", 2},
        {L"William", 3},
        {L"Robert", 4},
        {L"", 5}
        };

    status = EventRegister(
        &ProviderGuid,      // GUID that identifies the provider
        NULL,               // Callback not used
        NULL,               // Context noot used
        &RegistrationHandle // Used when calling EventWrite and EventUnregister
        );

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"EventRegister failed with %lu\n", status);
        goto cleanup;
    }
  
    // Load the array of data descriptors for the TransferEvent event. 
    // Add the data to the array in the order of the <data> elements
    // defined in the event's template. 
   
    EventDataDescCreate(&Descriptors[i++], &pImage, sizeof(ULONG));
    EventDataDescCreate(&Descriptors[i++], Scores, sizeof(Scores));
    EventDataDescCreate(&Descriptors[i++], Guid, sizeof(GUID));
    EventDataDescCreate(&Descriptors[i++], Cert, sizeof(Cert));
    EventDataDescCreate(&Descriptors[i++], &IsLocal, sizeof(BOOL));
    EventDataDescCreate(&Descriptors[i++], Path, (ULONG)(wcslen(Path) + 1) * sizeof(WCHAR));
    EventDataDescCreate(&Descriptors[i++], &ArraySize, sizeof(USHORT));

    // If your event contains a structure, you should write each member
    // of the structure separately. If the structure contained integral data types
    // such as DWORDs and the data types were aligned on an 8-byte boundary, you 
    // could use the following call to write the structure, however, you are 
    // encouraged to write the members separately.
    //
    // EventDataDescCreate(&EvtData, struct, sizeof(struct));
    //
    // Because the array of structures in this example contains both strings 
    // and numbers, you must write each member of the structure separately.

    for (int j = 0; j < MAX_NAMEDVALUES; j++)
    {
        EventDataDescCreate(&Descriptors[i++], NamedValues[j].name, (ULONG)(wcslen(NamedValues[j].name)+1) * sizeof(WCHAR) );
        EventDataDescCreate(&Descriptors[i++], &(NamedValues[j].value), sizeof(USHORT) );
    }

    EventDataDescCreate(&Descriptors[i++], &Day, sizeof(DWORD));
    EventDataDescCreate(&Descriptors[i++], &TransferType, sizeof(DWORD));

    // Write the event. You do not have to verify if your provider is enabled before
    // writing the event. ETW will write the event to any session that enabled
    // the provider. If no session enabled the provider, the event is not 
    // written. If you need to perform extra work to write an event that you
    // would not otherwise do, you may want to call the EventEnabled function
    // before performing the extra work. The EventEnabled function tells you if a
    // session has enabled your provider, so you know if you need to perform the 
    // extra work or not.

    status = EventWrite(
        RegistrationHandle,              // From EventRegister
        &TransferEvent,                  // EVENT_DESCRIPTOR generated from the manifest
        (ULONG)MAX_PAYLOAD_DESCRIPTORS,  // Size of the array of EVENT_DATA_DESCRIPTORs
        &Descriptors[0]                  // Array of descriptors that contain the event data
        );

    if (status != ERROR_SUCCESS) 
    {
        wprintf(L"EventWrite failed with 0x%x", status);
    }

cleanup:

    EventUnregister(RegistrationHandle);
}
```



Quando você compila o manifesto (consulte Compilando um manifesto de [instrumentação](../wes/compiling-an-instrumentation-manifest.md)) que o exemplo acima usa, ele cria o seguinte arquivo de header (referenciado no exemplo acima).


```C++
//**********************************************************************`
//* This is an include file generated by Message Compiler.             *`
//*                                                                    *`
//* Copyright (c) Microsoft Corporation. All Rights Reserved.          *`
//**********************************************************************`
#pragma once
//+
// Provider Microsoft-Windows-ETWProvider Event Count 1
//+
EXTERN_C __declspec(selectany) const GUID ProviderGuid = {0xd8909c24, 0x5be9, 0x4502, {0x98, 0xca, 0xab, 0x7b, 0xdc, 0x24, 0x89, 0x9d}};
//
// Keyword
//
#define READ_KEYWORD 0x1
#define WRITE_KEYWORD 0x2
#define LOCAL_KEYWORD 0x4
#define REMOTE_KEYWORD 0x8

//
// Event Descriptors
//
EXTERN_C __declspec(selectany) const EVENT_DESCRIPTOR TransferEvent = {0x1, 0x0, 0x0, 0x4, 0x0, 0x0, 0x5};
#define TransferEvent_value 0x1
#define MSG_Provider_Name                    0x90000001L
#define MSG_Event_WhenToTransfer             0xB0000001L
#define MSG_Map_Download                     0xD0000001L
#define MSG_Map_Upload                       0xD0000002L
#define MSG_Map_UploadReply                  0xD0000003L
#define MSG_Map_Sunday                       0xF0000001L
#define MSG_Map_Monday                       0xF0000002L
#define MSG_Map_Tuesday                      0xF0000003L
#define MSG_Map_Wednesday                    0xF0000004L
#define MSG_Map_Thursday                     0xF0000005L
#define MSG_Map_Friday                       0xF0000006L
#define MSG_Map_Saturday                     0xF0000007L
```



 

 
