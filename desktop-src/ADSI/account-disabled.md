---
title: Conta desabilitada (Provedor LDAP)
description: Para desabilitar uma conta de usuário, de definir a propriedade AccountDisabled como TRUE na interface IADsUser. Isso é semelhante ao provedor WinNT. Os exemplos de código a seguir mostram como desabilitar uma conta de usuário.
ms.assetid: 7911baa4-4178-47a9-80eb-11dc608a0ea3
ms.tgt_platform: multiple
keywords:
- ADSI desabilitado da conta, provedor LDAP
- ADSI do provedor LDAP, exemplos de gerenciamento de usuários, Conta Desabilitada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf753da0770e19504d496be20ba350f79bd4788a797eb5241e68261df844b626
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181440"
---
# <a name="account-disabled-ldap-provider"></a>Conta desabilitada (Provedor LDAP)

Para desabilitar uma conta de usuário, de definir a propriedade AccountDisabled **como TRUE** na interface [**IADsUser.**](/windows/desktop/api/Iads/nn-iads-iadsuser) Isso é semelhante ao provedor WinNT. Os exemplos de código a seguir mostram como desabilitar uma conta de usuário.

## <a name="example-1"></a>Exemplo 1


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



## <a name="example-2"></a>Exemplo 2


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



 

 




