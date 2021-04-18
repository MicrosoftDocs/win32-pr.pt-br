---
title: Conta desabilitada (provedor LDAP)
description: Para desabilitar uma conta de usuário, defina a propriedade AccountDisabled como TRUE na interface IADsUser. Isso é semelhante ao provedor WinNT. Os exemplos de código a seguir mostram como desabilitar uma conta de usuário.
ms.assetid: 7911baa4-4178-47a9-80eb-11dc608a0ea3
ms.tgt_platform: multiple
keywords:
- Conta desabilitada pelo ADSI, provedor LDAP
- ADSI do provedor LDAP, exemplos de gerenciamento de usuário, conta desabilitada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e61fb65a06f4e2afb1b43595b955c577b2a6090
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "105755905"
---
# <a name="account-disabled-ldap-provider"></a><span data-ttu-id="9ac83-107">Conta desabilitada (provedor LDAP)</span><span class="sxs-lookup"><span data-stu-id="9ac83-107">Account Disabled (LDAP Provider)</span></span>

<span data-ttu-id="9ac83-108">Para desabilitar uma conta de usuário, defina a propriedade AccountDisabled como **true** na interface [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) .</span><span class="sxs-lookup"><span data-stu-id="9ac83-108">To disable a user account, set the AccountDisabled property to **TRUE** in the [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) interface.</span></span> <span data-ttu-id="9ac83-109">Isso é semelhante ao provedor WinNT.</span><span class="sxs-lookup"><span data-stu-id="9ac83-109">This is similar to the WinNT provider.</span></span> <span data-ttu-id="9ac83-110">Os exemplos de código a seguir mostram como desabilitar uma conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="9ac83-110">The following code examples show how to disable a user account.</span></span>

## <a name="example-1"></a><span data-ttu-id="9ac83-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9ac83-111">Example 1</span></span>


```VB
Dim usr As IADsUser
On Error GoTo Cleanup

Set usr = GetObject("LDAP:// CN=JeffSmith, OU=Sales, DC=Fabrikam, DC=Com")
usr.AccountDisabled = TRUE ' Disable the account.
usr.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set usr = Nothing
```



## <a name="example-2"></a><span data-ttu-id="9ac83-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9ac83-112">Example 2</span></span>


```C++
IADsUser *pUser = NULL;

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath=L"LDAP://serv1/cn=Jeff Smith,cn=Users, dc=Fabrikam, dc=com";
hr = ADsGetObject(adsPath,IID_IADsUser,(void**)&pUser);

if(FAILED(hr)){return;}

hr = pUser->put_AccountDisabled(true);
hr = pUser->SetInfo();
```



 

 




