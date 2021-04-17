---
title: O usuário deve alterar a senha no próximo logon (provedor WinNT)
description: Para habilitar essa opção, defina o atributo PasswordExpired do usuário como um (1). Definir esse atributo como zero (0) permite que o usuário faça logon sem alterar a senha.
ms.assetid: 97dd4232-dcd3-44bd-8a2a-1dcb0f85d53c
ms.tgt_platform: multiple
keywords:
- O usuário deve alterar a senha no próximo logon (provedor WinNT) ADSI
- O usuário deve alterar a senha no próximo logon ADSI, provedor de WinNT
- ADSI do provedor WinNT, exemplos de gerenciamento de usuário, o usuário deve alterar a senha no próximo logon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787be5f5f4e1534574a68c179bb699ac68c61e3e
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "105749156"
---
# <a name="user-must-change-password-at-next-logon-winnt-provider"></a>O usuário deve alterar a senha no próximo logon (provedor WinNT)

Para habilitar essa opção, defina o atributo **PasswordExpired** do usuário como um (1). Definir esse atributo como zero (0) permite que o usuário faça logon sem alterar a senha.

## <a name="example-1"></a>Exemplo 1

O exemplo de código a seguir mostra como definir a opção Alterar senha no próximo logon usando Visual Basic com ADSI.


```VB
Set usr = GetObject("WinNT://Fabrikam/jeffsmith,user")
usr.Put "PasswordExpired", CLng(1)   ' User must change password.
usr.SetInfo
```



## <a name="example-2"></a>Exemplo 2

O exemplo de código a seguir mostra como definir a senha de alteração na próxima opção de logon usando C++ com ADSI.


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



 

 




