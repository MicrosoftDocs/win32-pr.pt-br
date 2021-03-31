---
title: Métodos de propriedade IADso (IADs. h)
description: Os métodos de propriedade da interface IADso obtêm ou definem as propriedades descritas na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: d4bc1d29-98de-462d-b59c-2bc2641c25a0
ms.tgt_platform: multiple
keywords:
- ADSI dos métodos de propriedade IADso
topic_type:
- apiref
api_name:
- IADsO Property Methods
- IADsO.Description
- IADsO.get_Description
- IADsO.put_Description
- IADsO.FaxNumber
- IADsO.get_FaxNumber
- IADsO.put_FaxNumber
- IADsO.LocalityName
- IADsO.get_LocalityName
- IADsO.put_LocalityName
- IADsO.PostalAddress
- IADsO.get_PostalAddress
- IADsO.put_PostalAddress
- IADsO.TelephoneNumber
- IADsO.get_TelephoneNumber
- IADsO.put_TelephoneNumber
- IADsO.SeeAlso
- IADsO.get_SeeAlso
- IADsO.put_SeeAlso
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09840cf62d6883eb4f5ca326998b697a34698c90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644946"
---
# <a name="iadso-property-methods"></a><span data-ttu-id="b720c-105">Métodos de propriedade IADso</span><span class="sxs-lookup"><span data-stu-id="b720c-105">IADsO Property Methods</span></span>

<span data-ttu-id="b720c-106">Os métodos de propriedade da interface [**iadso**](/windows/desktop/api/Iads/nn-iads-iadso) obtêm ou definem as propriedades descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b720c-106">The property methods of the [**IADsO**](/windows/desktop/api/Iads/nn-iads-iadso) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="b720c-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="b720c-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="b720c-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b720c-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="b720c-109">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b720c-109">**Description**</span></span>
<span data-ttu-id="b720c-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b720c-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="b720c-111">A descrição da organização.</span><span class="sxs-lookup"><span data-stu-id="b720c-111">The description of the organization.</span></span>

<dt>

<span data-ttu-id="b720c-112">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b720c-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b720c-113">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b720c-113">Scripting data type: **BSTR**</span></span>
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


</dt> </dl> </dd> <dt>

<span data-ttu-id="b720c-114">**FaxNumber**</span><span class="sxs-lookup"><span data-stu-id="b720c-114">**FaxNumber**</span></span>
<span data-ttu-id="b720c-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b720c-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="b720c-116">O número de faxes (fax) da organização.</span><span class="sxs-lookup"><span data-stu-id="b720c-116">The facsimile (fax) number of the organization.</span></span>

<dt>

<span data-ttu-id="b720c-117">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b720c-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b720c-118">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b720c-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_FaxNumber(
  [out] BSTR* pbstrFaxNumber
);
HRESULT put_FaxNumber(
  [in] BSTR bstrFaxNumber
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="b720c-119">**LocalityName**</span><span class="sxs-lookup"><span data-stu-id="b720c-119">**LocalityName**</span></span>
<span data-ttu-id="b720c-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b720c-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="b720c-121">O nome do local em que a organização está localizada.</span><span class="sxs-lookup"><span data-stu-id="b720c-121">The name of the place in which the organization is located.</span></span>

<dt>

<span data-ttu-id="b720c-122">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b720c-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b720c-123">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b720c-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LocalityName(
  [out] BSTR* pbstrLocalityName
);
HRESULT put_LocalityName(
  [in] BSTR bstrLocalityName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="b720c-124">**PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="b720c-124">**PostalAddress**</span></span>
<span data-ttu-id="b720c-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b720c-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="b720c-126">O endereço postal da organização.</span><span class="sxs-lookup"><span data-stu-id="b720c-126">The postal address of the organization.</span></span>

<dt>

<span data-ttu-id="b720c-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b720c-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b720c-128">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b720c-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PostalAddress(
  [out] BSTR* pbstrPostalAddress
);
HRESULT put_PostalAddress(
  [in] BSTR bstrPostalAddress
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="b720c-129">**SeeAlso**</span><span class="sxs-lookup"><span data-stu-id="b720c-129">**SeeAlso**</span></span>
<span data-ttu-id="b720c-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b720c-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="b720c-131">Uma matriz de nomes ADsPath de outros objetos ADSI que podem ser relevantes para esse objeto.</span><span class="sxs-lookup"><span data-stu-id="b720c-131">An array of ADsPath names of other ADSI objects which may be relevant to this object.</span></span>

<dt>

<span data-ttu-id="b720c-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b720c-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b720c-133">Tipo de dados de script: **Variant**</span><span class="sxs-lookup"><span data-stu-id="b720c-133">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SeeAlso(
  [out] VARIANT* pvSeeAlso
);
HRESULT put_SeeAlso(
  [in] VARIANT vSeeAlso
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="b720c-134">**TelephoneNumber**</span><span class="sxs-lookup"><span data-stu-id="b720c-134">**TelephoneNumber**</span></span>
<span data-ttu-id="b720c-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b720c-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="b720c-136">O número de telefone da organização.</span><span class="sxs-lookup"><span data-stu-id="b720c-136">The telephone number of the organization.</span></span>

<dt>

<span data-ttu-id="b720c-137">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b720c-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b720c-138">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b720c-138">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TelephoneNumber(
  [out] BSTR* pbstrTelephoneNumber
);
HRESULT put_TelephoneNumber(
  [in] BSTR bstrTelephoneNumber
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="b720c-139">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b720c-139">Examples</span></span>

<span data-ttu-id="b720c-140">O exemplo de código a seguir exibe a descrição de uma determinada organização.</span><span class="sxs-lookup"><span data-stu-id="b720c-140">The following code example displays the description of a given organization.</span></span> <span data-ttu-id="b720c-141">Ele assume que o serviço de diretório subjacente dá suporte ao agrupamento de objetos de diretório por organização.</span><span class="sxs-lookup"><span data-stu-id="b720c-141">It assumes the underlying directory service supports grouping directory objects by organization.</span></span>


```VB
Dim dom As IADsContainer
Dim dso As IADsOpenDSObject
Dim szUsername As String
Dim szPassword As String
On Error GoTo Cleanup

' Insert code to securely retrieve the user name and password
 
Set dso = GetObject("LDAP:")
Set dom = dso.OpenDSObject("LDAP://adsrv1/dc=Fabrikam, dc=Com", _
                           szUsername, szPassword,1)
dom.Filter = Array("organization")
For Each o In dom
    MsgBox "Fax number of " & o.Name & " : " & o.Description
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set dom = Nothing
    Set dso = Nothing
```



## <a name="requirements"></a><span data-ttu-id="b720c-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b720c-142">Requirements</span></span>



| <span data-ttu-id="b720c-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="b720c-143">Requirement</span></span> | <span data-ttu-id="b720c-144">Valor</span><span class="sxs-lookup"><span data-stu-id="b720c-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b720c-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b720c-145">Minimum supported client</span></span><br/> | <span data-ttu-id="b720c-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b720c-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b720c-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b720c-147">Minimum supported server</span></span><br/> | <span data-ttu-id="b720c-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b720c-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b720c-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b720c-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="b720c-150"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="b720c-150"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="b720c-151">DLL</span><span class="sxs-lookup"><span data-stu-id="b720c-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b720c-152"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b720c-152"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="b720c-153">IID</span><span class="sxs-lookup"><span data-stu-id="b720c-153">IID</span></span><br/>                      | <span data-ttu-id="b720c-154">IID \_ iadso é definido como A1CD2DC6-EFFE-11CF-8ABC-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="b720c-154">IID\_IADsO is defined as A1CD2DC6-EFFE-11CF-8ABC-00C04FD8D503</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="b720c-155">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b720c-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b720c-156">**IADso**</span><span class="sxs-lookup"><span data-stu-id="b720c-156">**IADsO**</span></span>](/windows/desktop/api/Iads/nn-iads-iadso)
</dt> <dt>

[<span data-ttu-id="b720c-157">Métodos de propriedade de interface</span><span class="sxs-lookup"><span data-stu-id="b720c-157">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





