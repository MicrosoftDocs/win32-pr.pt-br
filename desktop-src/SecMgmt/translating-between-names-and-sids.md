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
# <a name="translating-between-names-and-sids"></a><span data-ttu-id="54a9f-103">Convertendo entre nomes e SIDs</span><span class="sxs-lookup"><span data-stu-id="54a9f-103">Translating Between Names and SIDs</span></span>

<span data-ttu-id="54a9f-104">A [*autoridade de segurança local*](/windows/desktop/SecGloss/l-gly) (LSA) fornece funções para converter entre o usuário, o grupo e os nomes de grupo local e seus valores de Sid ( [*identificador de segurança*](/windows/desktop/SecGloss/s-gly) ) correspondentes.</span><span class="sxs-lookup"><span data-stu-id="54a9f-104">The [*Local Security Authority*](/windows/desktop/SecGloss/l-gly) (LSA) provides functions to translate between user, group, and local group names and their corresponding [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) values.</span></span> <span data-ttu-id="54a9f-105">Para localizar nomes de conta, chame a função [**LsaLookupNames**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames) .</span><span class="sxs-lookup"><span data-stu-id="54a9f-105">To locate account names, call the [**LsaLookupNames**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames) function.</span></span> <span data-ttu-id="54a9f-106">Essa função retorna o SID como um par de índices RID/Domain.</span><span class="sxs-lookup"><span data-stu-id="54a9f-106">This function returns the SID as a RID/Domain index pair.</span></span> <span data-ttu-id="54a9f-107">Para obter o SID como um único elemento, chame a função [**LsaLookupNames2**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2) .</span><span class="sxs-lookup"><span data-stu-id="54a9f-107">To get the SID as a single element, call the [**LsaLookupNames2**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2) function.</span></span> <span data-ttu-id="54a9f-108">Para localizar SIDs, chame [**LsaLookupSids**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids).</span><span class="sxs-lookup"><span data-stu-id="54a9f-108">To locate SIDs, call [**LsaLookupSids**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids).</span></span>

<span data-ttu-id="54a9f-109">Essas funções podem traduzir informações de nome e SID de qualquer domínio confiável pelo sistema local.</span><span class="sxs-lookup"><span data-stu-id="54a9f-109">These functions can translate name and SID information from any domain trusted by the local system.</span></span>

<span data-ttu-id="54a9f-110">Antes de poder converter entre os nomes de conta e os SIDs, seu aplicativo deve obter um identificador para o objeto de [**política**](policy-object.md) local, conforme demonstrado na [abertura de um identificador de objeto de política](opening-a-policy-object-handle.md).</span><span class="sxs-lookup"><span data-stu-id="54a9f-110">Before you can translate between account names and SIDs, your application must get a handle to the local [**Policy**](policy-object.md) object, as demonstrated in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span>

<span data-ttu-id="54a9f-111">O exemplo a seguir pesquisa o SID de uma conta, dado o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="54a9f-111">The following example looks up the SID for an account, given the account name.</span></span>


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



<span data-ttu-id="54a9f-112">No exemplo anterior, a função **InitLsaString** converte uma cadeia de caracteres Unicode em uma estrutura de [**cadeia de \_ \_ caracteres Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) .</span><span class="sxs-lookup"><span data-stu-id="54a9f-112">In the preceding example, the function **InitLsaString** converts a Unicode string to an [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structure.</span></span> <span data-ttu-id="54a9f-113">O código para essa função é mostrado em [usando cadeias de caracteres de Unicode LSA](using-lsa-unicode-strings.md).</span><span class="sxs-lookup"><span data-stu-id="54a9f-113">The code for this function is shown in [Using LSA Unicode Strings](using-lsa-unicode-strings.md).</span></span>

> [!Note]  
> <span data-ttu-id="54a9f-114">Essas funções de tradução são fornecidas principalmente para uso por editores de permissões para exibir informações de ACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/a-gly) ).</span><span class="sxs-lookup"><span data-stu-id="54a9f-114">These translation functions are primarily provided for use by permissions editors to display [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL) information.</span></span> <span data-ttu-id="54a9f-115">Um editor de permissões sempre deve chamar essas funções usando o objeto de [**política**](policy-object.md) para o sistema no qual o nome ou o SID do [*identificador de segurança*](/windows/desktop/SecGloss/s-gly) está localizado.</span><span class="sxs-lookup"><span data-stu-id="54a9f-115">A permission editor should always call these functions using the [**Policy**](policy-object.md) object for the system where the name or [*security identifier*](/windows/desktop/SecGloss/s-gly) SID is located.</span></span> <span data-ttu-id="54a9f-116">Isso garante que o conjunto adequado de domínios confiáveis seja referenciado durante a tradução.</span><span class="sxs-lookup"><span data-stu-id="54a9f-116">This ensures that the proper set of trusted domains is referenced during the translation.</span></span>

 

<span data-ttu-id="54a9f-117">O controle de acesso do Windows também fornece funções que executam traduções entre SIDs e nomes de conta: [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) e [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida).</span><span class="sxs-lookup"><span data-stu-id="54a9f-117">Windows Access Control also provides functions that perform translations between SIDs and account names: [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) and [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida).</span></span> <span data-ttu-id="54a9f-118">Se o seu aplicativo precisar pesquisar um nome de conta ou SID e não usar a funcionalidade de política LSA adicional, use as funções de controle de acesso do Windows em vez das funções de política de LSA.</span><span class="sxs-lookup"><span data-stu-id="54a9f-118">If your application needs to look up an account name or SID and does not use additional LSA Policy functionality, use the Windows Access Control functions instead of the LSA Policy functions.</span></span> <span data-ttu-id="54a9f-119">Para obter mais informações sobre essas funções, consulte [controle de acesso](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="54a9f-119">For more information about these functions, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

 

 
