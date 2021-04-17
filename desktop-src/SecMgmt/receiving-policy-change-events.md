---
description: O LSA fornece funções que você pode usar para receber notificações quando há uma alteração na política no sistema local.
ms.assetid: 29c693f5-db2b-4fda-847c-4e5220eadfd3
title: Recebendo eventos de alteração de política
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33145974ce712f21b338ba35f1571c8f3046c42c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779937"
---
# <a name="receiving-policy-change-events"></a>Recebendo eventos de alteração de política

O LSA fornece funções que você pode usar para receber notificações quando há uma alteração na política no sistema local.

Para receber a notificação, crie um novo objeto de evento chamando a função [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) e, em seguida, chame a função [**LsaRegisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification) . Em seguida, seu aplicativo pode chamar uma função de espera como [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)ou [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) para aguardar a ocorrência do evento. A função Wait retorna quando o evento ocorre ou quando o período de tempo limite expira. Normalmente, os eventos de notificação são usados em aplicativos multissegmentados, em que um thread aguarda um evento, enquanto outros threads continuam sendo processados.

Quando o aplicativo não precisa mais receber notificações, ele deve chamar [**LsaUnregisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification) e, em seguida, chamar [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) para liberar o identificador do objeto de evento.

O exemplo a seguir mostra como um aplicativo de thread único pode receber eventos de notificação quando a política de auditoria do sistema é alterada.


```C++
#include <windows.h>
#include <stdio.h>

void WaitForPolicyChanges()
{
  HANDLE hEvent;
  NTSTATUS ntsResult;
  DWORD dwResult;

  // Create an event object.
  hEvent = CreateEvent( 
    NULL,  // child processes cannot inherit 
    FALSE, // automatically reset event
    FALSE, // start as a nonsignaled event
    NULL   // do not need a name
  );

  // Check that the event was created.
  if (hEvent == NULL) 
  {
    wprintf(L"Event object creation failed: %d\n",GetLastError());
    return;
  }
  // Register to receive auditing policy change notifications.
  ntsResult = LsaRegisterPolicyChangeNotification(
    PolicyNotifyAuditEventsInformation,
    hEvent
  );
  if (STATUS_SUCCESS != ntsResult)
  {
    wprintf(L"LsaRegisterPolicyChangeNotification failed.\n");
    CloseHandle(hEvent);
    return;
  }

  // Wait for the event to be triggered.
  dwResult = WaitForSingleObject( 
    hEvent, // handle to the event object
    300000  // time-out interval, in milliseconds
  );

  // The wait function returned.
  if (dwResult == WAIT_OBJECT_0)
  {  // received the notification signal
    wprintf(L"Notification received.\n");
  } 
  else 
  {  // received a time-out or error
    wprintf(L"Notification was not received.\n");
  }
  // Unregister for notification.
  LsaUnregisterPolicyChangeNotification(
    PolicyNotifyAuditEventsInformation,
    hEvent
  );

  // Free the event handle.
  CloseHandle(hEvent);
}
```



Para obter mais informações sobre objetos de evento, funções de espera e sincronização, consulte [usando objetos de evento](/windows/desktop/Sync/using-event-objects).

 

 
