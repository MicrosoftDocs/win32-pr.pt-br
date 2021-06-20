---
title: O usuário de leitura não pode alterar a senha (provedor WinNT)
description: Saiba como determinar se um usuário tem permissão para alterar uma senha para o Provedor WinNT. A capacidade de um usuário alterar uma senha pode ser concedida ou negada.
ms.assetid: b8b8de00-0def-4506-ab73-d03a7e06256d
ms.tgt_platform: multiple
keywords:
- O usuário de leitura não pode alterar a senha (Provedor WinNT) ADSI
- O usuário não pode alterar a SENHA (Provedor WinNT) ADSI, lendo
- ADSI do provedor WinNT, exemplos de gerenciamento de usuário, Usuário não pode alterar senha, leitura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd075bfb6700779b60f9e578a4e89957487a2646
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405909"
---
# <a name="reading-user-cannot-change-password-winnt-provider"></a>O usuário de leitura não pode alterar a senha (provedor WinNT)

A capacidade de um usuário alterar sua própria senha é uma permissão que pode ser concedida ou negada. Para determinar se o usuário recebeu essa permissão com o provedor WinNT, leia o sinalizador **\_ ADS UF \_ PASSWD \_ CANT \_ CHANGE** da propriedade **userFlags** do objeto de usuário. O **sinalizador ADS UF \_ \_ PASSWD \_ CANT \_ CHANGE** é definido na [**enumeração ENUM do SINALIZADOR \_ DE USUÁRIO \_ \_ ADS.**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum)

## <a name="example-code"></a>Código de exemplo

O exemplo de código a seguir mostra como obter o sinalizador **\_ ADS UF \_ PASSWD \_ CANT \_ CHANGE** da **propriedade userFlags** de um objeto de usuário.


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



O exemplo de código a seguir mostra como obter o sinalizador **\_ ADS UF \_ PASSWD \_ CANT \_ CHANGE** da **propriedade userFlags** de um objeto de usuário.


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



 

 




