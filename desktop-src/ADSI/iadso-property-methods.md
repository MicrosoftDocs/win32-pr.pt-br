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
# <a name="iadso-property-methods"></a><span data-ttu-id="35d35-105">Métodos de propriedade IADso</span><span class="sxs-lookup"><span data-stu-id="35d35-105">IADsO Property Methods</span></span>

<span data-ttu-id="35d35-106">Os métodos de propriedade da interface [**iadso**](/windows/desktop/api/Iads/nn-iads-iadso) obtêm ou definem as propriedades descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="35d35-106">The property methods of the [**IADsO**](/windows/desktop/api/Iads/nn-iads-iadso) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="35d35-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="35d35-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="35d35-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="35d35-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="35d35-109">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="35d35-109">**Description**</span></span>
<span data-ttu-id="35d35-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="35d35-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="35d35-111">A descrição da organização.</span><span class="sxs-lookup"><span data-stu-id="35d35-111">The description of the organization.</span></span>

<dt>

<span data-ttu-id="35d35-112">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="35d35-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35d35-113">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="35d35-113">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="35d35-114">**FaxNumber**</span><span class="sxs-lookup"><span data-stu-id="35d35-114">**FaxNumber**</span></span>
<span data-ttu-id="35d35-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="35d35-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="35d35-116">O número de faxes (fax) da organização.</span><span class="sxs-lookup"><span data-stu-id="35d35-116">The facsimile (fax) number of the organization.</span></span>

<dt>

<span data-ttu-id="35d35-117">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="35d35-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35d35-118">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="35d35-118">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="35d35-119">**LocalityName**</span><span class="sxs-lookup"><span data-stu-id="35d35-119">**LocalityName**</span></span>
<span data-ttu-id="35d35-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="35d35-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="35d35-121">O nome do local em que a organização está localizada.</span><span class="sxs-lookup"><span data-stu-id="35d35-121">The name of the place in which the organization is located.</span></span>

<dt>

<span data-ttu-id="35d35-122">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="35d35-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35d35-123">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="35d35-123">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="35d35-124">**PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="35d35-124">**PostalAddress**</span></span>
<span data-ttu-id="35d35-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="35d35-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="35d35-126">O endereço postal da organização.</span><span class="sxs-lookup"><span data-stu-id="35d35-126">The postal address of the organization.</span></span>

<dt>

<span data-ttu-id="35d35-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="35d35-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35d35-128">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="35d35-128">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="35d35-129">**SeeAlso**</span><span class="sxs-lookup"><span data-stu-id="35d35-129">**SeeAlso**</span></span>
<span data-ttu-id="35d35-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="35d35-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="35d35-131">Uma matriz de nomes ADsPath de outros objetos ADSI que podem ser relevantes para esse objeto.</span><span class="sxs-lookup"><span data-stu-id="35d35-131">An array of ADsPath names of other ADSI objects which may be relevant to this object.</span></span>

<dt>

<span data-ttu-id="35d35-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="35d35-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35d35-133">Tipo de dados de script: **Variant**</span><span class="sxs-lookup"><span data-stu-id="35d35-133">Scripting data type: **VARIANT**</span></span>
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

<span data-ttu-id="35d35-134">**TelephoneNumber**</span><span class="sxs-lookup"><span data-stu-id="35d35-134">**TelephoneNumber**</span></span>
<span data-ttu-id="35d35-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="35d35-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="35d35-136">O número de telefone da organização.</span><span class="sxs-lookup"><span data-stu-id="35d35-136">The telephone number of the organization.</span></span>

<dt>

<span data-ttu-id="35d35-137">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="35d35-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35d35-138">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="35d35-138">Scripting data type: **BSTR**</span></span>
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

 

## <a name="examples"></a><span data-ttu-id="35d35-139">Exemplos</span><span class="sxs-lookup"><span data-stu-id="35d35-139">Examples</span></span>

<span data-ttu-id="35d35-140">O exemplo de código a seguir exibe a descrição de uma determinada organização.</span><span class="sxs-lookup"><span data-stu-id="35d35-140">The following code example displays the description of a given organization.</span></span> <span data-ttu-id="35d35-141">Ele assume que o serviço de diretório subjacente dá suporte ao agrupamento de objetos de diretório por organização.</span><span class="sxs-lookup"><span data-stu-id="35d35-141">It assumes the underlying directory service supports grouping directory objects by organization.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="35d35-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35d35-142">Requirements</span></span>



| <span data-ttu-id="35d35-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="35d35-143">Requirement</span></span> | <span data-ttu-id="35d35-144">Valor</span><span class="sxs-lookup"><span data-stu-id="35d35-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35d35-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35d35-145">Minimum supported client</span></span><br/> | <span data-ttu-id="35d35-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35d35-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="35d35-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35d35-147">Minimum supported server</span></span><br/> | <span data-ttu-id="35d35-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35d35-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="35d35-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="35d35-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="35d35-150"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="35d35-150"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="35d35-151">DLL</span><span class="sxs-lookup"><span data-stu-id="35d35-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35d35-152"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35d35-152"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="35d35-153">IID</span><span class="sxs-lookup"><span data-stu-id="35d35-153">IID</span></span><br/>                      | <span data-ttu-id="35d35-154">IID \_ iadso é definido como A1CD2DC6-EFFE-11CF-8ABC-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="35d35-154">IID\_IADsO is defined as A1CD2DC6-EFFE-11CF-8ABC-00C04FD8D503</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="35d35-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="35d35-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35d35-156">**IADso**</span><span class="sxs-lookup"><span data-stu-id="35d35-156">**IADsO**</span></span>](/windows/desktop/api/Iads/nn-iads-iadso)
</dt> <dt>

[<span data-ttu-id="35d35-157">Métodos de propriedade de interface</span><span class="sxs-lookup"><span data-stu-id="35d35-157">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





