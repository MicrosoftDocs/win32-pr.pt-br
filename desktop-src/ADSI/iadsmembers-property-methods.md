---
title: Métodos de propriedade IADsMembers (IADs. h)
description: Os métodos da interface IADsMembers lêem e gravam as propriedades descritas neste tópico. Para obter mais informações, consulte interface Property Methods.
ms.assetid: ed4e98e5-053c-4d3b-bcd0-3add96bbe120
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsMembers
topic_type:
- apiref
api_name:
- IADsMembers Property Methods
- IADsMembers.Count
- IADsMembers.get_Count
- IADsMembers.Filter
- IADsMembers.get_Filter
- IADsMembers.put_Filter
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af047d6fe52fdd7d808b1d7e5dbfb35303d3ff59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105750980"
---
# <a name="iadsmembers-property-methods"></a><span data-ttu-id="3411d-105">Métodos de propriedade IADsMembers</span><span class="sxs-lookup"><span data-stu-id="3411d-105">IADsMembers Property Methods</span></span>

<span data-ttu-id="3411d-106">Os métodos da interface [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) lêem e gravam as propriedades descritas neste tópico.</span><span class="sxs-lookup"><span data-stu-id="3411d-106">The methods of the [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) interface read and write the properties described in this topic.</span></span> <span data-ttu-id="3411d-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="3411d-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="3411d-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3411d-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="3411d-109">**Count**</span><span class="sxs-lookup"><span data-stu-id="3411d-109">**Count**</span></span>
<span data-ttu-id="3411d-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3411d-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="3411d-111">Indica o número de itens no contêiner.</span><span class="sxs-lookup"><span data-stu-id="3411d-111">Indicates the number of items in the container.</span></span> <span data-ttu-id="3411d-112">Se o filtro for definido, Count retornará apenas o número de itens que se ajustam à descrição do filtro.</span><span class="sxs-lookup"><span data-stu-id="3411d-112">If the filter is set then count returns only the number of items that fit the filter description.</span></span>

<dt>

<span data-ttu-id="3411d-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3411d-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3411d-114">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="3411d-114">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* plCountr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="3411d-115">**Filter**</span><span class="sxs-lookup"><span data-stu-id="3411d-115">**Filter**</span></span>
<span data-ttu-id="3411d-116"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3411d-116"></dt> <dd> <dl></span></span>

<span data-ttu-id="3411d-117">Indica o filtro.</span><span class="sxs-lookup"><span data-stu-id="3411d-117">Indicates the filter.</span></span> <span data-ttu-id="3411d-118">A sintaxe das entradas na matriz de filtro é igual ao filtro usado na interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="3411d-118">The syntax of the entries in the filter array is the same as the Filter used on the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface.</span></span>

<dt>

<span data-ttu-id="3411d-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3411d-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3411d-120">Tipo de dados de script: **Variant**</span><span class="sxs-lookup"><span data-stu-id="3411d-120">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Filter(
  [out] VARIANT* pvFilter
);
HRESULT put_Filter(
  [in] VARIANT vFilter
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="3411d-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="3411d-121">Remarks</span></span>

<span data-ttu-id="3411d-122">Os provedores de sistema ADSI não dão suporte ao método de propriedade de **\_ contagem IADsMembers:: Get** .</span><span class="sxs-lookup"><span data-stu-id="3411d-122">The ADSI system providers do not support the **IADsMembers::get\_Count** property method.</span></span>

## <a name="examples"></a><span data-ttu-id="3411d-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3411d-123">Examples</span></span>

<span data-ttu-id="3411d-124">O exemplo de código a seguir mostra como usar os métodos de propriedade dessa interface.</span><span class="sxs-lookup"><span data-stu-id="3411d-124">The following code example shows how to use the property methods of this interface.</span></span>


```VB
Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("WinNT://myComputer/someGroup")
grp.members.filter = Array("user")
For Each usr In grp.Members
    MsgBox usr.Name & "," & usr.Class & "," & usr.AdsPath
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
```



<span data-ttu-id="3411d-125">O exemplo de código a seguir usa o método de **\_ filtro IADsMembers::p UT** para se preparar para uma enumeração da coleção de membros de um grupo.</span><span class="sxs-lookup"><span data-stu-id="3411d-125">The following code example uses the **IADsMembers::put\_Filter** method to prepare for an enumeration of the collection of members of a group.</span></span>


```C++
IADsGroup *pGroup;
HRESULT hr = S_OK;

LPWSTR grpPath = L"WinNT://myComputer/someGroup";
hr = ADsGetObject(grpPath,IID_IADsGroup,(void**)&pGroup);
if(FAILED(hr)){goto Cleanup;}

IADsMembers *pMembers;
hr = pGroup->Members(&pMembers);
if(FAILED(hr)){goto Cleanup;}

hr = pGroup->Release();

SAFEARRAY *sa = CreateSafeArray(L"user");
hr = pMembers->put_Filter(sa);
if(FAILED(hr)){goto Cleanup;}

hr = EnumMembers(pMembers);    // For more information, and a 
                               // code example, see 
                               // IADsMembers::get__NewEnum.
if(FAILED(hr)){goto Cleanup;}

Cleanup:
    if(pGroup) pGroup->Release();
    if(pMembers) pMembers->Release();
    return hr;
```



## <a name="requirements"></a><span data-ttu-id="3411d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3411d-126">Requirements</span></span>



| <span data-ttu-id="3411d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3411d-127">Requirement</span></span> | <span data-ttu-id="3411d-128">Valor</span><span class="sxs-lookup"><span data-stu-id="3411d-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3411d-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3411d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3411d-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3411d-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3411d-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3411d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3411d-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3411d-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3411d-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3411d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3411d-134"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="3411d-134"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="3411d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3411d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3411d-136"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3411d-136"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="3411d-137">IID</span><span class="sxs-lookup"><span data-stu-id="3411d-137">IID</span></span><br/>                      | <span data-ttu-id="3411d-138">IID \_ IADsMembers é definido como 451A0030-72EC-11CF-B03B-00AA006E0975</span><span class="sxs-lookup"><span data-stu-id="3411d-138">IID\_IADsMembers is defined as 451A0030-72EC-11CF-B03B-00AA006E0975</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="3411d-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="3411d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3411d-140">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="3411d-140">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> <dt>

[<span data-ttu-id="3411d-141">**IADsMembers:: obter \_ \_ NewEnum**</span><span class="sxs-lookup"><span data-stu-id="3411d-141">**IADsMembers::get\_\_NewEnum**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsmembers-get__newenum)
</dt> <dt>

[<span data-ttu-id="3411d-142">**IADsMembers**</span><span class="sxs-lookup"><span data-stu-id="3411d-142">**IADsMembers**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsmembers)
</dt> <dt>

[<span data-ttu-id="3411d-143">Métodos de propriedade de interface</span><span class="sxs-lookup"><span data-stu-id="3411d-143">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





