---
description: O LSA fornece várias funções que os aplicativos podem chamar para enumerar ou definir privilégios para contas de usuário, grupo e grupo local.
ms.assetid: c28c03f0-4638-42ed-8dad-1e934cf99273
title: Gerenciando permissões de conta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4dc22a4088986abbdaa98d8cdde43415af84905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461026"
---
# <a name="managing-account-permissions"></a><span data-ttu-id="c254f-103">Gerenciando permissões de conta</span><span class="sxs-lookup"><span data-stu-id="c254f-103">Managing Account Permissions</span></span>

<span data-ttu-id="c254f-104">O LSA fornece várias funções que os aplicativos podem chamar para enumerar ou definir [*privilégios*](/windows/desktop/SecGloss/p-gly) para contas de usuário, grupo e grupo local.</span><span class="sxs-lookup"><span data-stu-id="c254f-104">The LSA provides several functions that applications can call to enumerate or set [*privileges*](/windows/desktop/SecGloss/p-gly) for user, group, and local group accounts.</span></span>

<span data-ttu-id="c254f-105">Antes de poder gerenciar as informações da conta, seu aplicativo deve obter um identificador para o objeto de [**política**](policy-object.md) local, conforme demonstrado na [abertura de um identificador de objeto de política](opening-a-policy-object-handle.md).</span><span class="sxs-lookup"><span data-stu-id="c254f-105">Before you can manage account information, your application must get a handle to the local [**Policy**](policy-object.md) object, as demonstrated in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span> <span data-ttu-id="c254f-106">Além disso, para enumerar ou editar permissões para uma conta, você deve ter o Sid ( [*identificador de segurança*](/windows/desktop/SecGloss/s-gly) ) para essa conta.</span><span class="sxs-lookup"><span data-stu-id="c254f-106">In addition, to enumerate or edit permissions for an account, you must have the [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) for that account.</span></span> <span data-ttu-id="c254f-107">Seu aplicativo pode localizar um SID dado o nome da conta, conforme descrito em [conversão entre nomes e SIDs](translating-between-names-and-sids.md).</span><span class="sxs-lookup"><span data-stu-id="c254f-107">Your application can locate a SID given the account name, as described in [Translating Between Names and SIDs](translating-between-names-and-sids.md).</span></span>

<span data-ttu-id="c254f-108">Para acessar todas as contas que têm uma permissão específica, chame [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright).</span><span class="sxs-lookup"><span data-stu-id="c254f-108">To access all accounts that have a particular permission, call [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright).</span></span> <span data-ttu-id="c254f-109">Essa função popula uma matriz com os SIDs de todas as contas que têm a permissão especificada.</span><span class="sxs-lookup"><span data-stu-id="c254f-109">This function populates an array with the SIDs of all accounts that have the specified permission.</span></span>

<span data-ttu-id="c254f-110">Depois de obter o SID de uma conta, você pode modificar suas permissões.</span><span class="sxs-lookup"><span data-stu-id="c254f-110">After you have obtained the SID of an account, you can modify its permissions.</span></span> <span data-ttu-id="c254f-111">Chame [**LsaAddAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights) para adicionar permissões à conta.</span><span class="sxs-lookup"><span data-stu-id="c254f-111">Call [**LsaAddAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights) to add permissions to the account.</span></span> <span data-ttu-id="c254f-112">Se a conta especificada não existir, o **LsaAddAccountRights** a criará.</span><span class="sxs-lookup"><span data-stu-id="c254f-112">If the specified account does not exist, **LsaAddAccountRights** creates it.</span></span> <span data-ttu-id="c254f-113">Para remover permissões de uma conta, chame [**LsaRemoveAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights).</span><span class="sxs-lookup"><span data-stu-id="c254f-113">To remove permissions from an account, call [**LsaRemoveAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights).</span></span> <span data-ttu-id="c254f-114">Se você remover todas as permissões de uma conta, o **LsaRemoveAccountRights** também excluirá a conta.</span><span class="sxs-lookup"><span data-stu-id="c254f-114">If you remove all permissions from an account, **LsaRemoveAccountRights** also deletes the account.</span></span>

<span data-ttu-id="c254f-115">Seu aplicativo pode verificar as permissões atualmente atribuídas a uma conta chamando [**LsaEnumerateAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights).</span><span class="sxs-lookup"><span data-stu-id="c254f-115">Your application can check the permissions currently assigned to an account by calling [**LsaEnumerateAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights).</span></span> <span data-ttu-id="c254f-116">Essa função popula uma matriz de estruturas [**de \_ \_ cadeia de caracteres Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) .</span><span class="sxs-lookup"><span data-stu-id="c254f-116">This function populates an array of [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structures.</span></span> <span data-ttu-id="c254f-117">Cada estrutura contém o nome de um privilégio mantido pela conta especificada.</span><span class="sxs-lookup"><span data-stu-id="c254f-117">Each structure contains the name of a privilege held by the specified account.</span></span>

<span data-ttu-id="c254f-118">O exemplo a seguir adiciona a permissão SeServiceLogonRight a uma conta.</span><span class="sxs-lookup"><span data-stu-id="c254f-118">The following example adds the SeServiceLogonRight permission to an account.</span></span> <span data-ttu-id="c254f-119">Neste exemplo, a variável AccountId especifica o SID da conta.</span><span class="sxs-lookup"><span data-stu-id="c254f-119">In this example, the AccountSID variable specifies the SID of the account.</span></span> <span data-ttu-id="c254f-120">Para obter mais informações sobre como pesquisar um SID de conta, consulte [convertendo entre nomes e SIDs](translating-between-names-and-sids.md).</span><span class="sxs-lookup"><span data-stu-id="c254f-120">For more information about how to lookup an account SID, see [Translating Between Names and SIDs](translating-between-names-and-sids.md).</span></span>


```C++
#include <windows.h>
#include <ntsecapi.h>

void AddPrivileges(PSID AccountSID, LSA_HANDLE PolicyHandle)
{
  LSA_UNICODE_STRING lucPrivilege;
  NTSTATUS ntsResult;

  // Create an LSA_UNICODE_STRING for the privilege names.
  if (!InitLsaString(&lucPrivilege, L"SeServiceLogonRight"))
  {
         wprintf(L"Failed InitLsaString\n");
         return;
  }

  ntsResult = LsaAddAccountRights(
    PolicyHandle,  // An open policy handle.
    AccountSID,    // The target SID.
    &lucPrivilege, // The privileges.
    1              // Number of privileges.
  );                
  if (ntsResult == STATUS_SUCCESS) 
  {
    wprintf(L"Privilege added.\n");
  }
  else
  {
    wprintf(L"Privilege was not added - %lu \n",
      LsaNtStatusToWinError(ntsResult));
  }
} 
```



<span data-ttu-id="c254f-121">No exemplo anterior, a função InitLsaString converte uma cadeia de caracteres [*Unicode*](/windows/desktop/SecGloss/u-gly) em uma estrutura de [**cadeia de \_ \_ caracteres Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) .</span><span class="sxs-lookup"><span data-stu-id="c254f-121">In the preceding example, the function InitLsaString converts a [*Unicode*](/windows/desktop/SecGloss/u-gly) string to an [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structure.</span></span> <span data-ttu-id="c254f-122">O código para essa função é mostrado em [usando cadeias de caracteres de Unicode LSA](using-lsa-unicode-strings.md).</span><span class="sxs-lookup"><span data-stu-id="c254f-122">The code for this function is shown in [Using LSA Unicode Strings](using-lsa-unicode-strings.md).</span></span>

 

 
