---
description: O exemplo a seguir usa a função ExitWindowsEx para desligar o sistema.
ms.assetid: bf8723aa-1c7f-4761-9034-d5a9447a4bc4
title: Como desligar o sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3880319e0ada6c82c6c6c12a7f3b5faf00415a93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749442"
---
# <a name="how-to-shut-down-the-system"></a>Como desligar o sistema

O exemplo a seguir usa a função [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) para desligar o sistema. Desligar libera os buffers de arquivo para o disco e leva o sistema a uma condição em que é seguro desligar o computador. O aplicativo deve primeiro habilitar o \_ privilégio de nome de desligamento se \_ . Para obter mais informações, consulte [privilégios](../secauthz/privileges.md).


```C++
#include <windows.h>

#pragma comment(lib, "user32.lib")
#pragma comment(lib, "advapi32.lib")

BOOL MySystemShutdown()
{
   HANDLE hToken; 
   TOKEN_PRIVILEGES tkp; 
 
   // Get a token for this process. 
 
   if (!OpenProcessToken(GetCurrentProcess(), 
        TOKEN_ADJUST_PRIVILEGES | TOKEN_QUERY, &hToken)) 
      return( FALSE ); 
 
   // Get the LUID for the shutdown privilege. 
 
   LookupPrivilegeValue(NULL, SE_SHUTDOWN_NAME, 
        &tkp.Privileges[0].Luid); 
 
   tkp.PrivilegeCount = 1;  // one privilege to set    
   tkp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED; 
 
   // Get the shutdown privilege for this process. 
 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
        (PTOKEN_PRIVILEGES)NULL, 0); 
 
   if (GetLastError() != ERROR_SUCCESS) 
      return FALSE; 
 
   // Shut down the system and force all applications to close. 
 
   if (!ExitWindowsEx(EWX_SHUTDOWN | EWX_FORCE, 
               SHTDN_REASON_MAJOR_OPERATINGSYSTEM |
               SHTDN_REASON_MINOR_UPGRADE |
               SHTDN_REASON_FLAG_PLANNED)) 
      return FALSE; 

   //shutdown was successful
   return TRUE;
}
```



O parâmetro final na chamada para [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) indica que o sistema foi desligado para uma atualização de planejamento do sistema operacional. Para obter mais informações, consulte [códigos de motivo de desligamento do sistema](system-shutdown-reason-codes.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desligando](shutting-down.md)
</dt> </dl>

 

 
