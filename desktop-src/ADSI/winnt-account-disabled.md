---
title: Conta desabilitada (provedor de WinNT)
description: Ao usar o provedor WinNT, uma conta pode ser habilitada ou desabilitada usando a propriedade IADsUser. AccountDisabled.
ms.assetid: a3d855cc-5e3d-49c2-b61e-3b35064002ea
ms.tgt_platform: multiple
keywords:
- Conta desabilitada (provedor de WinNT)
- Conta desabilitada ADSI, provedor de WinNT
- ADSI do provedor WinNT, exemplos de gerenciamento de usuário, conta desabilitada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a99b1fe45b71eda14547703f8721b2a13d581b8e
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104370908"
---
# <a name="account-disabled-winnt-provider"></a>Conta desabilitada (provedor de WinNT)

Ao usar o provedor WinNT, uma conta pode ser habilitada ou desabilitada usando a propriedade [**IADsUser. AccountDisabled**](iadsuser-property-methods.md) .

## <a name="example-1"></a>Exemplo 1

O exemplo de código a seguir mostra como desabilitar uma conta usando Visual Basic com ADSI.


```VB
Dim usr as IADsUser
On Error GoTo Cleanup

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
usr.AccountDisabled = TRUE ' Disable the account.
usr.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



## <a name="example-2"></a>Exemplo 2

O exemplo de código a seguir mostra como desabilitar uma conta usando C++ com ADSI.


```C++
IADsUser *pUser;

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath=L"WinNT://Fabrikam/JeffSmith";
hr = ADsGetObject(adsPath, IID_IADsUser, (void**)&pUser);

hr = pUser->put_AccountDisabled(TRUE);
hr = pUser->SetInfo();
```



 

 




