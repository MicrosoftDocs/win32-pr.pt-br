---
description: O LSA fornece funções que os administradores podem usar para consultar e definir informações de política global para o computador local e o domínio.
ms.assetid: bbe27d16-0a6b-435a-ae80-5e983047b511
title: Gerenciando informações de política
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fdc76137f41c592370dbeecafd243f11012cb1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768425"
---
# <a name="managing-policy-information"></a><span data-ttu-id="380b6-103">Gerenciando informações de política</span><span class="sxs-lookup"><span data-stu-id="380b6-103">Managing Policy Information</span></span>

<span data-ttu-id="380b6-104">O LSA fornece funções que os administradores podem usar para consultar e definir informações de política global para o computador local e o domínio.</span><span class="sxs-lookup"><span data-stu-id="380b6-104">The LSA provides functions that administrators can use to query and set global policy information for the local computer and the domain.</span></span>

<span data-ttu-id="380b6-105">Antes de poder gerenciar as informações de política, seu aplicativo deve obter um identificador para o objeto de [**política**](policy-object.md) local, conforme demonstrado na [abertura de um identificador de objeto de política](opening-a-policy-object-handle.md).</span><span class="sxs-lookup"><span data-stu-id="380b6-105">Before you can manage policy information, your application must get a handle to the local [**Policy**](policy-object.md) object, as demonstrated in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span> <span data-ttu-id="380b6-106">Esse identificador é exigido pelas funções que gerenciam informações de política.</span><span class="sxs-lookup"><span data-stu-id="380b6-106">This handle is required by the functions that manage policy information.</span></span>

<span data-ttu-id="380b6-107">Para recuperar informações sobre a política de segurança local, chame [**LsaQueryInformationPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy).</span><span class="sxs-lookup"><span data-stu-id="380b6-107">To retrieve information about the local security policy, call [**LsaQueryInformationPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy).</span></span> <span data-ttu-id="380b6-108">Para definir a política de segurança local, chame [**LsaSetInformationPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasetinformationpolicy).</span><span class="sxs-lookup"><span data-stu-id="380b6-108">To set local security policy, call [**LsaSetInformationPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasetinformationpolicy).</span></span> <span data-ttu-id="380b6-109">A descrição da [**classe de \_ informações \_ da política**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class) de enumeração fornece detalhes sobre os tipos de informações de política que podem ser consultados ou definidos.</span><span class="sxs-lookup"><span data-stu-id="380b6-109">The description of the [**POLICY\_INFORMATION\_CLASS**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class) enumeration details the types of policy information that can be queried or set.</span></span>

<span data-ttu-id="380b6-110">O exemplo a seguir demonstra como obter as informações de domínio da conta do sistema, considerando um identificador para o objeto de [**política**](policy-object.md) do sistema.</span><span class="sxs-lookup"><span data-stu-id="380b6-110">The following example demonstrates how to obtain a system's account domain information, given a handle to the system's [**Policy**](policy-object.md) object.</span></span>


```C++
#include <windows.h>

BOOL GetAccountDomainInfo(LSA_HANDLE PolicyHandle)
{
  NTSTATUS ntsResult = STATUS_SUCCESS;
  PPOLICY_ACCOUNT_DOMAIN_INFO pPADInfo = NULL;
  PWCHAR name = NULL;
  UINT nameSize;
  
  ntsResult = LsaQueryInformationPolicy(
    PolicyHandle,                   // Open handle to a Policy object.
    PolicyAccountDomainInformation, // The information to get.
    (PVOID *)&pPADInfo              // Storage for the information.
  );

  if (ntsResult == STATUS_SUCCESS)
  {  
    // There is no guarantee that the LSA_UNICODE_STRING buffer
    // is null-terminated, so copy the name to a buffer that is.
    nameSize =  pPADInfo->DomainName.Length + 1 * sizeof(WCHAR);
    name = (WCHAR *) LocalAlloc(LPTR, nameSize);
    if (!name)
    {
        wprintf(L"Failed LocalAlloc\n");
        exit(1);
    }
    wcsncpy_s(name, nameSize, pPADInfo->DomainName.Buffer,
        pPADInfo->DomainName.Length);
    wprintf(L"The account domain name is %ws\n", name);
    LocalFree(name);
    if (STATUS_SUCCESS != LsaFreeMemory(pPADInfo))
        wprintf(L"LsaFreeMemory error\n");
  }
  else
  {
    // Show the corresponding win32 error code.
    wprintf(
        L"Error obtaining account domain information - (win32) %lu\n",
        LsaNtStatusToWinError(ntsResult));
  }

  return !ntsResult;
}

```



 

 
