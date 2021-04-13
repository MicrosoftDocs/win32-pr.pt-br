---
description: A política LSA fornece duas funções que você pode usar para definir e recuperar dados privados.
ms.assetid: 7b6e63d4-ce8f-4279-85d9-da6b2b589afa
title: Armazenando dados privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6281f77e66a4217bda534b34342d6cefd92bd7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370640"
---
# <a name="storing-private-data"></a><span data-ttu-id="e6480-103">Armazenando dados privados</span><span class="sxs-lookup"><span data-stu-id="e6480-103">Storing Private Data</span></span>

<span data-ttu-id="e6480-104">A política LSA fornece duas funções que você pode usar para definir e recuperar dados privados.</span><span class="sxs-lookup"><span data-stu-id="e6480-104">LSA Policy provides two functions that you can use to set and retrieve private data.</span></span> <span data-ttu-id="e6480-105">Esses dados são armazenados como uma cadeia de caracteres criptografada no registro.</span><span class="sxs-lookup"><span data-stu-id="e6480-105">This data is stored as an encrypted string in the registry.</span></span> <span data-ttu-id="e6480-106">Por exemplo, você pode usar essas funções para armazenar senhas de conta de servidor e outras informações confidenciais.</span><span class="sxs-lookup"><span data-stu-id="e6480-106">For example, you can use these functions to store server account passwords and other sensitive information.</span></span>

<span data-ttu-id="e6480-107">Chame a função [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) para armazenar e criptografar dados privados.</span><span class="sxs-lookup"><span data-stu-id="e6480-107">Call the [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) function to store and encrypt private data.</span></span> <span data-ttu-id="e6480-108">Conforme descrito em [Private Data Object](private-data-object.md), os objetos de dados privados incluem três tipos especializados: local, global e computador.</span><span class="sxs-lookup"><span data-stu-id="e6480-108">As described in [Private Data Object](private-data-object.md), private data objects include three specialized types: local, global, and machine.</span></span> <span data-ttu-id="e6480-109">Para criar um objeto especializado, adicione um prefixo ao nome da chave passado para **LsaStorePrivateData**: "L $" para objetos locais, "G $" para objetos globais e "M $" para objetos de máquina.</span><span class="sxs-lookup"><span data-stu-id="e6480-109">To create a specialized object, add a prefix to the key name passed to **LsaStorePrivateData**: "L$" for local objects, "G$" for global objects, and "M$" for machine objects.</span></span> <span data-ttu-id="e6480-110">Se você não estiver criando um desses tipos especializados, não será necessário especificar um prefixo de nome de chave.</span><span class="sxs-lookup"><span data-stu-id="e6480-110">If you are not creating one of these specialized types, you do not need to specify a key name prefix.</span></span>

<span data-ttu-id="e6480-111">Para recuperar e decodificar dados privados armazenados anteriormente, chame [**LsaRetrievePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaretrieveprivatedata).</span><span class="sxs-lookup"><span data-stu-id="e6480-111">To retrieve and decode previously stored private data, call [**LsaRetrievePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaretrieveprivatedata).</span></span> <span data-ttu-id="e6480-112">Observe que você não pode recuperar objetos de dados privados do computador; os objetos de computador podem ser recuperados somente pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="e6480-112">Note that you cannot retrieve machine private data objects; machine objects can be retrieved only by the operating system.</span></span>

<span data-ttu-id="e6480-113">Antes de poder armazenar ou recuperar dados privados, seu aplicativo deve obter um identificador para o objeto de [**política**](policy-object.md) local, conforme demonstrado na [abertura de um identificador de objeto de política](opening-a-policy-object-handle.md).</span><span class="sxs-lookup"><span data-stu-id="e6480-113">Before you can store or retrieve private data, your application must get a handle to the local [**Policy**](policy-object.md) object, as demonstrated in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span>

<span data-ttu-id="e6480-114">O exemplo a seguir cria um objeto de dados particular local.</span><span class="sxs-lookup"><span data-stu-id="e6480-114">The following example creates a local private data object.</span></span> <span data-ttu-id="e6480-115">Observe que a função InitLsaString converte uma cadeia de caracteres [*Unicode*](/windows/desktop/SecGloss/u-gly) em uma estrutura de [**cadeia de \_ \_ caracteres Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) .</span><span class="sxs-lookup"><span data-stu-id="e6480-115">Note that the function InitLsaString converts a [*Unicode*](/windows/desktop/SecGloss/u-gly) string to an [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structure.</span></span> <span data-ttu-id="e6480-116">O código para essa função é mostrado em [usando cadeias de caracteres de Unicode LSA](using-lsa-unicode-strings.md).</span><span class="sxs-lookup"><span data-stu-id="e6480-116">The code for this function is shown in [Using LSA Unicode Strings](using-lsa-unicode-strings.md).</span></span>


```C++
#include <windows.h>
#include <stdio.h>

BOOL CreatePrivateDataObject(LSA_HANDLE PolicyHandle)
{
  NTSTATUS ntsResult;
  LSA_UNICODE_STRING lucKeyName;
  LSA_UNICODE_STRING lucPrivateData;
  // The L$ prefix specifies a local private data object
  WCHAR wszKeyName[] = L"L$MyPrivateKey";
  WCHAR wszPrivateData[] = L"Something secret.";

  // Initializing PLSA_UNICODE_STRING structures
  if (!InitLsaString(&lucKeyName, wszKeyName))
  {
         wprintf(L"Failed InitLsaString\n");
         return FALSE;
  }
  if (!InitLsaString(&lucPrivateData, wszPrivateData))
  {
         wprintf(L"Failed InitLsaString\n");
         return FALSE;
  }

  // Store the private data.
  ntsResult = LsaStorePrivateData(
    PolicyHandle,   // handle to a Policy object
    &lucKeyName,    // key to identify the data
    &lucPrivateData // the private data
  );
  if (ntsResult != STATUS_SUCCESS)
  {
    wprintf(L"Store private object failed %lu\n",
      LsaNtStatusToWinError(ntsResult));
    return FALSE;
  }
  return TRUE;
}
```



> [!Note]  
> <span data-ttu-id="e6480-117">Os dados armazenados pela função [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) não são absolutamente protegidos.</span><span class="sxs-lookup"><span data-stu-id="e6480-117">The data stored by the [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) function is not absolutely protected.</span></span> <span data-ttu-id="e6480-118">No entanto, a chave tem uma DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) que permite que apenas o criador e os administradores leiam os dados.</span><span class="sxs-lookup"><span data-stu-id="e6480-118">The key, however, has a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) that allows only the creator and administrators to read the data.</span></span>

 

 

 
