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
# <a name="user-must-change-password-at-next-logon-winnt-provider"></a><span data-ttu-id="44ef6-107">O usuário deve alterar a senha no próximo logon (provedor WinNT)</span><span class="sxs-lookup"><span data-stu-id="44ef6-107">User Must Change Password at Next Logon (WinNT Provider)</span></span>

<span data-ttu-id="44ef6-108">Para habilitar essa opção, defina o atributo **PasswordExpired** do usuário como um (1).</span><span class="sxs-lookup"><span data-stu-id="44ef6-108">To enable this option, set the **PasswordExpired** attribute of the user to one (1).</span></span> <span data-ttu-id="44ef6-109">Definir esse atributo como zero (0) permite que o usuário faça logon sem alterar a senha.</span><span class="sxs-lookup"><span data-stu-id="44ef6-109">Setting this attribute to zero (0) enables the user to log on without changing the password.</span></span>

## <a name="example-1"></a><span data-ttu-id="44ef6-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="44ef6-110">Example 1</span></span>

<span data-ttu-id="44ef6-111">O exemplo de código a seguir mostra como definir a opção Alterar senha no próximo logon usando Visual Basic com ADSI.</span><span class="sxs-lookup"><span data-stu-id="44ef6-111">The following code example shows how to set the change password on next logon option using Visual Basic with ADSI.</span></span>


```VB
Set usr = GetObject("WinNT://Fabrikam/jeffsmith,user")
usr.Put "PasswordExpired", CLng(1)   ' User must change password.
usr.SetInfo
```



## <a name="example-2"></a><span data-ttu-id="44ef6-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="44ef6-112">Example 2</span></span>

<span data-ttu-id="44ef6-113">O exemplo de código a seguir mostra como definir a senha de alteração na próxima opção de logon usando C++ com ADSI.</span><span class="sxs-lookup"><span data-stu-id="44ef6-113">The following code example shows how to set the change password on next logon option using C++ with ADSI.</span></span>


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



 

 




