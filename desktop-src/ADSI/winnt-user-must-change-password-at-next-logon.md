---
title: O usuário deve alterar a senha no próximo logon (provedor WinNT)
description: Para habilitar essa opção, de definido o atributo PasswordExpired do usuário como um (1). Definir esse atributo como zero (0) permite que o usuário faça logoff sem alterar a senha.
ms.assetid: 97dd4232-dcd3-44bd-8a2a-1dcb0f85d53c
ms.tgt_platform: multiple
keywords:
- O usuário deve alterar a senha no próximo logon (Provedor WinNT) ADSI
- O usuário deve alterar a senha no próximo logon ADSI, provedor WinNT
- ADSI do provedor WinNT, exemplos de gerenciamento de usuário, Usuário deve alterar senha no próximo logon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be50e5cdccb4969e59a5b32516a35278b867062e8cced2e80d96b26c56c6173b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023034"
---
# <a name="user-must-change-password-at-next-logon-winnt-provider"></a>O usuário deve alterar a senha no próximo logon (provedor WinNT)

Para habilitar essa opção, de definido o atributo **PasswordExpired** do usuário como um (1). Definir esse atributo como zero (0) permite que o usuário faça logoff sem alterar a senha.

## <a name="example-1"></a>Exemplo 1

O exemplo de código a seguir mostra como definir a opção alterar senha na próxima opção de logon usando Visual Basic ADSI.


```VB
Set usr = GetObject("WinNT://Fabrikam/jeffsmith,user")
usr.Put "PasswordExpired", CLng(1)   ' User must change password.
usr.SetInfo
```



## <a name="example-2"></a>Exemplo 2

O exemplo de código a seguir mostra como definir a opção alterar senha na próxima opção de logon usando C++ com ADSI.


```C++
IADsUser *pUser = NULL;
HRESULT hr;

hr=ADsGetObject(L"WinNT://Fabrikam/jeffsmith,user",
                IID_IADsUser,
                (void**)&pUser);
VARIANT var;
VariantInit(&var);
V_I4(&var)=1;
V_VT(&var)=VT_I4;
hr = pUser->Put(_bstr_t("PasswordExpired"),var); // User must change password.
hr = pUser->SetInfo();

VariantClear(&var);
pUser->Release();
```



 

 




