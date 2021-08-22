---
description: A LSA (Autoridade de Segurança Local) fornece funções para traduzir entre nomes de usuário, grupo e grupo local e seus valores de SID (identificador de segurança) correspondentes.
ms.assetid: 8845b709-a8f9-4d0f-a4a6-86d23d6b01d5
title: Traduzindo entre nomes e SIDs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d5f67bd95e41a9813522d635e737f4fc528a61aebceeab205a2d40e1f44d7c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004804"
---
# <a name="translating-between-names-and-sids"></a>Traduzindo entre nomes e SIDs

A LSA (Autoridade de Segurança [*Local)*](/windows/desktop/SecGloss/l-gly) fornece funções para traduzir entre nomes de usuário, grupo e grupo local e seus valores de SID (identificador de segurança) correspondentes. [](/windows/desktop/SecGloss/s-gly) Para localizar nomes de conta, chame a [**função LsaLookupNames.**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames) Essa função retorna o SID como um par de índice RID/Domain. Para obter o SID como um único elemento, chame a [**função LsaLookupNames2.**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2) Para localizar SIDs, chame [**LsaLookupSids.**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids)

Essas funções podem converter informações de nome e SID de qualquer domínio confiável pelo sistema local.

Antes de converter entre nomes de conta e SIDs, seu aplicativo deve obter um identificador para o objeto De política [**local,**](policy-object.md) conforme demonstrado em Abrindo um identificador [de objeto de política](opening-a-policy-object-handle.md).

O exemplo a seguir procura o SID de uma conta, considerando o nome da conta.


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



No exemplo anterior, a função **InitLsaString** converte uma cadeia de caracteres Unicode em uma estrutura DE CADEIA DE [**CARACTERES \_ UNICODE \_ LSA.**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) O código para essa função é mostrado em Usando [cadeias de caracteres Unicode LSA](using-lsa-unicode-strings.md).

> [!Note]  
> Essas funções de tradução são fornecidas principalmente para uso por editores de permissões para exibir [*informações*](/windows/desktop/SecGloss/a-gly) de ACL (lista de controle de acesso). Um editor de permissões sempre deve chamar essas funções usando o [**objeto Política**](policy-object.md) para o sistema em que o nome ou SID [*do identificador de*](/windows/desktop/SecGloss/s-gly) segurança está localizado. Isso garante que o conjunto adequado de domínios confiáveis seja referenciado durante a tradução.

 

Windows O Controle de Acesso também fornece funções que executam traduções entre SIDs e nomes de conta: [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) e [**LookupAccountSid.**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) Se o aplicativo precisar procurar um nome de conta ou SID e não usar a funcionalidade de política LSA adicional, use as funções de Controle de Acesso Windows em vez das funções de Política de LSA. Para obter mais informações sobre essas funções, consulte [Controle de acesso](/windows/desktop/SecAuthZ/access-control).

 

 
