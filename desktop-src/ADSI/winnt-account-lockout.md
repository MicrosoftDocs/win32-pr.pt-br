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
# <a name="account-lockout-winnt-provider"></a><span data-ttu-id="499e5-105">Bloqueio de conta (provedor de WinNT)</span><span class="sxs-lookup"><span data-stu-id="499e5-105">Account Lockout (WinNT Provider)</span></span>

<span data-ttu-id="499e5-106">Quando o número de tentativas de logon com falha for excedido, a conta de usuário ficará bloqueada durante o número de minutos especificado pelo atributo [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) .</span><span class="sxs-lookup"><span data-stu-id="499e5-106">When the number of failed logon attempts is exceeded, the user account becomes locked out for the number of minutes specified by the [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) attribute.</span></span> <span data-ttu-id="499e5-107">A propriedade [**IADsUser. IsAccountLocked**](iadsuser-property-methods.md) parece ser a propriedade a ser usada para ler e modificar o estado de bloqueio de uma conta de usuário, mas o provedor ADSI do Winnt tem restrições que limitam o uso da propriedade **IsAccountLocked** .</span><span class="sxs-lookup"><span data-stu-id="499e5-107">The [**IADsUser.IsAccountLocked**](iadsuser-property-methods.md) property appears to be the property to use to read and modify the lockout state of a user account, but the WinNT ADSI provider has restrictions that limit the use of the **IsAccountLocked** property.</span></span>

## <a name="resetting-the-account-lockout-status"></a><span data-ttu-id="499e5-108">Redefinindo o status de bloqueio da conta</span><span class="sxs-lookup"><span data-stu-id="499e5-108">Resetting the Account Lockout Status</span></span>

<span data-ttu-id="499e5-109">Ao usar o provedor WinNT, a propriedade [**IsAccountLocked**](iadsuser-property-methods.md) só pode ser definida como **false**, o que desbloqueia a conta.</span><span class="sxs-lookup"><span data-stu-id="499e5-109">When using the WinNT provider, the [**IsAccountLocked**](iadsuser-property-methods.md) property can only be set to **FALSE**, which unlocks the account.</span></span> <span data-ttu-id="499e5-110">A tentativa de definir a propriedade **IsAccountLocked** como **true** falhará.</span><span class="sxs-lookup"><span data-stu-id="499e5-110">Attempting to set the **IsAccountLocked** property to **TRUE** will fail.</span></span> <span data-ttu-id="499e5-111">Somente o sistema pode bloquear uma conta.</span><span class="sxs-lookup"><span data-stu-id="499e5-111">Only the system can lock an account.</span></span>

<span data-ttu-id="499e5-112">O exemplo de código a seguir demonstra como usar Visual Basic com ADSI para desbloquear uma conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="499e5-112">The following code example demonstrates how to use Visual Basic with ADSI to unlock a user account.</span></span>


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



<span data-ttu-id="499e5-113">O exemplo de código a seguir demonstra como usar o C++ com ADSI para desbloquear uma conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="499e5-113">The following code example demonstrates how to use C++ with ADSI to unlock a user account.</span></span>


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



## <a name="reading-the-account-lockout-status"></a><span data-ttu-id="499e5-114">Lendo o status de bloqueio da conta</span><span class="sxs-lookup"><span data-stu-id="499e5-114">Reading the Account Lockout Status</span></span>

<span data-ttu-id="499e5-115">Com o provedor WinNT, a propriedade [**IsAccountLocked**](iadsuser-property-methods.md) pode ser usada para determinar se uma conta está bloqueada. Se uma conta estiver bloqueada, a propriedade **IsAccountLocked** conterá **true**.</span><span class="sxs-lookup"><span data-stu-id="499e5-115">With the WinNT provider, the [**IsAccountLocked**](iadsuser-property-methods.md) property can be used to determine if an account is locked out. If an account is locked out, the **IsAccountLocked** property will contain **TRUE**.</span></span> <span data-ttu-id="499e5-116">Se uma conta não estiver bloqueada, a propriedade **IsAccountLocked** conterá **false**.</span><span class="sxs-lookup"><span data-stu-id="499e5-116">If an account is not locked out, the **IsAccountLocked** property will contain **FALSE**.</span></span>

<span data-ttu-id="499e5-117">O exemplo de código a seguir demonstra como usar Visual Basic com ADSI para determinar se uma conta está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="499e5-117">The following code example demonstrates how to use Visual Basic with ADSI to determine if an account is locked out.</span></span>


```VB
Public Function IsAccountLocked(AccountDN As String) As Boolean
    Dim oUser As IADsUser
    
    ' Bind to the object.
    Set oUser = GetObject("WinNT://" + AccountDN)
    
    ' Get the IsAccountLocked property.
    IsAccountLocked = oUser.IsAccountLocked
End Function
```



<span data-ttu-id="499e5-118">O exemplo de código a seguir demonstra como usar C++ com ADSI para determinar se uma conta está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="499e5-118">The following code example demonstrates how to use C++ with ADSI to determine if an account is locked out.</span></span>


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



 

 