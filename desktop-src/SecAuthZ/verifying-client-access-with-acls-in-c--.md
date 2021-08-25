---
description: Verifique os direitos de acesso que um descritor de segurança permite para um cliente.
ms.assetid: de21968e-4590-4798-9152-43204d55521f
title: Verificando o acesso do cliente com ACLs no C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2160b48a3b88a617eaaea1e8fae63168db5a85e82cad62be5aef248ff51581
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906686"
---
# <a name="verifying-client-access-with-acls-in-c"></a>Verificando o acesso do cliente com ACLs no C++

O exemplo a seguir mostra como um servidor pode verificar os direitos de acesso que um [*descritor de*](/windows/desktop/SecGloss/s-gly) segurança permite para um cliente. O exemplo usa a [**função ImpersonateNamedPipeClient;**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) no entanto, funcionaria da mesma forma usando qualquer uma das outras funções de representação. Depois de representar o cliente, o exemplo chama a [**função OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) para obter o [*token de representação*](/windows/desktop/SecGloss/i-gly). Em seguida, ele chama a [**função MapGenericMask**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-mapgenericmask) para converter quaisquer direitos de acesso genéricos para os direitos específicos e padrão correspondentes de acordo com o mapeamento especificado na estrutura [**GENERIC \_ MAPPING.**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping)

A [**função AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) verifica os direitos de acesso solicitados em relação aos direitos permitidos para o cliente na DACL do descritor de segurança. Para verificar o acesso e gerar uma entrada no log de eventos de segurança, use a [**função AccessCheckAndAuditAlarm.**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma)


```C++
#include <windows.h>
#pragma comment(lib, "advapi32.lib")

BOOL ImpersonateAndCheckAccess(
  HANDLE hNamedPipe,               // handle of pipe to impersonate
  PSECURITY_DESCRIPTOR pSD,        // security descriptor to check
  DWORD dwAccessDesired,           // access rights to check
  PGENERIC_MAPPING pGeneric,       // generic mapping for object
  PDWORD pdwAccessAllowed          // returns allowed access rights
) 
{
   HANDLE hToken;
   PRIVILEGE_SET PrivilegeSet;
   DWORD dwPrivSetSize = sizeof( PRIVILEGE_SET );
   BOOL fAccessGranted=FALSE;

// Impersonate the client.

   if (! ImpersonateNamedPipeClient(hNamedPipe) ) 
      return FALSE;

// Get an impersonation token with the client's security context.

   if (! OpenThreadToken( GetCurrentThread(), TOKEN_ALL_ACCESS,
         TRUE, &hToken ))
   {
      goto Cleanup;
   }

// Use the GENERIC_MAPPING structure to convert any 
// generic access rights to object-specific access rights.

   MapGenericMask( &dwAccessDesired, pGeneric );

// Check the client's access rights.

   if( !AccessCheck( 
      pSD,                 // security descriptor to check
      hToken,              // impersonation token
      dwAccessDesired,     // requested access rights
      pGeneric,            // pointer to GENERIC_MAPPING
      &PrivilegeSet,       // receives privileges used in check
      &dwPrivSetSize,      // size of PrivilegeSet buffer
      pdwAccessAllowed,    // receives mask of allowed access rights
      &fAccessGranted ))   // receives results of access check
   {
      goto Cleanup;
   }

Cleanup:

   RevertToSelf();

   if (hToken != INVALID_HANDLE_VALUE)
      CloseHandle(hToken);  

   return fAccessGranted;
}
```



 

 
