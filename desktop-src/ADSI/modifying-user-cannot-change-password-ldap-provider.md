---
title: Modificar o usuário não pode alterar a senha (provedor LDAP)
description: A capacidade de um usuário alterar sua própria senha é uma permissão que pode ser concedida ou negada.
ms.assetid: 9d5c2d6a-9997-4d0c-b896-bf1b578e64ac
ms.tgt_platform: multiple
keywords:
- A modificação do usuário não pode alterar a senha (provedor LDAP) ADSI
- O usuário não pode alterar a senha (provedor LDAP) ADSI, modificando
- ADSI do provedor LDAP, exemplos de gerenciamento de usuário, o usuário deve alterar a senha no próximo logon, modificando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1628b113c2f15278bc72e41aa79e4be03a98f2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641843"
---
# <a name="modifying-user-cannot-change-password-ldap-provider"></a><span data-ttu-id="22d61-106">Modificar o usuário não pode alterar a senha (provedor LDAP)</span><span class="sxs-lookup"><span data-stu-id="22d61-106">Modifying User Cannot Change Password (LDAP Provider)</span></span>

<span data-ttu-id="22d61-107">A capacidade de um usuário alterar sua própria senha é uma permissão que pode ser concedida ou negada.</span><span class="sxs-lookup"><span data-stu-id="22d61-107">The ability of a user to change their own password is a permission that can be grant or denied.</span></span> <span data-ttu-id="22d61-108">Para negar essa permissão, defina duas ACEs na DACL (lista de controle de acesso discricionário) do descritor de segurança do objeto de usuário com o tipo de ACE de **\_ \_ objeto de acesso \_ negado \_ do ADS ACETYPE** .</span><span class="sxs-lookup"><span data-stu-id="22d61-108">To deny this permission, set two ACEs in the security descriptor discretionary access control list (DACL) of the user object with the **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT** ace type.</span></span> <span data-ttu-id="22d61-109">Uma ACE nega a permissão ao usuário e outra ACE nega a permissão ao grupo Everyone.</span><span class="sxs-lookup"><span data-stu-id="22d61-109">One ACE denies the permission to the user and another ACE denies the permission to the Everyone group.</span></span> <span data-ttu-id="22d61-110">As ACEs são ACEs de negação específicas de objeto que especificam o GUID da permissão estendida para a alteração de senhas.</span><span class="sxs-lookup"><span data-stu-id="22d61-110">Both ACEs are object-specific deny ACEs that specify the GUID of the extended permission for changing passwords.</span></span> <span data-ttu-id="22d61-111">Para conceder essa permissão, defina as mesmas ACEs com o tipo de ACE de **\_ \_ objeto de acesso \_ permitido \_ pelo ADS ACETYPE** .</span><span class="sxs-lookup"><span data-stu-id="22d61-111">To grant this permission, set the same ACEs with the **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** ace type.</span></span>

<span data-ttu-id="22d61-112">O procedimento a seguir descreve como modificar ou adicionar ACEs para essa permissão.</span><span class="sxs-lookup"><span data-stu-id="22d61-112">The following procedure describes how to modify or add ACEs for this permission.</span></span>

<span data-ttu-id="22d61-113">**Para modificar ou adicionar as ACEs para essa permissão**</span><span class="sxs-lookup"><span data-stu-id="22d61-113">**To modify or add the ACEs for this permission**</span></span>

1.  <span data-ttu-id="22d61-114">Associar ao objeto de usuário.</span><span class="sxs-lookup"><span data-stu-id="22d61-114">Bind to the user object.</span></span>
2.  <span data-ttu-id="22d61-115">Obtenha o objeto [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) da propriedade **ntSecurityDescriptor** do objeto de usuário.</span><span class="sxs-lookup"><span data-stu-id="22d61-115">Obtain the [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) object from the **ntSecurityDescriptor** property of the user object.</span></span>
3.  <span data-ttu-id="22d61-116">Obtenha uma interface [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist) para o descritor de segurança da propriedade [**IADsSecurityDescriptor. DiscretionaryAcl**](iadssecuritydescriptor-property-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="22d61-116">Obtain an [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist) interface for the security descriptor from the [**IADsSecurityDescriptor.DiscretionaryAcl**](iadssecuritydescriptor-property-methods.md) property.</span></span>
4.  <span data-ttu-id="22d61-117">Enumere as ACEs para o objeto e pesquise as ACEs que têm o GUID de alteração de senha ({AB721A53-1E2F-11D0-9819-00AA0040529B}) para a propriedade [**IADsAccessControlEntry. ObjectType**](iadsaccesscontrolentry-property-methods.md) e "Everyone" ou "NT Authority \\ self" para a propriedade **IADsAccessControlEntry. Trustee** .</span><span class="sxs-lookup"><span data-stu-id="22d61-117">Enumerate the ACEs for the object and search for the ACEs that have the change password GUID ({AB721A53-1E2F-11D0-9819-00AA0040529B}) for the [**IADsAccessControlEntry.ObjectType**](iadsaccesscontrolentry-property-methods.md) property and "Everyone" or "NT AUTHORITY\\SELF" for the **IADsAccessControlEntry.Trustee** property.</span></span>

    > [!Note]  
    > <span data-ttu-id="22d61-118">As cadeias de caracteres "todos" e "auto-Autoridade NT \\ " são localizadas com base no idioma do primeiro controlador de domínio no domínio.</span><span class="sxs-lookup"><span data-stu-id="22d61-118">The "Everyone" and "NT AUTHORITY\\SELF" strings are localized based on the language of the first domain controller in the domain.</span></span> <span data-ttu-id="22d61-119">Por isso, as cadeias de caracteres não devem ser usadas diretamente.</span><span class="sxs-lookup"><span data-stu-id="22d61-119">Because of this, the strings should not be used directly.</span></span> <span data-ttu-id="22d61-120">Os nomes de conta devem ser obtidos em tempo de execução chamando a função [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) com o Sid para "Everyone" ("s-1-1-0") e "NT Authority \\ self" ("S-1-5-10") entidades de segurança bem conhecidas.</span><span class="sxs-lookup"><span data-stu-id="22d61-120">The account names should be obtained at run time by calling the [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) function with the SID for "Everyone" ("S-1-1-0") and "NT AUTHORITY\\SELF" ("S-1-5-10") well-known security principals.</span></span> <span data-ttu-id="22d61-121">As funções de exemplo **GetSidAccountName**, **GetSidAccountName \_ Everyone** e **GetSidAccountName \_ Self** C++ mostradas em [lendo usuário não podem alterar a senha (provedor LDAP)](reading-user-cannot-change-password-ldap-provider.md) demonstre como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="22d61-121">The **GetSidAccountName**, **GetSidAccountName\_Everyone**, and **GetSidAccountName\_Self** C++ example functions shown in [Reading User Cannot Change Password (LDAP Provider)](reading-user-cannot-change-password-ldap-provider.md) demonstrate how to do this.</span></span>

     

5.  <span data-ttu-id="22d61-122">Modifique a propriedade [**IADsAccessControlEntry. AceType**](iadsaccesscontrolentry-property-methods.md) das ACEs que foram encontradas para o **\_ objeto ADS AceType \_ acesso \_ negado \_** se o usuário não puder alterar sua senha ou se o **ADS \_ AceType acessar o \_ \_ \_ objeto permitido** se o usuário puder alterar sua senha.</span><span class="sxs-lookup"><span data-stu-id="22d61-122">Modify the [**IADsAccessControlEntry.AceType**](iadsaccesscontrolentry-property-methods.md) property of the ACEs that were found to **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT** if the user cannot change their password or **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** if the user can change their password.</span></span>
6.  <span data-ttu-id="22d61-123">Se a ACE "Everyone" não for encontrada, crie um novo objeto [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) que contenha os valores de propriedade mostrados na tabela abaixo e adicione a nova entrada à ACL com o método [**IADsAccessControlList. AddAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace) .</span><span class="sxs-lookup"><span data-stu-id="22d61-123">If the "Everyone" ACE is not found, create a new [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) object that contains the property values shown in the table below and add the new entry to the ACL with the [**IADsAccessControlList.AddAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace) method.</span></span>
7.  <span data-ttu-id="22d61-124">Se a ACE "NT AUTHORITY \\ self" não for encontrada, crie um novo objeto [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) com os mesmos valores de propriedade mostrados na tabela abaixo, exceto que a propriedade [**Trustee**](iadsaccesscontrolentry-property-methods.md) contiver o nome da conta para o Sid "S-1-5-10" (" \\ auto Authority self").</span><span class="sxs-lookup"><span data-stu-id="22d61-124">If the "NT AUTHORITY\\SELF" ACE is not found, create a new [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) object with the same property values shown in the table below except the [**Trustee**](iadsaccesscontrolentry-property-methods.md) property contains the account name for SID "S-1-5-10" ("NT AUTHORITY\\SELF").</span></span> <span data-ttu-id="22d61-125">Adicione a entrada à ACL com o método [**IADsAccessControlList. AddAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace) .</span><span class="sxs-lookup"><span data-stu-id="22d61-125">Add the entry to the ACL with the [**IADsAccessControlList.AddAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace) method.</span></span>
8.  <span data-ttu-id="22d61-126">Para atualizar a propriedade **ntSecurityDescriptor** do objeto, chame o método [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) com o mesmo [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) obtido na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="22d61-126">To update the **ntSecurityDescriptor** property of the object, call the [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) method with the same [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) obtained in Step 2.</span></span>
9.  <span data-ttu-id="22d61-127">Confirme as alterações locais para o servidor com o método [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="22d61-127">Commit the local changes to the server with the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method.</span></span>
10. <span data-ttu-id="22d61-128">Se uma das ACEs foi criada, você deve reordenar a ACL para que as ACEs estejam na ordem correta.</span><span class="sxs-lookup"><span data-stu-id="22d61-128">If either of the ACEs were created, you must reorder the ACL so that the ACEs are in the correct order.</span></span> <span data-ttu-id="22d61-129">Para fazer isso, chame a função [**GetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa) com o ADsPath LDAP do objeto e, em seguida, a função [**SetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa) com a mesma DACL.</span><span class="sxs-lookup"><span data-stu-id="22d61-129">To do this, call the [**GetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa) function with the LDAP ADsPath of the object and then the [**SetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa) function with the same DACL.</span></span> <span data-ttu-id="22d61-130">Essa reordenação ocorrerá automaticamente quando as ACEs forem adicionadas.</span><span class="sxs-lookup"><span data-stu-id="22d61-130">This reordering will occur automatically when the ACEs are added.</span></span>

<span data-ttu-id="22d61-131">A tabela a seguir lista os valores de Propriedade do objeto [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) .</span><span class="sxs-lookup"><span data-stu-id="22d61-131">The following table lists the [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) object property values.</span></span>



| <span data-ttu-id="22d61-132">Propriedade IADsAccessControlEntry</span><span class="sxs-lookup"><span data-stu-id="22d61-132">IADsAccessControlEntry Property</span></span>                                        | <span data-ttu-id="22d61-133">Valor</span><span class="sxs-lookup"><span data-stu-id="22d61-133">Value</span></span>                                                                                                                                                                 |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22d61-134">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="22d61-134">**AccessMask**</span></span>](iadsaccesscontrolentry-property-methods.md)          | <span data-ttu-id="22d61-135">**\_acesso ao \_ controle de DS direito do ADS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22d61-135">**ADS\_RIGHT\_DS\_CONTROL\_ACCESS**</span></span>                                                                                                                                   |
| [<span data-ttu-id="22d61-136">**AceType**</span><span class="sxs-lookup"><span data-stu-id="22d61-136">**AceType**</span></span>](iadsaccesscontrolentry-property-methods.md)             | <span data-ttu-id="22d61-137">**Anúncios \_ do ACETYPE \_ o \_ \_ objeto acesso negado** se o usuário não puder alterar sua senha ou o **objeto de \_ \_ acesso \_ \_ permitido pelo ADS ACETYPE** se o usuário puder alterar sua senha.</span><span class="sxs-lookup"><span data-stu-id="22d61-137">**ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT** if the user cannot change their password or **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** if the user can change their password.</span></span> |
| [<span data-ttu-id="22d61-138">**AceFlags**</span><span class="sxs-lookup"><span data-stu-id="22d61-138">**AceFlags**</span></span>](iadsaccesscontrolentry-property-methods.md)            | <span data-ttu-id="22d61-139">0</span><span class="sxs-lookup"><span data-stu-id="22d61-139">0</span></span>                                                                                                                                                                     |
| [<span data-ttu-id="22d61-140">**Flags**</span><span class="sxs-lookup"><span data-stu-id="22d61-140">**Flags**</span></span>](iadsaccesscontrolentry-property-methods.md)               | <span data-ttu-id="22d61-141">**\_tipo de objeto de sinalizador ADS \_ \_ \_ presente**</span><span class="sxs-lookup"><span data-stu-id="22d61-141">**ADS\_FLAG\_OBJECT\_TYPE\_PRESENT**</span></span>                                                                                                                                  |
| [<span data-ttu-id="22d61-142">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="22d61-142">**ObjectType**</span></span>](iadsaccesscontrolentry-property-methods.md)          | <span data-ttu-id="22d61-143">"{AB721A53-1E2F-11D0-9819-00AA0040529B}", que é o GUID de alteração de senha na forma de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="22d61-143">"{AB721A53-1E2F-11D0-9819-00AA0040529B}" which is the change password GUID in string form.</span></span>                                                                            |
| [<span data-ttu-id="22d61-144">**InheritedObjectType**</span><span class="sxs-lookup"><span data-stu-id="22d61-144">**InheritedObjectType**</span></span>](iadsaccesscontrolentry-property-methods.md) | <span data-ttu-id="22d61-145">Não usado</span><span class="sxs-lookup"><span data-stu-id="22d61-145">Not used</span></span>                                                                                                                                                              |
| [<span data-ttu-id="22d61-146">**Confiança**</span><span class="sxs-lookup"><span data-stu-id="22d61-146">**Trustee**</span></span>](iadsaccesscontrolentry-property-methods.md)             | <span data-ttu-id="22d61-147">Nome da conta para o SID "S-1-1-0" (todos).</span><span class="sxs-lookup"><span data-stu-id="22d61-147">Account name for SID "S-1-1-0" (Everyone).</span></span>                                                                                                                            |



 

## <a name="example-code"></a><span data-ttu-id="22d61-148">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="22d61-148">Example Code</span></span>

<span data-ttu-id="22d61-149">O exemplo de código a seguir mostra como obter uma interface para alterar uma DACL.</span><span class="sxs-lookup"><span data-stu-id="22d61-149">The following code example shows how to obtain an interface to change a DACL.</span></span> <span data-ttu-id="22d61-150">A interface [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) pode ser usada definindo a opção **ADS \_ Security \_ info \_ DACL** .</span><span class="sxs-lookup"><span data-stu-id="22d61-150">The [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) interface can be used by setting the **ADS\_SECURITY\_INFO\_DACL** option.</span></span>

> [!Note]  
> <span data-ttu-id="22d61-151">Para usar o código documentado neste exemplo, será necessário ser um administrador.</span><span class="sxs-lookup"><span data-stu-id="22d61-151">To use the code documented in this example, you will need to be an Administrator.</span></span> <span data-ttu-id="22d61-152">Se você não for um administrador, precisará adicionar mais código que usará uma interface que permitirá que um usuário altere a maneira como o cache do lado do cliente é liberado de volta para o serviço de Domínio do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="22d61-152">If you are not an Administrator, then you will need to add more code that will use an interface that will allow a user to change the way the client-side cache is flushed back to the Active Directory Domain Service.</span></span>

 


```C++
//
// Obtain an IADsObjectOptions interface from the object whose
// DACL you wish to modify.
//
long CanReadSetDACL = ADS_SECURITY_INFO_DACL;

CComPtr<IADsObjectOptions> spObjOps;

hr = pads->QueryInterface(IID_IADsObjectOptions, (void**)&spObjOps);

if(SUCCEEDED(hr))

{

//
// Set the option mask you want to change. In this case
// we want to change the objects security information, so we'll
// use the ADS_OPTION_SECURITY_MASK. Since we want to modify the 
// DACL, we'll set the variant to ADS_SEDCURITY_INFO_DACL flag. 
//

    CComVariant svar;
    svar = CanReadSetDACL;
    hr = spObjOps->SetOption(ADS_OPTION_SECURITY_MASK, svar); 

}
//
// The smart pointer declared for pObjOptions can be released
// or it will be destroyed and released once the pointer goes 
// out of scope.
//

```



<span data-ttu-id="22d61-153">O exemplo de código a seguir mostra como modificar o usuário não pode alterar a permissão de senha usando o provedor LDAP.</span><span class="sxs-lookup"><span data-stu-id="22d61-153">The following code example shows how to modify the User Cannot Change Password Permission using the LDAP provider.</span></span> <span data-ttu-id="22d61-154">Este exemplo de código usa a função de utilitário **GetObjectACE** definida acima.</span><span class="sxs-lookup"><span data-stu-id="22d61-154">This code example uses the **GetObjectACE** utility function defined above.</span></span>

<span data-ttu-id="22d61-155">Este exemplo usa as funções de exemplo **GetSidAccountName \_ Everyone** e **GetSidAccountName \_ Self** C++ mostradas em [lendo o usuário não pode alterar a senha (provedor LDAP)](reading-user-cannot-change-password-ldap-provider.md).</span><span class="sxs-lookup"><span data-stu-id="22d61-155">This example uses the **GetSidAccountName\_Everyone** and **GetSidAccountName\_Self** C++ example functions shown in [Reading User Cannot Change Password (LDAP Provider)](reading-user-cannot-change-password-ldap-provider.md).</span></span>


```C++
#include <aclapi.h>

#define CHANGE_PASSWORD_GUID_W L"{AB721A53-1E2F-11D0-9819-00AA0040529B}"

/***************************************************************************

    CreateACE()

    Creates an ACE and returns the IDispatch pointer for the ACE. This 
    pointer can be passed directly to IADsAccessControlList::AddAce.

    bstrTrustee - Contains the Trustee for the ACE.

    bstrObjectType - Contains the ObjectType for the ACE.

    lAccessMask - Contains the AccessMask for the ACE.

    lACEType - Contains the ACEType for the ACE.

    lACEFlags - Contains the ACEFlags for the ACE.

    lFlags - Contains the Flags for the ACE.

***************************************************************************/

IDispatch* CreateACE(BSTR bstrTrustee, 
                     BSTR bstrObjectType, 
                     long lAccessMask, 
                     long lACEType, 
                     long lACEFlags, 
                     long lFlags)
{
    HRESULT hr;
    IDispatch *pDisp = NULL;
    IADsAccessControlEntry *pACE = NULL;

    hr = CoCreateInstance(CLSID_AccessControlEntry,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsAccessControlEntry,
                          (void**)&pACE);
    if(SUCCEEDED(hr)) 
    {
        hr = pACE->put_Trustee(bstrTrustee); 
        hr = pACE->put_ObjectType(bstrObjectType);
        hr = pACE->put_AccessMask(lAccessMask); 
        hr = pACE->put_AceType(lACEType);
        hr = pACE->put_AceFlags(lACEFlags);
        hr = pACE->put_Flags(lFlags);

        hr = pACE->QueryInterface(IID_IDispatch, (LPVOID*)&pDisp);

        pACE->Release();
    }

    return pDisp;
}

/***************************************************************************

    ReorderACEs()

    Causes the ACEs of an object DACL to be reordered properly. The ACEs are 
    automatically put in the proper order when they are added to the DACL. 
    On older systems however, this does not occur automatically, so this 
    function is necessary so the deny ACEs are ordered in the list before 
    the allow ACEs.

    pwszDN - A null-terminated Unicode string that contains the LDAP 
    ADsPath of the DS object to reorder the DACL for.

***************************************************************************/

HRESULT ReorderACEs(LPCWSTR pwszDN)
{
    HRESULT hr = E_FAIL;
    DWORD dwResult;
    ACL *pdacl;
    PSECURITY_DESCRIPTOR psd;
    
    dwResult = GetNamedSecurityInfoW(   (LPWSTR)pwszDN,
                                        SE_DS_OBJECT_ALL,
                                        DACL_SECURITY_INFORMATION,
                                        NULL,
                                        NULL,
                                        &pdacl,
                                        NULL,
                                        &psd);

    if(ERROR_SUCCESS == dwResult)
    {
        dwResult = SetNamedSecurityInfoW(   (LPWSTR)pwszDN,
                                            SE_DS_OBJECT_ALL,
                                            DACL_SECURITY_INFORMATION,
                                            NULL,
                                            NULL,
                                            pdacl,
                                            NULL);

        LocalFree(psd);
        
        if(ERROR_SUCCESS == dwResult)
        {
            hr = S_OK;
        }
    }
    
    return hr;
}

/***************************************************************************

    SetUserCannotChangePassword()

    Sets the "User Cannot Change Password" permission using the LDAP provider 
    to the specified setting. To do this, find the existing 
    ACEs and modify the AceType. If the ACE is not found, a new one of the 
    proper type is created and added. The ACEs should always be present, but 
    it is possible that the default DACL excludes them, so this situation 
    will be handled correctly.

    pwszUserDN - A null-terminated Unicode string that contains the LDAP 
    ADsPath of the user object to modify.

    pwszUsername - A null-terminated Unicode string that contains the user 
    name to use for authorization. If this is NULL, the credentials of the 
    current user are used.

    pwszPassword - A null-terminated Unicode string that contains the 
    password to use for authorization. This is ignored if pwszUsername is 
    NULL.

    fCannotChangePassword - Contains the new setting for the privilege. 
    Contains nonzero if the user cannot change their password or zero if 
    the can change their password.

***************************************************************************/

HRESULT SetUserCannotChangePassword(LPCWSTR pwszUserDN, 
                                    LPCWSTR pwszUsername, 
                                    LPCWSTR pwszPassword,
                                    BOOL fCannotChangePassword)
{
    HRESULT hr;

    CComBSTR sbstrEveryone;
    hr = GetSidAccountName_Everyone(&sbstrEveryone);
    if(FAILED(hr))
    {
        return hr;
    }

    CComBSTR sbstrSelf;
    hr = GetSidAccountName_Self(&sbstrSelf);
    if(FAILED(hr))
    {
        return hr;
    }

    if(NULL == pwszUserDN)
    {
        return E_INVALIDARG;
    }
    
    IADs *pads;

    hr = ADsOpenObject( pwszUserDN,
                        pwszUsername,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs, 
                        (LPVOID*)&pads);

    if(SUCCEEDED(hr))
    {
        CComBSTR sbstrSecDesc = "ntSecurityDescriptor";
        CComVariant svar;
        
        hr = pads->Get(sbstrSecDesc, &svar);
        if(SUCCEEDED(hr))
        {
            IADsSecurityDescriptor *psd;

            hr = svar.pdispVal->QueryInterface(IID_IADsSecurityDescriptor, (LPVOID*)&psd);
            if(SUCCEEDED(hr))
            {
                IDispatch *pDisp;

                hr = psd->get_DiscretionaryAcl(&pDisp);
                if(SUCCEEDED(hr))
                {
                    IADsAccessControlList *pACL;

                    hr = pDisp->QueryInterface(IID_IADsAccessControlList, (void**)&pACL);
                    if(SUCCEEDED(hr)) 
                    {
                        BOOL fMustReorder = FALSE;
                        /*
                        Get the existing ACE for the change password permission 
                        for Everyone. If it exists, just modify the existing 
                        ACE. If it does not exist, create a new one and add it 
                        to the ACL.
                        */
                        IADsAccessControlEntry *pACEEveryone = NULL;
                        hr = GetObjectACE(pACL, CHANGE_PASSWORD_GUID_W, sbstrEveryone, &pACEEveryone);
                        if(pACEEveryone)
                        {
                            hr = pACEEveryone->put_AceType(fCannotChangePassword ? 
                                ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                ADS_ACETYPE_ACCESS_ALLOWED_OBJECT);

                            pACEEveryone->Release();
                        }
                        else
                        {
                            IDispatch *pDispEveryone = NULL;
                            
                            pDispEveryone = CreateACE(sbstrEveryone, 
                                CComBSTR(CHANGE_PASSWORD_GUID_W),
                                ADS_RIGHT_DS_CONTROL_ACCESS, 
                                fCannotChangePassword ? 
                                    ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                    ADS_ACETYPE_ACCESS_ALLOWED_OBJECT, 
                                0,
                                ADS_FLAG_OBJECT_TYPE_PRESENT);
                            
                            if(pDispEveryone)
                            {
                                //add the new ACE for everyone
                                hr = pACL->AddAce(pDispEveryone);

                                pDispEveryone->Release();

                                fMustReorder = TRUE;
                            }                            
                        }
                        
                        /*
                        Get the existing ACE for the change password permission 
                        for Self. If it exists, just modify the existing 
                        ACE. If it does not exist, create a new one and add it 
                        to the ACL.
                        */
                        IADsAccessControlEntry *pACESelf = NULL;
                        hr = GetObjectACE(pACL, CHANGE_PASSWORD_GUID_W, sbstrSelf, &pACESelf);
                        if(pACESelf)
                        {
                            hr = pACESelf->put_AceType(fCannotChangePassword ? 
                                ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                ADS_ACETYPE_ACCESS_ALLOWED_OBJECT);
                        
                            pACESelf->Release();
                        }
                        else
                        {
                            IDispatch *pDispSelf = NULL;
                            
                            pDispSelf = CreateACE(sbstrSelf, 
                                CComBSTR(CHANGE_PASSWORD_GUID_W),
                                ADS_RIGHT_DS_CONTROL_ACCESS, 
                                fCannotChangePassword ? 
                                    ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                    ADS_ACETYPE_ACCESS_ALLOWED_OBJECT, 
                                0,
                                ADS_FLAG_OBJECT_TYPE_PRESENT);

                            if(pDispSelf)
                            {
                                //add the new ACE for self
                                hr = pACL->AddAce(pDispSelf);

                                pDispSelf->Release();

                                fMustReorder = TRUE;
                            }                            
                        }

                        //update the security descriptor property
                        hr = pads->Put(sbstrSecDesc, svar);
                        
                        //commit the changes
                        hr = pads->SetInfo();

                        if(fMustReorder)
                        {
                            ReorderACEs(pwszUserDN);
                        }

                        pACL->Release();
                    }

                    pDisp->Release();
                }
                
                psd->Release();
            }
        }
    }

    return hr;
}
```



<span data-ttu-id="22d61-156">O exemplo de código a seguir mostra como modificar o usuário não pode alterar a permissão de senha usando o provedor LDAP.</span><span class="sxs-lookup"><span data-stu-id="22d61-156">The following code example shows how to modify the User Cannot Change Password Permission using the LDAP provider.</span></span>

> [!Note]  
> <span data-ttu-id="22d61-157">O exemplo a seguir só funcionará em domínios em que o idioma principal é o inglês, pois as cadeias de caracteres "todos" e "auto Autoridade NT \\ " são localizadas com base no idioma do primeiro controlador de domínio no domínio.</span><span class="sxs-lookup"><span data-stu-id="22d61-157">The example below will only work on domains where the primary language is English because the "Everyone" and "NT AUTHORITY\\SELF" strings are localized based on the language of the first domain controller in the domain.</span></span> <span data-ttu-id="22d61-158">Não há nenhuma maneira de Visual Basic obter os nomes de conta para uma entidade de segurança conhecida sem chamar a função [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) .</span><span class="sxs-lookup"><span data-stu-id="22d61-158">There is no way in Visual Basic to obtain the account names for a well-known security principal without calling the [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) function.</span></span> <span data-ttu-id="22d61-159">Se estiver usando Visual Basic, é recomendável que você use o provedor WinNT para modificar a permissão o usuário não pode alterar a senha, conforme mostrado em [modificando o usuário não pode alterar a senha (provedor winnt)](modifying-user-cannot-change-password-winnt-provider.md).</span><span class="sxs-lookup"><span data-stu-id="22d61-159">If using Visual Basic, it is suggested that you use the WinNT provider to modify the User Cannot Change Password Permission as shown in [Modifying User Cannot Change Password (WinNT Provider)](modifying-user-cannot-change-password-winnt-provider.md).</span></span>

 


```VB
'******************************************************************************
'
'    SetUserCannotChangePassword
'
'    Sets the "User Cannot Change Password" permission using the LDAP provider
'    to the specified setting. This is accomplished by finding the existing
'    ACEs and modifying the AceType. The ACEs should always be present, but
'    it is possible that the default DACL excludes them. This function will not
'    work correctly if both ACEs are not present.
'
'    strUserDN - A string that contains the LDAP ADsPath of the user object to
'    modify.
'
'    strUsername - A string that contains the user name to use for
'    authorization. If this is an empty string, the credentials of the current
'    user are used.
'
'    strPassword - A string that contains the password to use for authorization.
'    This is ignored if strUsername is empty.
'
'    fCannotChangePassword - Contains the new setting for the privilege.
'    Contains True if the user cannot change their password or False if
'    the can change their password.
'
'******************************************************************************
Sub SetUserCannotChangePassword(strUserDN As String, strUsername As String, strPassword As String, fUserCannotChangePassword As Boolean)
    Dim oUser As IADs
    Dim oSecDesc As IADsSecurityDescriptor
    Dim oACL As IADsAccessControlList
    Dim oACE As IADsAccessControlEntry
    
    fEveryone = False
    fSelf = False
    
    If "" <> strUsername Then
        Dim dso As IADsOpenDSObject
        
        ' Bind to the group with the specified user name and password.
        Set dso = GetObject("LDAP:")
        Set oUser = dso.OpenDSObject(strUserDN, strUsername, strPassword, 1)
    Else
        ' Bind to the group with the current credentials.
        Set oUser = GetObject(strUserDN)
    End If
    
    Set oSecDesc = oUser.Get("ntSecurityDescriptor")
    Set oACL = oSecDesc.DiscretionaryAcl
    
    ' Modify the existing entries.
    For Each oACE In oACL
        If UCase(oACE.ObjectType) = UCase(CHANGE_PASSWORD_GUID) Then
            If oACE.Trustee = "Everyone" Then
                ' Modify the ace type of the entry.
                If fUserCannotChangePassword Then
                    oACE.AceType = ADS_ACETYPE_ACCESS_DENIED_OBJECT
                Else
                    oACE.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT
                End If
            End If
        
            If oACE.Trustee = "NT AUTHORITY\SELF" Then
                ' Modify the ace type of the entry.
                If fUserCannotChangePassword Then
                    oACE.AceType = ADS_ACETYPE_ACCESS_DENIED_OBJECT
                Else
                    oACE.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT
                End If
            End If
        End If
    Next
    
    ' Update the ntSecurityDescriptor property.
    oUser.Put "ntSecurityDescriptor", oSecDesc
    
    ' Commit the changes to the server.
    oUser.SetInfo
End Sub
```



 

 