---
title: Expiração da conta (provedor LDAP)
description: Para definir a data de expiração da conta, de definido a propriedade IADsUser.AccountExpirationDate como o valor de data desejado.
ms.assetid: d0b90bb3-ad7c-4394-956d-061a915f210d
ms.tgt_platform: multiple
keywords:
- ADSI de expiração da conta, provedor LDAP
- ADSI do provedor LDAP, exemplos de gerenciamento de usuário, Expiração da Conta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645ce5e2e1ae72ace0a8a642642eb5c15e7eabd63d51dba3f03596869bfb9efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024064"
---
# <a name="account-expiration-ldap-provider"></a>Expiração da conta (provedor LDAP)

Para definir a data de expiração da conta, de definido a [**propriedade IADsUser.AccountExpirationDate**](iadsuser-property-methods.md) como o valor de data desejado. Para desabilitar a data de expiração da conta, de definir [**o atributo accountExpires**](/windows/desktop/ADSchema/a-accountexpires) como zero. Os exemplos de código a seguir mostram como definir a data de validade.


```VB
Public Sub SetUserAccountExpirationDate(User As IADsUser, ExpirationDate As Date)
    If 0 = ExpirationDate Then
        ' Disable the account expiration date.
        User.Put "accountExpires", 0
    Else
        ' Set the new account expiration date.
        User.AccountExpirationDate = ExpirationDate
    End If
    
    User.SetInfo
 
End Sub
```




```C++
/***************************************************************************

    SetUserAccountExpirationDate()

***************************************************************************/

HRESULT SetUserAccountExpirationDate(IADsUser *pUser, DATE date)
{
    if(!pUser) 
    {
        return E_INVALIDARG;
    }

    HRESULT hr;

    if(!date || date < 0) 
    {
        // Account never expires. Set the accountExpires attribute to zero.
        VARIANT var;
        VariantInit(&var);
        V_I4(&var) = 0;
        V_VT(&var) = VT_I4;
        
        hr = pUser->Put(CComBSTR("accountExpires"), var); 

        VariantClear(&var);
    }
    else 
    {
        // Account expires on date.
        hr = pUser->put_AccountExpirationDate(date); 
    }

    if(S_OK == hr)
    {
        hr = pUser->SetInfo();
    }

    return hr;
}
```



> [!Note]  
> O [**atributo accountExpires**](/windows/desktop/ADSchema/a-accountexpires) contém a data de expiração da conta. O Usuários e Computadores do Active Directory snap-in do MMC exibe a data em que a conta expirará no final. Ou seja, o Usuários e Computadores do Active Directory snap-in do MMC exibirá a data de expiração da conta como um dia antes da data contida no atributo **accountExpires.**

 

 

 