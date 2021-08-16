---
description: A habilitação de um privilégio em um token de acesso permite que o processo execute ações no nível do sistema que não podiam antes.
ms.assetid: aa2d3fe7-01ee-4243-b72c-3e8b90068e22
title: Habilitando e desabilitando privilégios em C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc36e3db162b1a7a7f12f1849ab7708bda19d90991e58a65135d0eb4c0abd04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117781722"
---
# <a name="enabling-and-disabling-privileges-in-c"></a>Habilitando e desabilitando privilégios em C++

A habilitação de um privilégio em um token de acesso permite que o processo execute ações no nível do sistema que não podiam antes. Seu aplicativo deve verificar completamente se o privilégio é apropriado para o tipo de conta, especialmente para os privilégios poderosos a seguir.



| Constante de privilégio           | Valor da cadeia de caracteres                  | Nome de exibição                        |
|------------------------------|-------------------------------|-------------------------------------|
| \_ES ASSIGNPRIMARYTOKEN \_ NAME | SeAssignPrimaryTokenPrivilege | Substituir um token de nível de processo       |
| \_ES NOME DO \_ BACKUP             | SeBackupPrivilege             | Fazer backup de arquivos e pastas       |
| \_ES NOME DA \_ DEPURAÇÃO              | SeDebugPrivilege              | Depurar programas                      |
| \_ES AUMENTAR O \_ NOME DA \_ COTA    | SeIncreaseQuotaPrivilege      | Ajustar quotas de memória para um processo  |
| \_ES NOME \_ DO TCB                | SeTcbPrivilege                | Atuar como parte do sistema operacional |



 

Antes de habilenciar qualquer um desses privilégios potencialmente perigosos, determine que as funções ou operações em seu código realmente exigem os privilégios. Por exemplo, poucas funções no sistema operacional realmente exigem **o SeTcbPrivilege.** Para ver uma lista de todos os privilégios disponíveis, consulte [Constantes de privilégio.](authorization-constants.md)

O exemplo a seguir mostra como habilitar ou desabilitar um privilégio em um [*token de acesso*](/windows/desktop/SecGloss/a-gly). O exemplo chama a [**função LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) para obter o LUID (identificador exclusivo [*local)*](/windows/desktop/SecGloss/l-gly) que o sistema local usa para identificar o privilégio. Em seguida, o exemplo chama a função [**AdjustTokenPrivileges,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) que habilita ou desabilita o privilégio que depende do valor do parâmetro *bEnablePrivilege.*


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



 

