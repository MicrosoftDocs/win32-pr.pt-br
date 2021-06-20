---
title: Modificar o usuário não pode alterar a senha (provedor WinNT)
description: Saiba como negar a um usuário a permissão para alterar uma senha para o provedor WinNT. A capacidade de um usuário alterar sua própria senha pode ser concedida ou negada.
ms.assetid: 071a817b-087e-49ee-af1a-6f190493cac0
ms.tgt_platform: multiple
keywords:
- Modificar o usuário não pode alterar a senha (provedor WinNT)
- O usuário não pode alterar a senha (provedor WinNT), modificando
- ADSI do provedor WinNT, exemplos de gerenciamento de usuário, o usuário não pode alterar a senha, modificando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33510fa36285fa49a413b84d91e29f8d5a367622
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408089"
---
# <a name="modifying-user-cannot-change-password-winnt-provider"></a><span data-ttu-id="4cbcd-107">Modificar o usuário não pode alterar a senha (provedor WinNT)</span><span class="sxs-lookup"><span data-stu-id="4cbcd-107">Modifying User Cannot Change Password (WinNT Provider)</span></span>

<span data-ttu-id="4cbcd-108">A capacidade de um usuário alterar sua própria senha é uma permissão que pode ser concedida ou negada.</span><span class="sxs-lookup"><span data-stu-id="4cbcd-108">The ability of a user to change their own password is a permission that can be granted or denied.</span></span> <span data-ttu-id="4cbcd-109">Para negar essa permissão, adicione o sinalizador da **UF do ADS \_ passwd não \_ \_ \_ alterar** para a propriedade **UserFlags** do objeto de usuário.</span><span class="sxs-lookup"><span data-stu-id="4cbcd-109">To deny this permission, add the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag to the **userFlags** property of the user object.</span></span> <span data-ttu-id="4cbcd-110">Para conceder essa permissão, remova o sinalizador da **UF do ADS \_ passwd não \_ \_ \_ alterar** , da propriedade **UserFlags** do objeto de usuário.</span><span class="sxs-lookup"><span data-stu-id="4cbcd-110">To grant this permission, remove the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag from the **userFlags** property of the user object.</span></span>

## <a name="example-code"></a><span data-ttu-id="4cbcd-111">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="4cbcd-111">Example Code</span></span>

<span data-ttu-id="4cbcd-112">O exemplo de código a seguir mostra como alterar o sinalizador da **UF do ADS \_ passwd não \_ \_ \_ alterar** , da propriedade **UserFlags** de um objeto de usuário.</span><span class="sxs-lookup"><span data-stu-id="4cbcd-112">The following code example shows how to change the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag of the **userFlags** property of a user object.</span></span>


```VB
Const ADS_UF_PASSWD_CANT_CHANGE = &H40

Sub SetUserCannotChangePassword(strDomain As String, strUser As String, strUserCred As String, strPassword As String, fUserCannotChangePassword As Boolean)
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
    
    lUserFlags = oUser.Get("userFlags")
    
    If fUserCannotChangePassword Then
        lUserFlags = lUserFlags Or ADS_UF_PASSWD_CANT_CHANGE
    Else
        lUserFlags = lUserFlags And Not ADS_UF_PASSWD_CANT_CHANGE
    End If
    
    ' Modify the userFlags property.
    oUser.Put "userFlags", lUserFlags
    
    ' Commit the changes to the server.
    oUser.SetInfo
End Sub
```



<span data-ttu-id="4cbcd-113">O exemplo de código a seguir mostra como alterar o sinalizador da **UF do ADS \_ passwd não \_ \_ \_ alterar** , da propriedade **UserFlags** de um objeto de usuário.</span><span class="sxs-lookup"><span data-stu-id="4cbcd-113">The following code example shows how to change the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag of the **userFlags** property of a user object.</span></span>


```C++
//***************************************************************************
//  SetUserCannotChangePassword()
//***************************************************************************

HRESULT SetUserCannotChangePassword(LPCWSTR pwszDomain,
                                    LPCWSTR pwszUser, 
                                    LPCWSTR pwszUserCred, 
                                    LPCWSTR pwszPassword,
                                    BOOL fCannotChangePassword)
{
    if(NULL == pwszDomain || 
        NULL == pwszUser)
    {
        return E_INVALIDARG;
    }
    
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
        CComBSTR sbstrPropName = "userFlags";
        CComVariant svar;
        
        hr = pads->Get(sbstrPropName, &svar);
        if(SUCCEEDED(hr))
        {
            if(fCannotChangePassword)
            {
                svar.lVal |= ADS_UF_PASSWD_CANT_CHANGE;
            }
            else
            {
                svar.lVal &= ~ADS_UF_PASSWD_CANT_CHANGE;
            }

            // Perform the change.
            hr = pads->Put(sbstrPropName, svar);

            // Commit the change.
            hr = pads->SetInfo();
        }
        
        pads->Release();
    }

    return hr;
}
```



 

 




