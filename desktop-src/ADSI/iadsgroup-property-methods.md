---
title: Métodos de propriedade IADs (IADs. h)
description: Métodos de propriedade da interface IADs.
ms.assetid: a8aa88d4-4695-47bc-bf7f-a17236a5671c
ms.tgt_platform: multiple
keywords:
- ADSI dos métodos de propriedade de IADs
topic_type:
- apiref
api_name:
- IADsGroup Property Methods
- IADsGroup.Description
- IADsGroup.get_Description
- IADsGroup.put_Description
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 665cb91a55298012e4e906c2972da5371e3960be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755902"
---
# <a name="iadsgroup-property-methods"></a><span data-ttu-id="045ef-104">Métodos de propriedade IADs</span><span class="sxs-lookup"><span data-stu-id="045ef-104">IADsGroup Property Methods</span></span>

<span data-ttu-id="045ef-105">Os métodos de propriedade da interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iadsgroup) lêem e gravam as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="045ef-105">The property methods of the [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) interface read and write the following properties.</span></span> <span data-ttu-id="045ef-106">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="045ef-106">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="045ef-107">Propriedades</span><span class="sxs-lookup"><span data-stu-id="045ef-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="045ef-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="045ef-108">**Description**</span></span>
<span data-ttu-id="045ef-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="045ef-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="045ef-110">Indica a descrição textual da Associação de grupo.</span><span class="sxs-lookup"><span data-stu-id="045ef-110">Indicates the textual description of the group membership.</span></span>

<dt>

<span data-ttu-id="045ef-111">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="045ef-111">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="045ef-112">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="045ef-112">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="045ef-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="045ef-113">Remarks</span></span>

### <a name="using-iadsgroup-to-retrieve-descriptions-of-built-in-groups"></a><span data-ttu-id="045ef-114">Usando o IADs para recuperar descrições de grupos internos</span><span class="sxs-lookup"><span data-stu-id="045ef-114">Using IADsGroup to Retrieve Descriptions of Built-in Groups</span></span>

<span data-ttu-id="045ef-115">Os exemplos a seguir mostram como recuperar informações sobre objetos de grupo do Windows por nome.</span><span class="sxs-lookup"><span data-stu-id="045ef-115">The following examples show how to retrieve information about Windows group objects by name.</span></span> <span data-ttu-id="045ef-116">Em um ambiente multilíngue, os grupos internos são, às vezes, conhecidos por diferentes nomes localizados, o que significa que eles não podem ser recuperados diretamente usando identificadores de cadeia de caracteres como "WinNT://Microsoft/Administrators".</span><span class="sxs-lookup"><span data-stu-id="045ef-116">In a multilingual environment, built-in groups are sometimes known by different localized names, which means that they cannot be retrieved directly by using string identifiers such as "WinNT://Microsoft/Administrators".</span></span> <span data-ttu-id="045ef-117">Nesse caso, o usuário pode se associar ao objeto SID conhecido para o grupo, recuperar o nome do grupo localizado e fornecê-lo ao método GetObject.</span><span class="sxs-lookup"><span data-stu-id="045ef-117">In that case, the user can bind to the well-known SID object for the group, retrieve the localized group name, and supply that to the GetObject method.</span></span> <span data-ttu-id="045ef-118">Para obter mais informações, consulte [SIDs conhecidos](/windows/desktop/SecAuthZ/well-known-sids).</span><span class="sxs-lookup"><span data-stu-id="045ef-118">For more information, see [Well-known SIDs](/windows/desktop/SecAuthZ/well-known-sids).</span></span>

## <a name="examples"></a><span data-ttu-id="045ef-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="045ef-119">Examples</span></span>

<span data-ttu-id="045ef-120">O exemplo a seguir Visual Basic mostra como associar a um objeto de grupo e exibir a descrição do grupo.</span><span class="sxs-lookup"><span data-stu-id="045ef-120">The following Visual Basic example shows how to bind to a group object and display the description of the group.</span></span>


```VB
Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("WinNT://Microsoft/Administrators")
Debug.Print grp.Description

Cleanup
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
```



<span data-ttu-id="045ef-121">O exemplo de C++ a seguir mostra como associar a um objeto de grupo e exibir a descrição do grupo.</span><span class="sxs-lookup"><span data-stu-id="045ef-121">The following C++ example shows how to bind to a group object and display the description of the group.</span></span>


```C++
IADsGroup *pGroup = NULL;
HRESULT hr = S_OK;
LPWSTR adsPath = L"WinNT://localHost/Administrators";
BSTR bstr;

hr = ADsGetObject(adsPath,IID_IADsGroup,(void**)&pGroup);

if(FAILED(hr)) {goto Cleanup;}

hr = pGroup->get_Description(&bstr);
if(FAILED(hr)) {goto Cleanup;}

printf("Description: %S\n",bstr);

Cleanup:
    SysFreeString(bstr);
    if(pGroup) 
        pGroup->Release();

    return hr;
```



## <a name="requirements"></a><span data-ttu-id="045ef-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="045ef-122">Requirements</span></span>



| <span data-ttu-id="045ef-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="045ef-123">Requirement</span></span> | <span data-ttu-id="045ef-124">Valor</span><span class="sxs-lookup"><span data-stu-id="045ef-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="045ef-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="045ef-125">Minimum supported client</span></span><br/> | <span data-ttu-id="045ef-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="045ef-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="045ef-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="045ef-127">Minimum supported server</span></span><br/> | <span data-ttu-id="045ef-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="045ef-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="045ef-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="045ef-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="045ef-130"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="045ef-130"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="045ef-131">DLL</span><span class="sxs-lookup"><span data-stu-id="045ef-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="045ef-132"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="045ef-132"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="045ef-133">IID</span><span class="sxs-lookup"><span data-stu-id="045ef-133">IID</span></span><br/>                      | <span data-ttu-id="045ef-134">\_O IID IADs é definido como 27636B00-410f-11CF-B1FF-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="045ef-134">IID\_IADsGroup is defined as 27636B00-410F-11CF-B1FF-02608C9E7553</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="045ef-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="045ef-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="045ef-136">**IADs**</span><span class="sxs-lookup"><span data-stu-id="045ef-136">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[<span data-ttu-id="045ef-137">**IADs**</span><span class="sxs-lookup"><span data-stu-id="045ef-137">**IADsGroup**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsgroup)
</dt> <dt>

[<span data-ttu-id="045ef-138">Métodos de propriedade de interface</span><span class="sxs-lookup"><span data-stu-id="045ef-138">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

