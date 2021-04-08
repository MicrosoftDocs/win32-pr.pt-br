---
title: O usuário deve alterar a senha no próximo logon (provedor LDAP)
description: Para forçar um usuário a alterar sua senha no próximo logon, defina o atributo pwdLastSet como zero (0). Para remover esse requisito, defina o atributo pwdLastSet como-1. O atributo pwdLastSet não pode ser definido como qualquer outro valor, exceto pelo sistema.
ms.assetid: 0182151c-ddb7-4d08-98c6-c37e6e514cf0
ms.tgt_platform: multiple
keywords:
- O usuário deve alterar a senha no próximo logon ADSI, provedor LDAP
- ADSI do provedor LDAP, exemplos de gerenciamento de usuário, o usuário deve alterar a senha no próximo logon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 784ee0defbe3c8ec9abe2d110c2532b8c9688019
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004852"
---
# <a name="user-must-change-password-at-next-logon-ldap-provider"></a>O usuário deve alterar a senha no próximo logon (provedor LDAP)

Para forçar um usuário a alterar sua senha no próximo logon, defina o atributo **pwdLastSet** como zero (0). Para remover esse requisito, defina o atributo **pwdLastSet** como-1. O atributo **pwdLastSet** não pode ser definido como qualquer outro valor, exceto pelo sistema.

O exemplo de código a seguir mostra como definir a opção "o usuário deve alterar a senha no próximo logon".


```VB
Dim usr as IADs

Set usr = GetObject("LDAP://CN=Jeff Smith,OU=Sales,DC=Fabrikam,DC=Com")
usr.Put "pwdLastSet", CLng(0)
usr.SetInfo
```



O exemplo de código a seguir mostra como definir a opção "o usuário deve alterar a senha no próximo logon".


```C++
/***************************************************************************

    SetUserMustChangePassword()

***************************************************************************/

HRESULT SetUserMustChangePassword(LPCWSTR pwszUserADsPath, 
                                  LPCWSTR pwszUsername, 
                                  LPCWSTR pwszPassword)
{
    IADs *pUser;
    HRESULT hr;

    hr = ADsOpenObject(pwszUserADsPath,
                        pwszUsername,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs,
                        (void**)&pUser);

    if(SUCCEEDED(hr))
    {
        VARIANT var;
        VariantInit(&var);
        V_I4(&var) = 0;
        V_VT(&var) = VT_I4;
        hr = pUser->Put(CComBSTR("pwdLastSet"), var);
        hr = pUser->SetInfo();

        VariantClear(&var);
        pUser->Release();
    }

    return hr;
}
```



 

 




