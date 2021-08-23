---
description: As funções de Protótipo do Manipulador de Eventos são usadas para todas as funções que lidam com eventos de notificação do Winlogon.
ms.assetid: 99b91e80-5e4e-4119-89aa-c0a80fce69e3
title: Função de retorno de chamada Protótipo de Função do Manipulador de Eventos
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event_Handler_Function_Name
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: df6670e852ccd12fd2bed1d0c188aa0252c9b3afbcb899cf9480b7011d08625d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008224"
---
# <a name="event-handler-function-prototype-callback-function"></a>Função de retorno de chamada Protótipo de Função do Manipulador de Eventos

\[As funções de Protótipo do Manipulador de Eventos não estão mais disponíveis para uso Windows Server 2008 e Windows Vista. \]

As funções de Protótipo do Manipulador de Eventos são usadas para todas as funções que lidam com [*eventos de notificação do Winlogon.*](/windows/desktop/SecGloss/w-gly) O nome da função, representado abaixo pelo nome da função do manipulador de eventos do espaço reservado, normalmente reflete o nome do evento que a função trata. *\_ \_ \_* Por exemplo, a função que lida com eventos de logon pode ser nomeada: **WLEventLogon**.

## <a name="syntax"></a>Sintaxe


```C++
void Event_Handler_Function_Name(
  _In_ PWLX_NOTIFICATION_INFO pInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pInfo* \[ Em\]
</dt> <dd>

Um ponteiro para uma estrutura [**WLX \_ NOTIFICATION \_ INFO**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) que contém os detalhes do evento.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa função de retorno de chamada não retorna um valor.

## <a name="remarks"></a>Comentários

Se o manipulador de eventos precisar criar processos filho, ele deverá chamar a [**função CreateProcessAsUser.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) Caso contrário, o novo processo será criado na área de trabalho do Winlogon, não na área de trabalho do usuário.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como implementar manipuladores de eventos para eventos winlogon. Para simplificar, apenas as implementações dos manipuladores de eventos Logon e Logoff são mostradas. Você pode implementar manipuladores para o restante dos eventos exatamente da mesma maneira.


```C++
// Copyright (C) Microsoft. All rights reserved. 
#include <windows.h>

// Here is the entrance function for the DLL.
BOOL WINAPI LibMain(HINSTANCE hInstance, DWORD dwReason, LPVOID lpReserved)
{
    switch (dwReason)
    {
        case DLL_PROCESS_ATTACH:
            {

             // Disable DLL_THREAD_ATTACH & DLL_THREAD_DETACH
             // notification calls. This is a performance optimization
             // for multithreaded applications that do not need 
             // thread-level notifications of attachment or
             // detachment.

            DisableThreadLibraryCalls (hInstance);
            }
            break;
    }

    return TRUE;
}

// Here is the event handler for the Winlogon Logon event.
void WLEventLogon (PWLX_NOTIFICATION_INFO pInfo)
{

    // Print the name of the handler to debug output.
    // You can replace this with more useful functionality.
    OutputDebugString (TEXT("NOTIFY:  Entering WLEventLogon.\r\n"));
}

// Here is the event handler for the Winlogon Logoff event.
void WLEventLogoff (PWLX_NOTIFICATION_INFO pInfo)
{

    // Print the name of the handler to debug output.
    // You can replace this with more useful functionality.
    OutputDebugString (TEXT("NOTIFY:  Entering WLEventLogff.\r\n"));
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/> |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                       |



 

