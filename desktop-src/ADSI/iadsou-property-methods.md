---
title: Métodos de propriedade IADsOU (IADs. h)
description: Os métodos de propriedade da interface IADsOU obtêm ou definem as propriedades listadas na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: 8cb84972-733b-47ca-8647-1b7a85c97021
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsOU
topic_type:
- apiref
api_name:
- IADsOU Property Methods
- IADsOU.BusinessCategory
- IADsOU.get_BusinessCategory
- IADsOU.put_BusinessCategory
- IADsOU.Description
- IADsOU.get_Description
- IADsOU.put_Description
- IADsOU.FaxNumber
- IADsOU.get_FaxNumber
- IADsOU.put_FaxNumber
- IADsOU.LocalityName
- IADsOU.get_LocalityName
- IADsOU.put_LocalityName
- IADsOU.PostalAddress
- IADsOU.get_PostalAddress
- IADsOU.put_PostalAddress
- IADsOU.TelephoneNumber
- IADsOU.get_TelephoneNumber
- IADsOU.put_TelephoneNumber
- IADsOU.SeeAlso
- IADsOU.get_SeeAlso
- IADsOU.put_SeeAlso
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0ce30fad6a690a26a8e16b817b77b129dee25f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753617"
---
# <a name="iadsou-property-methods"></a><span data-ttu-id="5be68-105">Métodos de propriedade IADsOU</span><span class="sxs-lookup"><span data-stu-id="5be68-105">IADsOU Property Methods</span></span>

<span data-ttu-id="5be68-106">Os métodos de propriedade da interface [**IADsOU**](/windows/desktop/api/Iads/nn-iads-iadsou) obtêm ou definem as propriedades listadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5be68-106">The property methods of the [**IADsOU**](/windows/desktop/api/Iads/nn-iads-iadsou) interface get or set the properties listed in the following table.</span></span> <span data-ttu-id="5be68-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="5be68-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="5be68-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5be68-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="5be68-109">**BusinessCategory**</span><span class="sxs-lookup"><span data-stu-id="5be68-109">**BusinessCategory**</span></span>
<span data-ttu-id="5be68-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5be68-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="5be68-111">Uma cadeia de caracteres que contém a função comercial geral ou funções executadas pela unidade organizacional, por exemplo "contabilidade".</span><span class="sxs-lookup"><span data-stu-id="5be68-111">A string that contains the general business function or functions performed by the organizational unit, for example "Accounting".</span></span>

<dt>

<span data-ttu-id="5be68-112">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5be68-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5be68-113">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5be68-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BusinessCategory(
  [out] BSTR* pbstrBusinessCategory
);
HRESULT put_BusinessCategory(
  [in] BSTR bstrBusinessCategory
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="5be68-114">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5be68-114">**Description**</span></span>
<span data-ttu-id="5be68-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5be68-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="5be68-116">Uma cadeia de caracteres que contém uma descrição textual da unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="5be68-116">A string that contains a textual description of the organizational unit.</span></span>

<dt>

<span data-ttu-id="5be68-117">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5be68-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5be68-118">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5be68-118">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="5be68-119">**FaxNumber**</span><span class="sxs-lookup"><span data-stu-id="5be68-119">**FaxNumber**</span></span>
<span data-ttu-id="5be68-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5be68-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="5be68-121">Uma cadeia de caracteres que contém o número de fax da unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="5be68-121">A string that contains the facsimile number of the organizational unit.</span></span>

<dt>

<span data-ttu-id="5be68-122">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5be68-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5be68-123">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5be68-123">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="5be68-124">**LocalityName**</span><span class="sxs-lookup"><span data-stu-id="5be68-124">**LocalityName**</span></span>
<span data-ttu-id="5be68-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5be68-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="5be68-126">Uma cadeia de caracteres que contém o nome da região geográfica da unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="5be68-126">A string that contains the name of the geographic region of the organizational unit.</span></span>

<dt>

<span data-ttu-id="5be68-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5be68-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5be68-128">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5be68-128">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="5be68-129">**PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="5be68-129">**PostalAddress**</span></span>
<span data-ttu-id="5be68-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5be68-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="5be68-131">Uma cadeia de caracteres que contém o endereço postal da unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="5be68-131">A string that contains the postal address of the organizational unit.</span></span>

<dt>

<span data-ttu-id="5be68-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5be68-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5be68-133">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5be68-133">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="5be68-134">**SeeAlso**</span><span class="sxs-lookup"><span data-stu-id="5be68-134">**SeeAlso**</span></span>
<span data-ttu-id="5be68-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5be68-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="5be68-136">Uma matriz de cadeias de caracteres que contém os nomes distintos de outros objetos de diretório que podem ser relevantes para esse objeto.</span><span class="sxs-lookup"><span data-stu-id="5be68-136">An array of strings that contains the distinguished names of other directory objects which may be relevant to this object.</span></span>

<dt>

<span data-ttu-id="5be68-137">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5be68-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5be68-138">Tipo de dados de script: **Variant**</span><span class="sxs-lookup"><span data-stu-id="5be68-138">Scripting data type: **VARIANT**</span></span>
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

<span data-ttu-id="5be68-139">**TelephoneNumber**</span><span class="sxs-lookup"><span data-stu-id="5be68-139">**TelephoneNumber**</span></span>
<span data-ttu-id="5be68-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5be68-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="5be68-141">Uma cadeia de caracteres que contém o número de telefone da unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="5be68-141">A string that contains the telephone number of the organizational unit.</span></span>

<dt>

<span data-ttu-id="5be68-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5be68-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5be68-143">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5be68-143">Scripting data type: **BSTR**</span></span>
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

 

## <a name="examples"></a><span data-ttu-id="5be68-144">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5be68-144">Examples</span></span>

<span data-ttu-id="5be68-145">O exemplo de código a seguir exibe o **BusinessCategory** e a **Descrição** de todas as unidades organizacionais em um contêiner.</span><span class="sxs-lookup"><span data-stu-id="5be68-145">The following code example displays the **BusinessCategory** and **Description** of all organization units in a container.</span></span> <span data-ttu-id="5be68-146">Ele pressupõe que o serviço de diretório subjacente dá suporte ao agrupamento de objetos de diretório por unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="5be68-146">It assumes that the underlying directory service supports grouping of directory objects by organization unit.</span></span>


```VB
Dim dom As IADsContainer
Dim ou As IADsOU

' Bind to the container.
Set dom = GetObject("LDAP://server1/domain1")

' Filter out all objects that are not of class "organizationalUnit".
dom.filter = Array("organizationalUnit")

' Enumerate the organizational units in the container and display  
' the BusinessCategory and Description properties of each OU.
For Each ou In dom
    MsgBox ou.BusinessCategory & ": " & ou.Description
Next
```



## <a name="requirements"></a><span data-ttu-id="5be68-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5be68-147">Requirements</span></span>



| <span data-ttu-id="5be68-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="5be68-148">Requirement</span></span> | <span data-ttu-id="5be68-149">Valor</span><span class="sxs-lookup"><span data-stu-id="5be68-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5be68-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5be68-150">Minimum supported client</span></span><br/> | <span data-ttu-id="5be68-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5be68-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5be68-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5be68-152">Minimum supported server</span></span><br/> | <span data-ttu-id="5be68-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5be68-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5be68-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5be68-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="5be68-155"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="5be68-155"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="5be68-156">DLL</span><span class="sxs-lookup"><span data-stu-id="5be68-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5be68-157"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5be68-157"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="5be68-158">IID</span><span class="sxs-lookup"><span data-stu-id="5be68-158">IID</span></span><br/>                      | <span data-ttu-id="5be68-159">IID \_ IADsOU é definido como A2F733B8-EFFE-11CF-8ABC-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="5be68-159">IID\_IADsOU is defined as A2F733B8-EFFE-11CF-8ABC-00C04FD8D503</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="5be68-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="5be68-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5be68-161">**IADsOU**</span><span class="sxs-lookup"><span data-stu-id="5be68-161">**IADsOU**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsou)
</dt> <dt>

[<span data-ttu-id="5be68-162">Métodos de propriedade de interface</span><span class="sxs-lookup"><span data-stu-id="5be68-162">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





