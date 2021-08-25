---
title: A leitura do usuário não pode alterar a senha (provedor WinNT)
description: Saiba como determinar se um usuário tem permissão para alterar uma senha para o provedor WinNT. A capacidade de um usuário alterar uma senha pode ser concedida ou negada.
ms.assetid: b8b8de00-0def-4506-ab73-d03a7e06256d
ms.tgt_platform: multiple
keywords:
- A leitura do usuário não pode alterar a senha (provedor WinNT) ADSI
- O usuário não pode alterar a senha (provedor WinNT) ADSI, lendo
- ADSI do provedor WinNT, exemplos de gerenciamento de usuário, o usuário não pode alterar a senha, lendo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 761a1ef0a332f1cdfd7dad1b20426b749618ed2286832c7ff16b207cee57c176
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637546"
---
# <a name="reading-user-cannot-change-password-winnt-provider"></a>A leitura do usuário não pode alterar a senha (provedor WinNT)

A capacidade de um usuário alterar sua própria senha é uma permissão que pode ser concedida ou negada. Para determinar se o usuário recebeu essa permissão com o provedor de WinNT, leia o sinalizador da UF do ADS passwd não é possível **\_ \_ \_ \_ alterar** a propriedade **UserFlags** do objeto user. O sinalizador da **UF do ADS \_ passwd não \_ \_ \_ alterar** é definido na enumeração enum do [**\_ \_ sinalizador \_ do usuário ADS**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum) .

## <a name="example-code"></a>Código de exemplo

O exemplo de código a seguir mostra como obter o sinalizador da UF de anúncios passwd não é possível **\_ \_ \_ \_ alterar** a propriedade **UserFlags** de um objeto de usuário.


```VB
Const ADS_UF_PASSWD_CANT_CHANGE = &H40

Function UserCannotChangePassword(strDomain As String, strUser As String, strUserCred As String, strPassword As String) As Boolean
    UserCannotChangePassword = False
    
    Dim oUser As IADs
    
    strPath = "WinNT://" + strDomain + "/" + strUser
    
    If "" <> strUserCred Then
        Dim dso As IADsOpenDSObject
        
        ' Bind to the group with the specified user name and password.
        Set dso = GetObject("WinNT:")
        Set oUser = dso.OpenDSObject(strPath, strUserCred, strPassword, 1)
    Else
        ' Bind to the group with the current credentials.
        Set oUser = GetObject(strPath)
    End If
    
    If (oUser.Get("userFlags") And ADS_UF_PASSWD_CANT_CHANGE) <> 0 Then
        UserCannotChangePassword = True
    Else
        UserCannotChangePassword = False
    End If
End Function
```



O exemplo de código a seguir mostra como obter o sinalizador da UF de anúncios passwd não é possível **\_ \_ \_ \_ alterar** a propriedade **UserFlags** de um objeto de usuário.


```C++
//***************************************************************************
//
//  UserCannotChangePassword()
//
//***************************************************************************

HRESULT UserCannotChangePassword(LPCWSTR pwszDomain, 
                                 LPCWSTR pwszUser, 
                                 LPCWSTR pwszUserCred, 
                                 LPCWSTR pwszPassword, 
                                 BOOL *pfCannotChangePassword)
{
    if(NULL == pwszDomain || NULL == pwszUser)
    {
        return E_INVALIDARG;
    }
    
    *pfCannotChangePassword = FALSE;

    HRESULT hr;
    IADs *pads;

    CComBSTR sbstrADsPath = L"WinNT://";
    sbstrADsPath += pwszDomain;
    sbstrADsPath += "/";
    sbstrADsPath += pwszUser;

    hr = ADsOpenObject( sbstrADsPath,
                        pwszUserCred,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs, 
                        (void**)&pads);

    if(SUCCEEDED(hr))
    {
        CComVariant svar;
        
        hr = pads->Get(CComBSTR("userFlags"), &svar);
        if(SUCCEEDED(hr))
        {
            if(ADS_UF_PASSWD_CANT_CHANGE & svar.lVal)
            {
                *pfCannotChangePassword = TRUE;
            }
            else
            {
                *pfCannotChangePassword = FALSE;
            }
        }
        
        pads->Release();
    }

    return hr;
}
```



 

 




