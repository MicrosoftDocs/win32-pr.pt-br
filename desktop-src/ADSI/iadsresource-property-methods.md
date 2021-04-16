---
title: Métodos de propriedade IADsResource (IADs. h)
description: Os métodos de propriedade da interface IADsResource obtêm ou definem as propriedades descritas na tabela a seguir. Para obter uma discussão geral sobre métodos de propriedade, consulte interface Property Methods.
ms.assetid: a2d6ed76-88e9-468f-928a-a038b73fb362
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsResource
topic_type:
- apiref
api_name:
- IADsResource Property Methods
- IADsResource.LockCount
- IADsResource.get_LockCount
- IADsResource.Path
- IADsResource.get_Path
- IADsResource.User
- IADsResource.get_User
- IADsResource.UserPath
- IADsResource.get_UserPath
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0f2ab2642dd8d03062a26d096190cf7615977a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753833"
---
# <a name="iadsresource-property-methods"></a><span data-ttu-id="61424-105">Métodos de propriedade IADsResource</span><span class="sxs-lookup"><span data-stu-id="61424-105">IADsResource Property Methods</span></span>

<span data-ttu-id="61424-106">Os métodos de propriedade da interface [**IADsResource**](/windows/desktop/api/Iads/nn-iads-iadsresource) obtêm ou definem as propriedades descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="61424-106">The property methods of the [**IADsResource**](/windows/desktop/api/Iads/nn-iads-iadsresource) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="61424-107">Para obter uma discussão geral sobre métodos de propriedade, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="61424-107">For a general discussion of property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="61424-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="61424-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="61424-109">**LockCount**</span><span class="sxs-lookup"><span data-stu-id="61424-109">**LockCount**</span></span>
<span data-ttu-id="61424-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="61424-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="61424-111">Número de bloqueios no recurso.</span><span class="sxs-lookup"><span data-stu-id="61424-111">Number of locks on the resource.</span></span>

<dt>

<span data-ttu-id="61424-112">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61424-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61424-113">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="61424-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LockCount(
  [out] LONG* plLockCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="61424-114">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="61424-114">**Path**</span></span>
<span data-ttu-id="61424-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="61424-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="61424-116">O caminho do sistema de arquivos do recurso aberto.</span><span class="sxs-lookup"><span data-stu-id="61424-116">The file system path of the opened resource.</span></span>

<dt>

<span data-ttu-id="61424-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61424-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61424-118">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="61424-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="61424-119">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="61424-119">**User**</span></span>
<span data-ttu-id="61424-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="61424-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="61424-121">O nome do usuário que abriu o recurso.</span><span class="sxs-lookup"><span data-stu-id="61424-121">The name of the user who opened the resource.</span></span>

<dt>

<span data-ttu-id="61424-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61424-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61424-123">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="61424-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_User(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="61424-124">**UserPath**</span><span class="sxs-lookup"><span data-stu-id="61424-124">**UserPath**</span></span>
<span data-ttu-id="61424-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="61424-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="61424-126">O ADsPath do objeto de usuário para o usuário que abriu o recurso.</span><span class="sxs-lookup"><span data-stu-id="61424-126">The ADsPath of the user object for the user who opened the resource.</span></span>

<dt>

<span data-ttu-id="61424-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="61424-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61424-128">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="61424-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserPath(
  [out] BSTR* pbstrUserPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="61424-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="61424-129">Examples</span></span>

<span data-ttu-id="61424-130">O exemplo de código a seguir mostra como examinar os recursos abertos de um serviço de arquivo.</span><span class="sxs-lookup"><span data-stu-id="61424-130">The following code example shows how to examine open resources of a file service.</span></span>


```VB
Dim fso As IADsFileServiceOperations
' Bind to a file service operations object on "myComputer" in the local domain.
Set fso = GetObject("WinNT://myComputer/LanmanServer")

' Enumerate resources.
If (IsEmpty(fso) = False) Then
    For Each resource In fso.resources
        MsgBox "Resource name: " & resource.name
        MsgBox "Resource path: " & resource.path
    Next resource
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fso = Nothing
```



<span data-ttu-id="61424-131">O exemplo de código a seguir enumera uma coleção de recursos.</span><span class="sxs-lookup"><span data-stu-id="61424-131">The following code example enumerates a collection of resources.</span></span>


```C++
IADsFileServiceOperations *pFso = NULL;
IADsResource *pRes = NULL;
IADsCollection *pColl = NULL;
IUnknown *pUnk = NULL;
IEnumVARIANT *pEnum = NULL;
BSTR bstr = NULL;
VARIANT var;
ULONG lFetch = 0;
IDispatch *pDisp = NULL;
HRESULT hr = S_OK;

LPWSTR adsPath =L"WinNT://aMachine/LanmanServer";
hr = ADsGetObject(adsPath, IID_IADsFileServiceOperations,(void**)&pFso);
if(FAILED(hr)) {goto Cleanup;}

hr = pFso->Resources(&pColl);
if(FAILED(hr)) {goto Cleanup;}


// Enumerate print jobs. Code omitted.
hr = pColl->get__NewEnum(&pUnk);
if(FAILED(hr)) {goto Cleanup;}

hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
if(FAILED(hr)) {goto Cleanup;}

// Enumerate.
VariantInit(&var);
hr = pEnum->Next(1, &var, &lFetch);
while(hr == S_OK)
{
    if (lFetch == 1)    
    {
        pDisp = V_DISPATCH(&var);
        pDisp->QueryInterface(IID_IADsResource, (void**)&pRes);
        pRes->get_Name(&bstr);
        printf("Resource name: %S\n",bstr);
        SysFreeString(bstr);
        pRes->get_Path(&bstr);
        printf("Resource path: %S\n",bstr);
        SysFreeString(bstr);
        pRes->Release();
    }
    pDisp->Release();
    VariantClear(&var);
    hr = pEnum->Next(1, &var, &lFetch);
};

Cleanup:
    if(pRes) pRes->Release();
    if(pDisp) pDisp->Release();
    if(pEnum) pEnum->Release();
    if(pUnk) pUnk->Release();
    if(pColl) pColl->Release();
    if(pFso) pFso->Release();
```



## <a name="requirements"></a><span data-ttu-id="61424-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61424-132">Requirements</span></span>



| <span data-ttu-id="61424-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="61424-133">Requirement</span></span> | <span data-ttu-id="61424-134">Valor</span><span class="sxs-lookup"><span data-stu-id="61424-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="61424-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61424-135">Minimum supported client</span></span><br/> | <span data-ttu-id="61424-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="61424-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="61424-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61424-137">Minimum supported server</span></span><br/> | <span data-ttu-id="61424-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61424-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="61424-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="61424-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="61424-140"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="61424-140"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="61424-141">DLL</span><span class="sxs-lookup"><span data-stu-id="61424-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61424-142"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61424-142"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="61424-143">IID</span><span class="sxs-lookup"><span data-stu-id="61424-143">IID</span></span><br/>                      | <span data-ttu-id="61424-144">IID \_ IADsResource é definido como 34A05B20-4AAB-11CF-AE2C-00AA006EBFB9</span><span class="sxs-lookup"><span data-stu-id="61424-144">IID\_IADsResource is defined as 34A05B20-4AAB-11CF-AE2C-00AA006EBFB9</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="61424-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="61424-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61424-146">**IADsResource**</span><span class="sxs-lookup"><span data-stu-id="61424-146">**IADsResource**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsresource)
</dt> <dt>

[<span data-ttu-id="61424-147">**IADsFileServiceOperations:: recursos**</span><span class="sxs-lookup"><span data-stu-id="61424-147">**IADsFileServiceOperations::Resources**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsfileserviceoperations-resources)
</dt> </dl>

 

 





