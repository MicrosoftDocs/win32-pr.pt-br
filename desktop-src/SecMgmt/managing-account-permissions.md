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
# <a name="managing-account-permissions"></a>Gerenciando permissões de conta

O LSA fornece várias funções que os aplicativos podem chamar para enumerar ou definir [*privilégios*](/windows/desktop/SecGloss/p-gly) para contas de usuário, grupo e grupo local.

Antes de poder gerenciar as informações da conta, seu aplicativo deve obter um identificador para o objeto de [**política**](policy-object.md) local, conforme demonstrado na [abertura de um identificador de objeto de política](opening-a-policy-object-handle.md). Além disso, para enumerar ou editar permissões para uma conta, você deve ter o Sid ( [*identificador de segurança*](/windows/desktop/SecGloss/s-gly) ) para essa conta. Seu aplicativo pode localizar um SID dado o nome da conta, conforme descrito em [conversão entre nomes e SIDs](translating-between-names-and-sids.md).

Para acessar todas as contas que têm uma permissão específica, chame [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright). Essa função popula uma matriz com os SIDs de todas as contas que têm a permissão especificada.

Depois de obter o SID de uma conta, você pode modificar suas permissões. Chame [**LsaAddAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights) para adicionar permissões à conta. Se a conta especificada não existir, o **LsaAddAccountRights** a criará. Para remover permissões de uma conta, chame [**LsaRemoveAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights). Se você remover todas as permissões de uma conta, o **LsaRemoveAccountRights** também excluirá a conta.

Seu aplicativo pode verificar as permissões atualmente atribuídas a uma conta chamando [**LsaEnumerateAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights). Essa função popula uma matriz de estruturas [**de \_ \_ cadeia de caracteres Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) . Cada estrutura contém o nome de um privilégio mantido pela conta especificada.

O exemplo a seguir adiciona a permissão SeServiceLogonRight a uma conta. Neste exemplo, a variável AccountId especifica o SID da conta. Para obter mais informações sobre como pesquisar um SID de conta, consulte [convertendo entre nomes e SIDs](translating-between-names-and-sids.md).


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



No exemplo anterior, a função InitLsaString converte uma cadeia de caracteres [*Unicode*](/windows/desktop/SecGloss/u-gly) em uma estrutura de [**cadeia de \_ \_ caracteres Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) . O código para essa função é mostrado em [usando cadeias de caracteres de Unicode LSA](using-lsa-unicode-strings.md).

 

 
