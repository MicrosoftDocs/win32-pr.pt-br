---
description: As funções de protótipo do manipulador de eventos são usadas para todas as funções que manipulam eventos de notificação do Winlogon.
ms.assetid: 99b91e80-5e4e-4119-89aa-c0a80fce69e3
title: Função de manipulador de eventos funções de retorno de chamada do protótipo
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
ms.openlocfilehash: 935ddac5660c814b898be17218d879678f2135ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750579"
---
# <a name="event-handler-function-prototype-callback-function"></a>Função de manipulador de eventos funções de retorno de chamada do protótipo

\[As funções de protótipo do manipulador de eventos não estão mais disponíveis para uso a partir do Windows Server 2008 e do Windows Vista. \]

As funções de protótipo do manipulador de eventos são usadas para todas as funções que manipulam eventos de notificação do [*Winlogon*](/windows/desktop/SecGloss/w-gly) . O nome da função, representado abaixo do nome da função do *\_ manipulador de \_ \_ eventos* do espaço reservado, normalmente reflete o nome do evento manipulado pela função. Por exemplo, a função que manipula eventos de logon pode ser nomeada: **WLEventLogon**.

## <a name="syntax"></a>Sintaxe


```C++
void Event_Handler_Function_Name(
  _In_ PWLX_NOTIFICATION_INFO pInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pInfo* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ \_ informações de notificação do WLX**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) que contém os detalhes do evento.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função de retorno de chamada não retorna um valor.

## <a name="remarks"></a>Comentários

Se o seu manipulador de eventos precisar criar processos filho, ele deverá chamar a função [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) . Caso contrário, o novo processo será criado na área de trabalho do Winlogon, não na área de trabalho do usuário.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como implementar manipuladores de eventos para eventos do Winlogon. Para simplificar, somente as implementações dos manipuladores de eventos de logon e logoff são mostradas. Você pode implementar manipuladores para o restante dos eventos exatamente da mesma maneira.


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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                       |



 

