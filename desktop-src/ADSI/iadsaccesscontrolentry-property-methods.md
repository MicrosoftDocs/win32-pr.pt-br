---
title: Métodos de propriedade IADsAccessControlEntry (IADs. h)
description: Os métodos de propriedade da interface IADsAccessControlEntry obtêm ou definem as propriedades descritas na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: dce11723-0e30-4baa-8666-0a32f0968ebb
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsAccessControlEntry
topic_type:
- apiref
api_name:
- IADsAccessControlEntry Property Methods
- IADsAccessControlEntry.AccessMask
- IADsAccessControlEntry.get_AccessMask
- IADsAccessControlEntry.put_AccessMask
- IADsAccessControlEntry.AceType
- IADsAccessControlEntry.get_AceType
- IADsAccessControlEntry.put_AceType
- IADsAccessControlEntry.AceFlags
- IADsAccessControlEntry.get_AceFlags
- IADsAccessControlEntry.put_AceFlags
- IADsAccessControlEntry.Flags
- IADsAccessControlEntry.get_Flags
- IADsAccessControlEntry.put_Flags
- IADsAccessControlEntry.ObjectType
- IADsAccessControlEntry.get_ObjectType
- IADsAccessControlEntry.put_ObjectType
- IADsAccessControlEntry.InheritedObjectType
- IADsAccessControlEntry.get_InheritedObjectType
- IADsAccessControlEntry.put_InheritedObjectType
- IADsAccessControlEntry.Trustee
- IADsAccessControlEntry.get_Trustee
- IADsAccessControlEntry.put_Trustee
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b8539807f21944ab6f4b2c03f04b14a53dffdb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644406"
---
# <a name="iadsaccesscontrolentry-property-methods"></a><span data-ttu-id="1936e-105">Métodos de propriedade IADsAccessControlEntry</span><span class="sxs-lookup"><span data-stu-id="1936e-105">IADsAccessControlEntry Property Methods</span></span>

<span data-ttu-id="1936e-106">Os métodos de propriedade da interface [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) obtêm ou definem as propriedades descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1936e-106">The property methods of the [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="1936e-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="1936e-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="1936e-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1936e-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="1936e-109">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="1936e-109">**AccessMask**</span></span>
<span data-ttu-id="1936e-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1936e-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="1936e-111">Contém um conjunto de sinalizadores que especifica os privilégios de acesso para o objeto.</span><span class="sxs-lookup"><span data-stu-id="1936e-111">Contains a set of flags that specifies access privileges for the object.</span></span> <span data-ttu-id="1936e-112">Os valores válidos para os objetos de Active Directory são definidos na enumeração de enumeração de [**\_ \_ direitos do ADS**](/windows/win32/api/iads/ne-iads-ads_rights_enum) .</span><span class="sxs-lookup"><span data-stu-id="1936e-112">Valid values for Active Directory objects are defined in the [**ADS\_RIGHTS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_rights_enum) enumeration.</span></span>

<span data-ttu-id="1936e-113">Para obter mais informações e uma lista de valores possíveis para objetos de compartilhamento de arquivos ou arquivos, consulte [segurança de arquivos e direitos de acesso](/windows/desktop/FileIO/file-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="1936e-113">For more information and a list of possible values for file or file share objects, see [File Security and Access Rights](/windows/desktop/FileIO/file-security-and-access-rights).</span></span>

<span data-ttu-id="1936e-114">Para obter mais informações e uma lista de valores possíveis para objetos do registro, consulte [segurança da chave do registro e direitos de acesso](/windows/desktop/SysInfo/registry-key-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="1936e-114">For more information and a list of possible values for registry objects, see [Registry Key Security and Access Rights](/windows/desktop/SysInfo/registry-key-security-and-access-rights).</span></span>

<dt>

<span data-ttu-id="1936e-115">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1936e-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1936e-116">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="1936e-116">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AccessMask(
  [out] LONG* plnAccessMask
);
HRESULT put_AccessMask(
  [in] LONG lnAccessMask
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1936e-117">**AceFlags**</span><span class="sxs-lookup"><span data-stu-id="1936e-117">**AceFlags**</span></span>
<span data-ttu-id="1936e-118"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1936e-118"></dt> <dd> <dl></span></span>

<span data-ttu-id="1936e-119">Contém um conjunto de sinalizadores que especifica se outros contêineres ou objetos podem herdar a ACE.</span><span class="sxs-lookup"><span data-stu-id="1936e-119">Contains a set of flags that specifies if other containers or objects can inherit the ACE.</span></span> <span data-ttu-id="1936e-120">Os valores válidos para o objeto Active Directory são definidos na enumeração [**\_ \_ enum ACEFLAG do ADS**](/windows/win32/api/iads/ne-iads-ads_aceflag_enum) .</span><span class="sxs-lookup"><span data-stu-id="1936e-120">Valid values for Active Directory object are defined in the [**ADS\_ACEFLAG\_ENUM**](/windows/win32/api/iads/ne-iads-ads_aceflag_enum) enumeration.</span></span>

<span data-ttu-id="1936e-121">Para obter mais informações e os valores possíveis para arquivos, compartilhamento de arquivos e objetos do registro, consulte o membro **AceFlags** da estrutura de [**\_ cabeçalho Ace**](/windows/desktop/api/winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="1936e-121">For more information and possible values for file, file share, and registry objects, see the **AceFlags** member of the [**ACE\_HEADER**](/windows/desktop/api/winnt/ns-winnt-ace_header) structure.</span></span>

<dt>

<span data-ttu-id="1936e-122">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1936e-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1936e-123">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="1936e-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AceFlags(
  [out] LONG* plnAceFlags
);
HRESULT put_AceFlags(
  [in] LONG lnAceFlags
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1936e-124">**AceType**</span><span class="sxs-lookup"><span data-stu-id="1936e-124">**AceType**</span></span>
<span data-ttu-id="1936e-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1936e-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="1936e-126">Contém um valor que indica o tipo de ACE.</span><span class="sxs-lookup"><span data-stu-id="1936e-126">Contains a value that indicates the type of ACE.</span></span> <span data-ttu-id="1936e-127">Os valores válidos para os objetos Active Directory são definidos na enumeração [**\_ \_ enum ACETYPE do ADS**](/windows/win32/api/iads/ne-iads-ads_acetype_enum) .</span><span class="sxs-lookup"><span data-stu-id="1936e-127">Valid values for Active Directory objects are defined in the [**ADS\_ACETYPE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_acetype_enum) enumeration.</span></span>

<span data-ttu-id="1936e-128">Para obter mais informações e os valores possíveis para arquivos, compartilhamento de arquivos e objetos do registro, consulte o membro **AceType** da estrutura de [**\_ cabeçalho Ace**](/windows/desktop/api/winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="1936e-128">For more information and possible values for file, file share, and registry objects, see the **AceType** member of the [**ACE\_HEADER**](/windows/desktop/api/winnt/ns-winnt-ace_header) structure.</span></span>

<dt>

<span data-ttu-id="1936e-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1936e-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1936e-130">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="1936e-130">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AceType(
  [out] LONG* plAceType
);
HRESULT put_AceType(
  [in] LONG lnAceType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1936e-131">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="1936e-131">**Flags**</span></span>
<span data-ttu-id="1936e-132"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1936e-132"></dt> <dd> <dl></span></span>

<span data-ttu-id="1936e-133">Um sinalizador que indica se a ACE tem um tipo de objeto ou tipo de objeto herdado.</span><span class="sxs-lookup"><span data-stu-id="1936e-133">A flag that indicates if the ACE has an object type or inherited object type.</span></span> <span data-ttu-id="1936e-134">Os sinalizadores válidos são definidos na [**enumeração \_ \_ enumType do ADS**](/windows/win32/api/iads/ne-iads-ads_flagtype_enum) .</span><span class="sxs-lookup"><span data-stu-id="1936e-134">Valid flags are defined in the [**ADS\_FLAGTYPE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_flagtype_enum) enumeration.</span></span>

<dt>

<span data-ttu-id="1936e-135">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1936e-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1936e-136">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="1936e-136">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Flags(
  [out] LONG* lnflags
);
HRESULT put_Flags(
  [in] LONG lnflags
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1936e-137">**InheritedObjectType**</span><span class="sxs-lookup"><span data-stu-id="1936e-137">**InheritedObjectType**</span></span>
<span data-ttu-id="1936e-138"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1936e-138"></dt> <dd> <dl></span></span>

<span data-ttu-id="1936e-139">Um sinalizador que indica o tipo de um objeto filho de um objeto ADSI.</span><span class="sxs-lookup"><span data-stu-id="1936e-139">A flag that indicates the type of a child object of an ADSI object.</span></span> <span data-ttu-id="1936e-140">Seu valor é um **GUID** para um objeto no formato de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1936e-140">Its value is a **GUID** to an object in string format.</span></span> <span data-ttu-id="1936e-141">Quando tal **GUID** é definido, a Ace aplica-se somente ao objeto referido pelo **GUID**.</span><span class="sxs-lookup"><span data-stu-id="1936e-141">When such a **GUID** is set, the ACE applies only to the object referred to by the **GUID**.</span></span>

<dt>

<span data-ttu-id="1936e-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1936e-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1936e-143">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1936e-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_InheritedObjectType(
  [out] BSTR* bstrInheritedObjectType
);
HRESULT put_InheritedObjectType(
  [in] BSTR bstrInheritedObjectType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1936e-144">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="1936e-144">**ObjectType**</span></span>
<span data-ttu-id="1936e-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1936e-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="1936e-146">Um sinalizador que indica o tipo de objeto ADSI.</span><span class="sxs-lookup"><span data-stu-id="1936e-146">A flag that indicates the ADSI object type.</span></span> <span data-ttu-id="1936e-147">Seu valor é um **GUID** para uma propriedade ou um objeto no formato de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1936e-147">Its value is a **GUID** to a property or an object in string format.</span></span> <span data-ttu-id="1936e-148">O **GUID** refere-se a uma propriedade quando o ADS é o **\_ \_ DS \_ ler \_ prop** e **anúncios \_ Right \_ DS \_ Write \_ prop** . as máscaras de acesso são usadas.</span><span class="sxs-lookup"><span data-stu-id="1936e-148">The **GUID** refers to a property when **ADS\_RIGHT\_DS\_READ\_PROP** and **ADS\_RIGHT\_DS\_WRITE\_PROP** access masks are used.</span></span> <span data-ttu-id="1936e-149">O **GUID** especifica um objeto quando **ADS \_ direito \_ \_ criar \_ filho** e **anúncios direito de \_ \_ excluir DS de \_ exclusão \_** de acesso filho são usados.</span><span class="sxs-lookup"><span data-stu-id="1936e-149">The **GUID** specifies an object when **ADS\_RIGHT\_DS\_CREATE\_CHILD** and **ADS\_RIGHT\_DS\_DELETE\_CHILD** access masks are used.</span></span>

<dt>

<span data-ttu-id="1936e-150">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1936e-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1936e-151">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1936e-151">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectType(
  [out] BSTR* bstrObjectType
);
HRESULT put_ObjectType(
  [in] BSTR bstrObjectType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1936e-152">**Confiança**</span><span class="sxs-lookup"><span data-stu-id="1936e-152">**Trustee**</span></span>
<span data-ttu-id="1936e-153"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1936e-153"></dt> <dd> <dl></span></span>

<span data-ttu-id="1936e-154">Contém o nome da conta à qual a ACE se aplica.</span><span class="sxs-lookup"><span data-stu-id="1936e-154">Contains the name of the account that the ACE applies to.</span></span>

<dt>

<span data-ttu-id="1936e-155">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1936e-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1936e-156">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1936e-156">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Trustee(
  [out] BSTR* pbstrSecurityId
);
HRESULT put_Trustee(
  [in] BSTR bstrSecurityId
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="1936e-157">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1936e-157">Examples</span></span>

<span data-ttu-id="1936e-158">O exemplo de código a seguir mostra como adicionar entradas a uma ACL discricionária usando os métodos de propriedade [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) .</span><span class="sxs-lookup"><span data-stu-id="1936e-158">The following code example shows how to add entries to a discretionary ACL using the [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) property methods.</span></span>


```VB
Dim x As IADs
Dim sd As IADsSecurityDescriptor
Dim ace As IADsAccessControlEntry
Dim Dacl As IADsAccessControlList
Dim Ace1 As New AccessControlEntry
Dim Ace2 As New AccessControlEntry

On Error GoTo Cleanup
 
Set x = GetObject("LDAP://OU=Sales, DC=Fabrikam,DC=com")
Set sd = x.Get("ntSecurityDescriptor")
Set Dacl = sd.DiscretionaryAcl
 
' Show the existing ACEs.
For Each ace In Dacl
  Debug.Print ace.Trustee
Next
 
 
' Setup the first ACE.
Ace1.AccessMask = -1 'Full Permission (Allowed)
Ace1.AceType = ADS_ACETYPE_ACCESS_ALLOWED
Ace1.AceFlags = ADS_ACEFLAG_INHERIT_ACE
Ace1.Trustee = "ACTIVED\Administrator"
 
' Setup the 2nd ACE.
Ace2.AccessMask = -1 'Full Permission (Denied)
Ace2.AceType = ADS_ACETYPE_ACCESS_DENIED
Ace2.AceFlags = ADS_ACEFLAG_INHERIT_ACE
Ace2.Trustee = "ACTIVED\Andyhar"
 
' Add the ACEs to the Discretionary ACL.
Dacl.AddAce Ace1
Dacl.AddAce Ace2
 
sd.DiscretionaryAcl = Dacl
x.Put "ntSecurityDescriptor", Array(sd)
x.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set x = Nothing
    Set sd = Nothing
    Set ace = Nothing
    Set Dacl = Nothing
    Set Ace1 = Nothing
    Set Ace2 = Nothing
    Set obj = Nothing
    Set cls = Nothing
```



<span data-ttu-id="1936e-159">O exemplo de código a seguir exibe entradas de controle de acesso.</span><span class="sxs-lookup"><span data-stu-id="1936e-159">The following code example displays access-control entries.</span></span>


```C++
IADs *pADs = NULL;
IDispatch *pDisp = NULL;
IADsSecurityDescriptor *pSD = NULL;
VARIANT var;
HRESULT hr = S_OK;
 
VariantInit(&var);

hr = ADsOpenObject(L"LDAP://OU=Sales, DC=Fabrikam,DC=com",NULL,NULL,
                   ADS_SECURE_AUTHENTICATION, IID_IADs,(void**)&pADs);
if(FAILED(hr)) {goto Cleanup;}

hr = pADs->Get(CComBSTR("ntSecurityDescriptor"),&var);
if(FAILED(hr)) {goto Cleanup;}

pDisp = V_DISPATCH(&var);

hr = pDisp->QueryInterface(IID_IADsSecurityDescriptor,(void**)&pSD);
if(FAILED(hr)) {goto Cleanup;}
pDisp->Release();


pSD->get_DiscretionaryAcl(&pDisp);

hr = pDisp->QueryInterface(IID_IADsAccessControlList,(void**)&pACL);
if(FAILED(hr)) {goto Cleanup;}

hr = DisplayAccessInfo(pSD);
if(FAILED(hr)) {goto Cleanup;}
VariantClear(&var);

Cleanup:
    if(pADs) pADs->Release();
    if(pDisp) pDisp->Release();
    if(pSD) pSD->Release();
    return hr;



HRESULT DisplayAccessInfo(IADsSecurityDescriptor *pSD)
{
    LPWSTR lpszFunction = L"DisplayAccessInfo";
    IDispatch *pDisp = NULL;
    IADsAccessControlList *pACL = NULL;
    IADsAccessControlEntry *pACE = NULL;
    IEnumVARIANT *pEnum = NULL;
    IUnknown *pUnk = NULL;
    HRESULT hr = S_OK;
    ULONG nFetch = 0;
    BSTR bstrValue = NULL;
    VARIANT var;
    LPWSTR lpszOutput = NULL;
    LPWSTR lpszMask = NULL;
    size_t nLength = 0;
    
    VariantInit(&var);
    
    hr = pSD->get_DiscretionaryAcl(&pDisp);
    if(FAILED(hr)){goto Cleanup;}
    hr = pDisp->QueryInterface(IID_IADsAccessControlList,(void**)&pACL);
    if(FAILED(hr)){goto Cleanup;}
    
    hr = pACL->get__NewEnum(&pUnk);
    if(FAILED(hr)){goto Cleanup;}
    
    hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
    
    if(FAILED(hr)){goto Cleanup;}
    hr = pEnum->Next(1,&var,&nFetch);
    
    while(hr == S_OK)
    {
        if(nFetch==1)
        {
            if(VT_DISPATCH != V_VT(&var))
            {
                goto Cleanup;
            }
            
            pDisp = V_DISPATCH(&var);
            hr = pDisp->QueryInterface(IID_IADsAccessControlEntry,(void**)&pACE);
            
            if(SUCCEEDED(hr))
            {
                lpszMask = L"Trustee: %s";
                hr = pACE->get_Trustee(&bstrValue);
                nLength = wcslen(lpszMask) + wcslen(bstrValue) + 1;
                lpszOutput = new WCHAR[nLength];
                swprintf_s(lpszOutput,lpszMask,bstrValue);
                printf(lpszOutput);
                delete [] lpszOutput;
                SysFreeString(bstrValue);
                
                pACE->Release();
                pACE = NULL;
                pDisp->Release();
                pDisp = NULL;
            }       
            
            VariantClear(&var);
        }       
        hr = pEnum->Next(1,&var,&nFetch);
    }
    
Cleanup:
    if(pDisp) pDisp->Release();
    if(pACL) pACL->Release();
    if(pACE) pACE->Release();
    if(pEnum) pEnum->Release();
    if(pUnk) pUnk->Release();
    if(szValue) SysFreeString(szValue);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="1936e-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1936e-160">Requirements</span></span>



| <span data-ttu-id="1936e-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="1936e-161">Requirement</span></span> | <span data-ttu-id="1936e-162">Valor</span><span class="sxs-lookup"><span data-stu-id="1936e-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1936e-163">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1936e-163">Minimum supported client</span></span><br/> | <span data-ttu-id="1936e-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1936e-164">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="1936e-165">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1936e-165">Minimum supported server</span></span><br/> | <span data-ttu-id="1936e-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1936e-166">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="1936e-167">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1936e-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="1936e-168"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="1936e-168"><dt>Iads.h</dt></span></span> </dl>         |
| <span data-ttu-id="1936e-169">DLL</span><span class="sxs-lookup"><span data-stu-id="1936e-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1936e-170"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1936e-170"><dt>Activeds.dll</dt></span></span> </dl>   |
| <span data-ttu-id="1936e-171">IID</span><span class="sxs-lookup"><span data-stu-id="1936e-171">IID</span></span><br/>                      | <span data-ttu-id="1936e-172">IID \_ IADsAccessControlEntry é definido como B4F3A14C-9BDD-11D0-852C-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="1936e-172">IID\_IADsAccessControlEntry is defined as B4F3A14C-9BDD-11D0-852C-00C04FD8D503</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1936e-173">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1936e-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1936e-174">**IADsAccessControlEntry**</span><span class="sxs-lookup"><span data-stu-id="1936e-174">**IADsAccessControlEntry**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)
</dt> <dt>

[<span data-ttu-id="1936e-175">**IADsAccessControlList**</span><span class="sxs-lookup"><span data-stu-id="1936e-175">**IADsAccessControlList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)
</dt> <dt>

[<span data-ttu-id="1936e-176">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="1936e-176">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> </dl>

 

