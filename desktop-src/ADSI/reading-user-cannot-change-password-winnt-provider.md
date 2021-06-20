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
# <a name="reading-user-cannot-change-password-winnt-provider"></a><span data-ttu-id="2c221-107">O usuário de leitura não pode alterar a senha (provedor WinNT)</span><span class="sxs-lookup"><span data-stu-id="2c221-107">Reading User Cannot Change Password (WinNT Provider)</span></span>

<span data-ttu-id="2c221-108">A capacidade de um usuário alterar sua própria senha é uma permissão que pode ser concedida ou negada.</span><span class="sxs-lookup"><span data-stu-id="2c221-108">The ability of a user to change their own password is a permission that can be granted or denied.</span></span> <span data-ttu-id="2c221-109">Para determinar se o usuário recebeu essa permissão com o provedor WinNT, leia o sinalizador **\_ ADS UF \_ PASSWD \_ CANT \_ CHANGE** da propriedade **userFlags** do objeto de usuário.</span><span class="sxs-lookup"><span data-stu-id="2c221-109">To determine if the user has been granted this permission with the WinNT provider, read the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag of the **userFlags** property of the user object.</span></span> <span data-ttu-id="2c221-110">O **sinalizador ADS UF \_ \_ PASSWD \_ CANT \_ CHANGE** é definido na [**enumeração ENUM do SINALIZADOR \_ DE USUÁRIO \_ \_ ADS.**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum)</span><span class="sxs-lookup"><span data-stu-id="2c221-110">The **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag is defined in the [**ADS\_USER\_FLAG\_ENUM**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum) enumeration.</span></span>

## <a name="example-code"></a><span data-ttu-id="2c221-111">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="2c221-111">Example Code</span></span>

<span data-ttu-id="2c221-112">O exemplo de código a seguir mostra como obter o sinalizador **\_ ADS UF \_ PASSWD \_ CANT \_ CHANGE** da **propriedade userFlags** de um objeto de usuário.</span><span class="sxs-lookup"><span data-stu-id="2c221-112">The following code example shows how to obtain the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag of the **userFlags** property of a user object.</span></span>


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



<span data-ttu-id="2c221-113">O exemplo de código a seguir mostra como obter o sinalizador **\_ ADS UF \_ PASSWD \_ CANT \_ CHANGE** da **propriedade userFlags** de um objeto de usuário.</span><span class="sxs-lookup"><span data-stu-id="2c221-113">The following code example shows how to obtain the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag of the **userFlags** property of a user object.</span></span>


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



 

 




