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
# <a name="opening-a-policy-object-handle"></a>Abrindo um identificador de objeto de política

A maioria das funções de diretiva LSA requer um identificador para o objeto de [**política**](policy-object.md) para o sistema consultar ou modificar. Para obter um identificador para um objeto de **política** , chame [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) e especifique o nome do sistema que você deseja acessar e o conjunto de permissões de acesso necessárias.

As permissões de acesso necessárias para seu aplicativo dependem das ações que ele executa. Para obter detalhes sobre as permissões necessárias para cada função, consulte a descrição dessa função em [funções de política LSA](management-functions.md).

Se a chamada para [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) for bem-sucedida, ela retornará um identificador para o objeto de [**política**](policy-object.md) para o sistema especificado. Em seguida, seu aplicativo passa esse identificador em chamadas de função de política LSA subsequentes. Quando o aplicativo não precisar mais do identificador, ele deverá chamar [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) para liberá-lo.

O exemplo a seguir mostra como abrir um identificador de objeto de [**política**](policy-object.md) .


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



No exemplo anterior, o aplicativo solicitou a política \_ todos os \_ [*privilégios*](/windows/desktop/SecGloss/p-gly)de acesso. Para obter detalhes sobre quais permissões seu aplicativo deve solicitar ao chamar [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), consulte as descrições das funções para as quais seu aplicativo passará o identificador do objeto de [**política**](policy-object.md) .

Para abrir um identificador para o objeto de [**política**](policy-object.md) de um domínio confiável, chame [**LsaCreateTrustedDomainEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex) (para criar uma nova relação de confiança com um domínio) ou chame [**LsaOpenTrustedDomainByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname) (para acessar um domínio confiável existente). Ambas as funções definem um ponteiro para um [**\_ identificador LSA**](lsa-handle.md), que você pode especificar em chamadas de função de política LSA subsequentes. Assim como com o [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), seu aplicativo deve chamar [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) quando ele não precisar mais do identificador para o objeto de **política** do domínio confiável.

 

 
