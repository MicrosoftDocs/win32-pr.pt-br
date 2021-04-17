---
title: Bloqueio de conta (provedor de WinNT)
description: Quando o número de tentativas de logon com falha for excedido, a conta de usuário ficará bloqueada durante o número de minutos especificado pelo atributo lockoutDuration.
ms.assetid: d7c4134a-0712-4809-83ec-cc09e87afae9
ms.tgt_platform: multiple
keywords:
- Bloqueio de conta ADSI, provedor de WinNT
- ADSI do provedor WinNT, exemplos de gerenciamento de usuário, bloqueio de conta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ffeacb18b42beeb20b4af8bf571e611a85ab118
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105755485"
---
# <a name="account-lockout-winnt-provider"></a>Bloqueio de conta (provedor de WinNT)

Quando o número de tentativas de logon com falha for excedido, a conta de usuário ficará bloqueada durante o número de minutos especificado pelo atributo [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) . A propriedade [**IADsUser. IsAccountLocked**](iadsuser-property-methods.md) parece ser a propriedade a ser usada para ler e modificar o estado de bloqueio de uma conta de usuário, mas o provedor ADSI do Winnt tem restrições que limitam o uso da propriedade **IsAccountLocked** .

## <a name="resetting-the-account-lockout-status"></a>Redefinindo o status de bloqueio da conta

Ao usar o provedor WinNT, a propriedade [**IsAccountLocked**](iadsuser-property-methods.md) só pode ser definida como **false**, o que desbloqueia a conta. A tentativa de definir a propriedade **IsAccountLocked** como **true** falhará. Somente o sistema pode bloquear uma conta.

O exemplo de código a seguir demonstra como usar Visual Basic com ADSI para desbloquear uma conta de usuário.


```VB
Public Sub UnlockAccount(AccountDN As String)
    Dim usr As IADsUser
    
    ' Bind to the user account.
    Set usr = GetObject("WinNT://" + AccountDN)
    
    ' Set the IsAccountLocked property to False
    usr.IsAccountLocked = False
    
    ' Flush the cached attributes to the server.
    usr.SetInfo
End Sub
```



O exemplo de código a seguir demonstra como usar o C++ com ADSI para desbloquear uma conta de usuário.


```C++
HRESULT UnlockAccount(LPCWSTR pwszUserDN)
{
    if(!pwszUserDN)
    {
        return E_INVALIDARG;
    }

    // Build the ADsPath.
    CComBSTR sbstr = "WinNT://";
    sbstr += pwszUserDN;
    
    HRESULT hr;
    CComPtr<IADsUser> spADsUser;

    // Bind to the object.
    hr = ADsOpenObject(sbstr,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IADsUser,
        (void**)&spADsUser);
    if(S_OK != hr)
    {
        return hr;
    }
    
    // Set the IsAccountLocked property to FALSE;
    hr = spADsUser->put_IsAccountLocked(VARIANT_FALSE);

    // Commit the changes to the server.
    hr = spADsUser->SetInfo();

    return hr;
}
```



## <a name="reading-the-account-lockout-status"></a>Lendo o status de bloqueio da conta

Com o provedor WinNT, a propriedade [**IsAccountLocked**](iadsuser-property-methods.md) pode ser usada para determinar se uma conta está bloqueada. Se uma conta estiver bloqueada, a propriedade **IsAccountLocked** conterá **true**. Se uma conta não estiver bloqueada, a propriedade **IsAccountLocked** conterá **false**.

O exemplo de código a seguir demonstra como usar Visual Basic com ADSI para determinar se uma conta está bloqueada.


```VB
Public Function IsAccountLocked(AccountDN As String) As Boolean
    Dim oUser As IADsUser
    
    ' Bind to the object.
    Set oUser = GetObject("WinNT://" + AccountDN)
    
    ' Get the IsAccountLocked property.
    IsAccountLocked = oUser.IsAccountLocked
End Function
```



O exemplo de código a seguir demonstra como usar C++ com ADSI para determinar se uma conta está bloqueada.


```C++
HRESULT IsAccountLocked(LPCWSTR pwszUserDN, BOOL *pfLocked)
{
    if(!pwszUserDN || !pfLocked)
    {
        return E_INVALIDARG;
    }

    *pfLocked = FALSE;

    // Build the ADsPath.
    CComBSTR sbstr = "WinNT://";
    sbstr += pwszUserDN;
    
    HRESULT hr;
    CComPtr<IADsUser> spADsUser;

    // Bind to the object.
    hr = ADsOpenObject(sbstr,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IADsUser,
        (void**)&spADsUser);
    if(S_OK != hr)
    {
        return hr;
    }
    
    VARIANT_BOOL vfLocked;
    hr = spADsUser>get_IsAccountLocked(&vfLocked);
    if(S_OK != hr)
    {
        return hr;
    }

    *pfLocked = (vfLocked != 0);

    return hr;
}
```



 

 