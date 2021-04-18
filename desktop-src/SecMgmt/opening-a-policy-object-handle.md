---
description: A maioria das funções de diretiva LSA requer um identificador para o objeto de política para o sistema consultar ou modificar. Para obter um identificador para um objeto de política, chame LsaOpenPolicy e especifique o nome do sistema que você deseja acessar e o conjunto de permissões de acesso necessárias.
ms.assetid: 66fdc878-d9c4-421c-b79f-9df08984611c
title: Abrindo um identificador de objeto de política
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c187720692db4937b6e1299dd2bb63fac647852
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760376"
---
# <a name="opening-a-policy-object-handle"></a><span data-ttu-id="07a4c-104">Abrindo um identificador de objeto de política</span><span class="sxs-lookup"><span data-stu-id="07a4c-104">Opening a Policy Object Handle</span></span>

<span data-ttu-id="07a4c-105">A maioria das funções de diretiva LSA requer um identificador para o objeto de [**política**](policy-object.md) para o sistema consultar ou modificar.</span><span class="sxs-lookup"><span data-stu-id="07a4c-105">Most LSA Policy functions require a handle to the [**Policy**](policy-object.md) object for the system to query or modify.</span></span> <span data-ttu-id="07a4c-106">Para obter um identificador para um objeto de **política** , chame [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) e especifique o nome do sistema que você deseja acessar e o conjunto de permissões de acesso necessárias.</span><span class="sxs-lookup"><span data-stu-id="07a4c-106">To obtain a handle to a **Policy** object, call [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) and specify the name of the system you want to access and the set of access permissions required.</span></span>

<span data-ttu-id="07a4c-107">As permissões de acesso necessárias para seu aplicativo dependem das ações que ele executa.</span><span class="sxs-lookup"><span data-stu-id="07a4c-107">The access permissions required for your application depend on the actions it performs.</span></span> <span data-ttu-id="07a4c-108">Para obter detalhes sobre as permissões necessárias para cada função, consulte a descrição dessa função em [funções de política LSA](management-functions.md).</span><span class="sxs-lookup"><span data-stu-id="07a4c-108">For details about the permissions required for each function, see the description of that function in [LSA Policy Functions](management-functions.md).</span></span>

<span data-ttu-id="07a4c-109">Se a chamada para [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) for bem-sucedida, ela retornará um identificador para o objeto de [**política**](policy-object.md) para o sistema especificado.</span><span class="sxs-lookup"><span data-stu-id="07a4c-109">If the call to [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) is successful, it returns a handle to the [**Policy**](policy-object.md) object for the specified system.</span></span> <span data-ttu-id="07a4c-110">Em seguida, seu aplicativo passa esse identificador em chamadas de função de política LSA subsequentes.</span><span class="sxs-lookup"><span data-stu-id="07a4c-110">Your application then passes this handle in subsequent LSA Policy function calls.</span></span> <span data-ttu-id="07a4c-111">Quando o aplicativo não precisar mais do identificador, ele deverá chamar [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) para liberá-lo.</span><span class="sxs-lookup"><span data-stu-id="07a4c-111">When your application no longer needs the handle, it should call [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) to free it.</span></span>

<span data-ttu-id="07a4c-112">O exemplo a seguir mostra como abrir um identificador de objeto de [**política**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="07a4c-112">The following example shows how to open a [**Policy**](policy-object.md) object handle.</span></span>


```C++
#include <windows.h>

#define TARGET_SYSTEM_NAME L"mysystem"

LSA_HANDLE GetPolicyHandle()
{
  LSA_OBJECT_ATTRIBUTES ObjectAttributes;
  WCHAR SystemName[] = TARGET_SYSTEM_NAME;
  USHORT SystemNameLength;
  LSA_UNICODE_STRING lusSystemName;
  NTSTATUS ntsResult;
  LSA_HANDLE lsahPolicyHandle;

  // Object attributes are reserved, so initialize to zeros.
  ZeroMemory(&ObjectAttributes, sizeof(ObjectAttributes));

  //Initialize an LSA_UNICODE_STRING to the server name.
  SystemNameLength = wcslen(SystemName);
  lusSystemName.Buffer = SystemName;
  lusSystemName.Length = SystemNameLength * sizeof(WCHAR);
  lusSystemName.MaximumLength = (SystemNameLength+1) * sizeof(WCHAR);

  // Get a handle to the Policy object.
  ntsResult = LsaOpenPolicy(
        &lusSystemName,    //Name of the target system.
        &ObjectAttributes, //Object attributes.
        POLICY_ALL_ACCESS, //Desired access permissions.
        &lsahPolicyHandle  //Receives the policy handle.
    );

  if (ntsResult != STATUS_SUCCESS)
  {
    // An error occurred. Display it as a win32 error code.
    wprintf(L"OpenPolicy returned %lu\n",
      LsaNtStatusToWinError(ntsResult));
    return NULL;
  } 
  return lsahPolicyHandle;
}
```



<span data-ttu-id="07a4c-113">No exemplo anterior, o aplicativo solicitou a política \_ todos os \_ [*privilégios*](/windows/desktop/SecGloss/p-gly)de acesso.</span><span class="sxs-lookup"><span data-stu-id="07a4c-113">In the preceding example, the application requested POLICY\_ALL\_ACCESS [*privileges*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="07a4c-114">Para obter detalhes sobre quais permissões seu aplicativo deve solicitar ao chamar [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), consulte as descrições das funções para as quais seu aplicativo passará o identificador do objeto de [**política**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="07a4c-114">For details about which permissions your application should request when calling [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), see the descriptions of the functions that your application will pass the [**Policy**](policy-object.md) object handle to.</span></span>

<span data-ttu-id="07a4c-115">Para abrir um identificador para o objeto de [**política**](policy-object.md) de um domínio confiável, chame [**LsaCreateTrustedDomainEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex) (para criar uma nova relação de confiança com um domínio) ou chame [**LsaOpenTrustedDomainByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname) (para acessar um domínio confiável existente).</span><span class="sxs-lookup"><span data-stu-id="07a4c-115">To open a handle to the [**Policy**](policy-object.md) object of a trusted domain, call [**LsaCreateTrustedDomainEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex) (to create a new trust relationship with a domain) or call [**LsaOpenTrustedDomainByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname) (to access an existing trusted domain).</span></span> <span data-ttu-id="07a4c-116">Ambas as funções definem um ponteiro para um [**\_ identificador LSA**](lsa-handle.md), que você pode especificar em chamadas de função de política LSA subsequentes.</span><span class="sxs-lookup"><span data-stu-id="07a4c-116">Both of these functions set a pointer to an [**LSA\_HANDLE**](lsa-handle.md), which you can then specify in subsequent LSA Policy function calls.</span></span> <span data-ttu-id="07a4c-117">Assim como com o [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), seu aplicativo deve chamar [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) quando ele não precisar mais do identificador para o objeto de **política** do domínio confiável.</span><span class="sxs-lookup"><span data-stu-id="07a4c-117">As with [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), your application should call [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) when it no longer needs the handle to the trusted domain's **Policy** object.</span></span>

 

 
