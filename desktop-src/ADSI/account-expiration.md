---
title: Expiração da conta (provedor LDAP)
description: Para definir a data de expiração da conta, defina a propriedade IADsUser. AccountExpirationDate para o valor de data desejado.
ms.assetid: d0b90bb3-ad7c-4394-956d-061a915f210d
ms.tgt_platform: multiple
keywords:
- ADSI de expiração da conta, provedor LDAP
- ADSI do provedor LDAP, exemplos de gerenciamento de usuário, expiração de conta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c03ea33d8d5abb219c2b562aa05058b5dec45919
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105771727"
---
# <a name="account-expiration-ldap-provider"></a><span data-ttu-id="dc5a9-105">Expiração da conta (provedor LDAP)</span><span class="sxs-lookup"><span data-stu-id="dc5a9-105">Account Expiration (LDAP Provider)</span></span>

<span data-ttu-id="dc5a9-106">Para definir a data de expiração da conta, defina a propriedade [**IADsUser. AccountExpirationDate**](iadsuser-property-methods.md) para o valor de data desejado.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-106">To set the account expiration date, set the [**IADsUser.AccountExpirationDate**](iadsuser-property-methods.md) property to the desired date value.</span></span> <span data-ttu-id="dc5a9-107">Para desabilitar a data de expiração da conta, defina o atributo [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) como zero.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-107">To disable the account expiration date, set the [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) attribute to zero.</span></span> <span data-ttu-id="dc5a9-108">Os exemplos de código a seguir mostram como definir a data de validade.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-108">The following code examples show how to set the expiration date.</span></span>


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
> <span data-ttu-id="dc5a9-109">O atributo [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) contém a data de expiração da conta.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-109">The [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) attribute contains the account expire date.</span></span> <span data-ttu-id="dc5a9-110">O snap-in Active Directory usuários e computadores do MMC exibe a data em que a conta irá expirar no final de.</span><span class="sxs-lookup"><span data-stu-id="dc5a9-110">The Active Directory Users and Computers MMC snap-in displays the date that the account will expire at the end of.</span></span> <span data-ttu-id="dc5a9-111">Ou seja, o snap-in do MMC Active Directory usuários e computadores exibirá a data de expiração da conta como um dia anterior à data contida no atributo **accountExpires** .</span><span class="sxs-lookup"><span data-stu-id="dc5a9-111">That is, the Active Directory Users and Computers MMC snap-in will display the account expiration date as one day earlier than the date contained in the **accountExpires** attribute.</span></span>

 

 

 