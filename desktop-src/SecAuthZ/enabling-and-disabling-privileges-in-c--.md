---
description: A habilitação de um privilégio em um token de acesso permite que o processo execute ações no nível do sistema que não podiam ser realizadas anteriormente.
ms.assetid: aa2d3fe7-01ee-4243-b72c-3e8b90068e22
title: Habilitando e desabilitando privilégios em C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 354f3ac2b27a7c027bd7c48e753263c43b676dd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011519"
---
# <a name="enabling-and-disabling-privileges-in-c"></a>Habilitando e desabilitando privilégios em C++

A habilitação de um privilégio em um token de acesso permite que o processo execute ações no nível do sistema que não podiam ser realizadas anteriormente. Seu aplicativo deve verificar completamente se o privilégio é apropriado para o tipo de conta, especialmente para os seguintes privilégios poderosos.



| Constante de privilégio           | Valor da cadeia de caracteres                  | Nome de exibição                        |
|------------------------------|-------------------------------|-------------------------------------|
| \_nome do ASSIGNPRIMARYTOKEN se \_ | SeAssignPrimaryTokenPrivilege | Substituir um token de nível de processo       |
| \_nome do backup se \_             | SeBackupPrivilege             | Fazer backup de arquivos e pastas       |
| \_nome da depuração se \_              | SeDebugPrivilege              | Depurar programas                      |
| SE \_ aumentar \_ nome da cota \_    | SeIncreaseQuotaPrivilege      | Ajustar quotas de memória para um processo  |
| \_nome TCB do se \_                | SeTcbPrivilege;                | Atuar como parte do sistema operacional |



 

Antes de habilitar qualquer um desses privilégios potencialmente perigosos, determine que as funções ou operações em seu código realmente exigem os privilégios. Por exemplo, muito poucas funções no sistema operacional realmente exigem o **SeTcbPrivilege;**. Para obter uma lista de todos os privilégios disponíveis, consulte [constantes de privilégio](authorization-constants.md).

O exemplo a seguir mostra como habilitar ou desabilitar um privilégio em um [*token de acesso*](/windows/desktop/SecGloss/a-gly). O exemplo chama a função [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) para obter o [*identificador local exclusivo*](/windows/desktop/SecGloss/l-gly) (LUID) que o sistema local usa para identificar o privilégio. Em seguida, o exemplo chama a função [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) , que habilita ou desabilita o privilégio que depende do valor do parâmetro *bEnablePrivilege* .


```C++
#include <windows.h>
#include <stdio.h>
#pragma comment(lib, "cmcfg32.lib")

BOOL SetPrivilege(
    HANDLE hToken,          // access token handle
    LPCTSTR lpszPrivilege,  // name of privilege to enable/disable
    BOOL bEnablePrivilege   // to enable or disable privilege
    ) 
{
    TOKEN_PRIVILEGES tp;
    LUID luid;

    if ( !LookupPrivilegeValue( 
            NULL,            // lookup privilege on local system
            lpszPrivilege,   // privilege to lookup 
            &luid ) )        // receives LUID of privilege
    {
        printf("LookupPrivilegeValue error: %u\n", GetLastError() ); 
        return FALSE; 
    }

    tp.PrivilegeCount = 1;
    tp.Privileges[0].Luid = luid;
    if (bEnablePrivilege)
        tp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED;
    else
        tp.Privileges[0].Attributes = 0;

    // Enable the privilege or disable all privileges.

    if ( !AdjustTokenPrivileges(
           hToken, 
           FALSE, 
           &tp, 
           sizeof(TOKEN_PRIVILEGES), 
           (PTOKEN_PRIVILEGES) NULL, 
           (PDWORD) NULL) )
    { 
          printf("AdjustTokenPrivileges error: %u\n", GetLastError() ); 
          return FALSE; 
    } 

    if (GetLastError() == ERROR_NOT_ALL_ASSIGNED)

    {
          printf("The token does not have the specified privilege. \n");
          return FALSE;
    } 

    return TRUE;
}

```



 

