---
title: A senha nunca expira (provedor LDAP)
description: Para habilitar a opção a senha nunca expirar usando o provedor LDAP, defina o sinalizador de passwd da UF do ADS não \_ \_ \_ expirar \_ no atributo UserAccountControl do usuário.
ms.assetid: b8d7e7fe-c846-45c4-9c5f-770530453836
ms.tgt_platform: multiple
keywords:
- A senha nunca expira em ADSI, provedor LDAP
- ADSI do provedor LDAP, exemplos de gerenciamento de usuário, senha nunca expira
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94c0d9eb42d37c1bcc7d65495fa0d72609060407
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366707"
---
# <a name="password-never-expires-ldap-provider"></a><span data-ttu-id="66a93-105">A senha nunca expira (provedor LDAP)</span><span class="sxs-lookup"><span data-stu-id="66a93-105">Password Never Expires (LDAP Provider)</span></span>

<span data-ttu-id="66a93-106">Para habilitar a opção a senha nunca expirar usando o provedor LDAP, defina o sinalizador de [**passwd da UF do ADS não \_ \_ \_ expirar \_**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum) no atributo [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) do usuário.</span><span class="sxs-lookup"><span data-stu-id="66a93-106">To enable the password never expires option using the LDAP provider, set the [**ADS\_UF\_DONT\_EXPIRE\_PASSWD**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum) flag on the user [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) attribute.</span></span>


```VB
Const ADS_UF_DONT_EXPIRE_PASSWD = &H10000

Set usr = GetObject("LDAP://CN=jeffsmith,OU=Sales,DC=Fabrikam,DC=Com")
flag = usr.Get("userAccountControl")
newFlag = flag Or ADS_UF_DONT_EXPIRE_PASSWD
usr.Put "userAccountControl", newFlag
usr.SetInfo
```




```C++
#include <activeds.h>

IADsUser *pUser;
VARIANT var;
VariantInit(&var);

HRESULT hr = S_OK;
LPWSTR adsPath = L"LDAP://serv1/cn=Jeff Smith,cn=Users,dc=Fabrikam,dc=com";
hr = ADsGetObject(adsPath, IID_IADsUser, (void**)&pUser);

hr = pUser->Get(_bstr_t("userAccountControl"), &var);

V_I4(&var) |= ADS_UF_DONT_EXPIRE_PASSWD;
hr = pUser->Put(_bstr_t("userAccountControl"), var);

hr = pUser->SetInfo();
VariantClear(&var);
hr = pUser->Release();
```



 

 