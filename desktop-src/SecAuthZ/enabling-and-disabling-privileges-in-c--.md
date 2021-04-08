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
# <a name="enabling-and-disabling-privileges-in-c"></a><span data-ttu-id="f12f6-103">Habilitando e desabilitando privilégios em C++</span><span class="sxs-lookup"><span data-stu-id="f12f6-103">Enabling and Disabling Privileges in C++</span></span>

<span data-ttu-id="f12f6-104">A habilitação de um privilégio em um token de acesso permite que o processo execute ações no nível do sistema que não podiam ser realizadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f12f6-104">Enabling a privilege in an access token allows the process to perform system-level actions that it could not previously.</span></span> <span data-ttu-id="f12f6-105">Seu aplicativo deve verificar completamente se o privilégio é apropriado para o tipo de conta, especialmente para os seguintes privilégios poderosos.</span><span class="sxs-lookup"><span data-stu-id="f12f6-105">Your application should thoroughly verify that the privilege is appropriate to the type of account, especially for the following powerful privileges.</span></span>



| <span data-ttu-id="f12f6-106">Constante de privilégio</span><span class="sxs-lookup"><span data-stu-id="f12f6-106">Privilege constant</span></span>           | <span data-ttu-id="f12f6-107">Valor da cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="f12f6-107">String value</span></span>                  | <span data-ttu-id="f12f6-108">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="f12f6-108">Display name</span></span>                        |
|------------------------------|-------------------------------|-------------------------------------|
| <span data-ttu-id="f12f6-109">\_nome do ASSIGNPRIMARYTOKEN se \_</span><span class="sxs-lookup"><span data-stu-id="f12f6-109">SE\_ASSIGNPRIMARYTOKEN\_NAME</span></span> | <span data-ttu-id="f12f6-110">SeAssignPrimaryTokenPrivilege</span><span class="sxs-lookup"><span data-stu-id="f12f6-110">SeAssignPrimaryTokenPrivilege</span></span> | <span data-ttu-id="f12f6-111">Substituir um token de nível de processo</span><span class="sxs-lookup"><span data-stu-id="f12f6-111">Replace a process-level token</span></span>       |
| <span data-ttu-id="f12f6-112">\_nome do backup se \_</span><span class="sxs-lookup"><span data-stu-id="f12f6-112">SE\_BACKUP\_NAME</span></span>             | <span data-ttu-id="f12f6-113">SeBackupPrivilege</span><span class="sxs-lookup"><span data-stu-id="f12f6-113">SeBackupPrivilege</span></span>             | <span data-ttu-id="f12f6-114">Fazer backup de arquivos e pastas</span><span class="sxs-lookup"><span data-stu-id="f12f6-114">Back up files and directories</span></span>       |
| <span data-ttu-id="f12f6-115">\_nome da depuração se \_</span><span class="sxs-lookup"><span data-stu-id="f12f6-115">SE\_DEBUG\_NAME</span></span>              | <span data-ttu-id="f12f6-116">SeDebugPrivilege</span><span class="sxs-lookup"><span data-stu-id="f12f6-116">SeDebugPrivilege</span></span>              | <span data-ttu-id="f12f6-117">Depurar programas</span><span class="sxs-lookup"><span data-stu-id="f12f6-117">Debug programs</span></span>                      |
| <span data-ttu-id="f12f6-118">SE \_ aumentar \_ nome da cota \_</span><span class="sxs-lookup"><span data-stu-id="f12f6-118">SE\_INCREASE\_QUOTA\_NAME</span></span>    | <span data-ttu-id="f12f6-119">SeIncreaseQuotaPrivilege</span><span class="sxs-lookup"><span data-stu-id="f12f6-119">SeIncreaseQuotaPrivilege</span></span>      | <span data-ttu-id="f12f6-120">Ajustar quotas de memória para um processo</span><span class="sxs-lookup"><span data-stu-id="f12f6-120">Adjust memory quotas for a process</span></span>  |
| <span data-ttu-id="f12f6-121">\_nome TCB do se \_</span><span class="sxs-lookup"><span data-stu-id="f12f6-121">SE\_TCB\_NAME</span></span>                | <span data-ttu-id="f12f6-122">SeTcbPrivilege;</span><span class="sxs-lookup"><span data-stu-id="f12f6-122">SeTcbPrivilege</span></span>                | <span data-ttu-id="f12f6-123">Atuar como parte do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="f12f6-123">Act as part of the operating system</span></span> |



 

<span data-ttu-id="f12f6-124">Antes de habilitar qualquer um desses privilégios potencialmente perigosos, determine que as funções ou operações em seu código realmente exigem os privilégios.</span><span class="sxs-lookup"><span data-stu-id="f12f6-124">Before enabling any of these potentially dangerous privileges, determine that functions or operations in your code actually require the privileges.</span></span> <span data-ttu-id="f12f6-125">Por exemplo, muito poucas funções no sistema operacional realmente exigem o **SeTcbPrivilege;**.</span><span class="sxs-lookup"><span data-stu-id="f12f6-125">For example, very few functions in the operating system actually require the **SeTcbPrivilege**.</span></span> <span data-ttu-id="f12f6-126">Para obter uma lista de todos os privilégios disponíveis, consulte [constantes de privilégio](authorization-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f12f6-126">For a list of all the available privileges, see [Privilege Constants](authorization-constants.md).</span></span>

<span data-ttu-id="f12f6-127">O exemplo a seguir mostra como habilitar ou desabilitar um privilégio em um [*token de acesso*](/windows/desktop/SecGloss/a-gly).</span><span class="sxs-lookup"><span data-stu-id="f12f6-127">The following example shows how to enable or disable a privilege in an [*access token*](/windows/desktop/SecGloss/a-gly).</span></span> <span data-ttu-id="f12f6-128">O exemplo chama a função [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) para obter o [*identificador local exclusivo*](/windows/desktop/SecGloss/l-gly) (LUID) que o sistema local usa para identificar o privilégio.</span><span class="sxs-lookup"><span data-stu-id="f12f6-128">The example calls the [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) function to get the [*locally unique identifier*](/windows/desktop/SecGloss/l-gly) (LUID) that the local system uses to identify the privilege.</span></span> <span data-ttu-id="f12f6-129">Em seguida, o exemplo chama a função [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) , que habilita ou desabilita o privilégio que depende do valor do parâmetro *bEnablePrivilege* .</span><span class="sxs-lookup"><span data-stu-id="f12f6-129">Then the example calls the [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function, which either enables or disables the privilege that depends on the value of the *bEnablePrivilege* parameter.</span></span>


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



 

