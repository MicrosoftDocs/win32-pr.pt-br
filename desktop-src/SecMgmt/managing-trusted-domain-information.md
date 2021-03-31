---
description: A política LSA fornece várias funções que você pode usar para criar, enumerar e excluir domínios confiáveis e para definir e recuperar informações de domínio confiável.
ms.assetid: 0c7534d7-3372-49c4-992c-9b519279982d
title: Gerenciando informações de domínio confiável
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b7df297b8c83ebe9054ca6f04b657905c21fae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171104"
---
# <a name="managing-trusted-domain-information"></a>Gerenciando informações de domínio confiável

A política LSA fornece várias funções que você pode usar para criar, enumerar e excluir domínios confiáveis e para definir e recuperar informações de domínio confiável.

Antes que você possa gerenciar informações de domínio confiável, seu aplicativo deve obter um identificador para um objeto de [**política**](policy-object.md) , conforme explicado na [abertura de um identificador de objeto de política](opening-a-policy-object-handle.md).

Você pode enumerar os domínios confiáveis chamando [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex).

Para recuperar informações sobre um domínio confiável, chame [**LsaQueryTrustedDomainInfo**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo) ou [**LsaQueryTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfobyname). Ambas as funções retornam as mesmas informações; no entanto, **LsaQueryTrustedDomainInfo** identifica o domínio confiável por Sid e **LsaQueryTrustedDomainInfoByName** identifica o domínio confiável pelo nome.

Para definir informações para um domínio confiável, chame [**LsaSetTrustedDomainInformation**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation) ou [**LsaSetTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininfobyname). Assim como acontece com as funções de consulta, **LsaSetTrustedDomainInformation** identifica o domínio confiável por Sid, enquanto **LsaSetTrustedDomainInfoByName** identifica o domínio confiável pelo nome.

Seu aplicativo pode revogar uma relação de confiança para um domínio confiável chamando [**LsaDeleteTrustedDomain**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsadeletetrusteddomain).

O exemplo a seguir enumera os domínios confiáveis para o sistema local.


```C++
#include <windows.h>

void EnumerateTrusts(LSA_HANDLE PolicyHandle)
{
  LSA_ENUMERATION_HANDLE hEnum=0; 
  PLSA_TRUST_INFORMATION TrustInfo = NULL;
  ULONG ulReturned = 0;               
  NTSTATUS Status = 0;
  ULONG i;
  WCHAR StringBuffer[256];

  // Enumerate the trusted domains until there are no more to return.
  do 
  {
    Status = LsaEnumerateTrustedDomains(
       PolicyHandle,         // an open policy handle
       &hEnum,               // enumeration tracker
       (PVOID*)&TrustInfo,   // buffer to receive data
       32000,                // recommended buffer size
       &ulReturned           // number of items returned in TrustInfo
    );

    // Check the return status for errors.
    if((Status != STATUS_SUCCESS) &&
       (Status != STATUS_MORE_ENTRIES) &&
     (Status != STATUS_NO_MORE_ENTRIES))
      {
        // Handle the error.
        wprintf(L"Error occurred enumerating domains %lu\n",
        LsaNtStatusToWinError(Status));
        return;
      } 

      wprintf(L"Status %lu\n", LsaNtStatusToWinError(Status));
      // Process the trusted domain information.
      for (i=0;i<ulReturned; i++) 
      {
        // LSA_Unicode strings might not be null-terminated.
        if(TrustInfo[i].Name.Length < 256)
        {
            wcsncpy_s(StringBuffer,
                256,
                TrustInfo[i].Name.Buffer,
                TrustInfo[i].Name.Length
            );
            // Guarantee that StringBuffer is null-terminated.
            StringBuffer[TrustInfo[i].Name.Length] = NULL; 
        }
        else
        {
            fprintf(stderr, "Name too long for string buffer.\n");
            exit(1);
        }
        
        wprintf(L"Enum Trusted Domain - %ws ", StringBuffer);
      }
      // Free the buffer.
      if (TrustInfo != NULL) 
      {
        LsaFreeMemory(TrustInfo);
        TrustInfo = NULL;
      }
    } while (Status != STATUS_NO_MORE_ENTRIES);
    return;
}
```



 

 



