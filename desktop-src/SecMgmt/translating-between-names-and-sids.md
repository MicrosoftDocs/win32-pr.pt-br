---
description: A autoridade de segurança local (LSA) fornece funções para converter entre o usuário, o grupo e os nomes de grupo local e seus valores de SID (identificador de segurança) correspondentes.
ms.assetid: 8845b709-a8f9-4d0f-a4a6-86d23d6b01d5
title: Convertendo entre nomes e SIDs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417034a99331c09f20546f2f352bc762a86f02e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779936"
---
# <a name="translating-between-names-and-sids"></a>Convertendo entre nomes e SIDs

A [*autoridade de segurança local*](/windows/desktop/SecGloss/l-gly) (LSA) fornece funções para converter entre o usuário, o grupo e os nomes de grupo local e seus valores de Sid ( [*identificador de segurança*](/windows/desktop/SecGloss/s-gly) ) correspondentes. Para localizar nomes de conta, chame a função [**LsaLookupNames**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames) . Essa função retorna o SID como um par de índices RID/Domain. Para obter o SID como um único elemento, chame a função [**LsaLookupNames2**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2) . Para localizar SIDs, chame [**LsaLookupSids**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids).

Essas funções podem traduzir informações de nome e SID de qualquer domínio confiável pelo sistema local.

Antes de poder converter entre os nomes de conta e os SIDs, seu aplicativo deve obter um identificador para o objeto de [**política**](policy-object.md) local, conforme demonstrado na [abertura de um identificador de objeto de política](opening-a-policy-object-handle.md).

O exemplo a seguir pesquisa o SID de uma conta, dado o nome da conta.


```C++
void GetSIDInformation (LPWSTR AccountName,LSA_HANDLE PolicyHandle)
{
  LSA_UNICODE_STRING lucName;
  PLSA_TRANSLATED_SID ltsTranslatedSID;
  PLSA_REFERENCED_DOMAIN_LIST lrdlDomainList;
  LSA_TRUST_INFORMATION myDomain;
  NTSTATUS ntsResult;
  PWCHAR DomainString = NULL;

  // Initialize an LSA_UNICODE_STRING with the name.
  if (!InitLsaString(&lucName, AccountName))
  {
         wprintf(L"Failed InitLsaString\n");
         return;
  }

  ntsResult = LsaLookupNames(
     PolicyHandle,     // handle to a Policy object
     1,                // number of names to look up
     &lucName,         // pointer to an array of names
     &lrdlDomainList,  // receives domain information
     &ltsTranslatedSID // receives relative SIDs
  );
  if (STATUS_SUCCESS != ntsResult) 
  {
    wprintf(L"Failed LsaLookupNames - %lu \n",
      LsaNtStatusToWinError(ntsResult));
    return;
  }

  // Get the domain the account resides in.
  myDomain = lrdlDomainList->Domains[ltsTranslatedSID->DomainIndex];
  DomainString = (PWCHAR) LocalAlloc(LPTR, myDomain.Name.Length + 1);
  wcsncpy_s(DomainString,
     myDomain.Name.Length + 1, 
     myDomain.Name.Buffer, 
     myDomain.Name.Length);

  // Display the relative Id. 
  wprintf(L"Relative Id is %lu in domain %ws.\n",
    ltsTranslatedSID->RelativeId,
    DomainString);

  LocalFree(DomainString);
  LsaFreeMemory(ltsTranslatedSID);
  LsaFreeMemory(lrdlDomainList);
}
```



No exemplo anterior, a função **InitLsaString** converte uma cadeia de caracteres Unicode em uma estrutura de [**cadeia de \_ \_ caracteres Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) . O código para essa função é mostrado em [usando cadeias de caracteres de Unicode LSA](using-lsa-unicode-strings.md).

> [!Note]  
> Essas funções de tradução são fornecidas principalmente para uso por editores de permissões para exibir informações de ACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/a-gly) ). Um editor de permissões sempre deve chamar essas funções usando o objeto de [**política**](policy-object.md) para o sistema no qual o nome ou o SID do [*identificador de segurança*](/windows/desktop/SecGloss/s-gly) está localizado. Isso garante que o conjunto adequado de domínios confiáveis seja referenciado durante a tradução.

 

O controle de acesso do Windows também fornece funções que executam traduções entre SIDs e nomes de conta: [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) e [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida). Se o seu aplicativo precisar pesquisar um nome de conta ou SID e não usar a funcionalidade de política LSA adicional, use as funções de controle de acesso do Windows em vez das funções de política de LSA. Para obter mais informações sobre essas funções, consulte [controle de acesso](/windows/desktop/SecAuthZ/access-control).

 

 
