---
title: Métodos de propriedade IADsLocality (IADs. h)
description: Os métodos da interface IADsLocality lêem e gravam as propriedades descritas neste tópico. Para obter mais informações, consulte interface Property Methods.
ms.assetid: 5d1cea40-62fb-49d4-857f-4563e9db7f51
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsLocality
topic_type:
- apiref
api_name:
- IADsLocality Property Methods
- IADsLocality.Description
- IADsLocality.get_Description
- IADsLocality.put_Description
- IADsLocality.LocalityName
- IADsLocality.get_LocalityName
- IADsLocality.put_LocalityName
- IADsLocality.PostalAddress
- IADsLocality.get_PostalAddress
- IADsLocality.put_PostalAddress
- IADsLocality.SeeAlso
- IADsLocality.get_SeeAlso
- IADsLocality.put_SeeAlso
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34023f0af5365deb4f023d53a843dcf688c40afd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918890"
---
# <a name="iadslocality-property-methods"></a><span data-ttu-id="12f13-105">Métodos de propriedade IADsLocality</span><span class="sxs-lookup"><span data-stu-id="12f13-105">IADsLocality Property Methods</span></span>

<span data-ttu-id="12f13-106">Os métodos da interface [**IADsLocality**](/windows/desktop/api/Iads/nn-iads-iadslocality) lêem e gravam as propriedades descritas neste tópico.</span><span class="sxs-lookup"><span data-stu-id="12f13-106">The methods of the [**IADsLocality**](/windows/desktop/api/Iads/nn-iads-iadslocality) interface read and write the properties described in this topic.</span></span> <span data-ttu-id="12f13-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="12f13-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="12f13-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="12f13-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="12f13-109">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="12f13-109">**Description**</span></span>
<span data-ttu-id="12f13-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="12f13-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="12f13-111">Indica o texto que descreve a localidade.</span><span class="sxs-lookup"><span data-stu-id="12f13-111">Indicates the text that describes the locality.</span></span>

<dt>

<span data-ttu-id="12f13-112">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="12f13-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="12f13-113">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="12f13-113">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="12f13-114">**LocalityName**</span><span class="sxs-lookup"><span data-stu-id="12f13-114">**LocalityName**</span></span>
<span data-ttu-id="12f13-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="12f13-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="12f13-116">Indica o nome da região geográfica conforme representado por esse objeto de localidade.</span><span class="sxs-lookup"><span data-stu-id="12f13-116">Indicates the name of the geographical region as represented by this locality object.</span></span>

<dt>

<span data-ttu-id="12f13-117">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="12f13-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="12f13-118">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="12f13-118">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="12f13-119">**PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="12f13-119">**PostalAddress**</span></span>
<span data-ttu-id="12f13-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="12f13-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="12f13-121">Indica o endereço postal principal da localidade.</span><span class="sxs-lookup"><span data-stu-id="12f13-121">Indicates the main postal address of the locality.</span></span>

<dt>

<span data-ttu-id="12f13-122">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="12f13-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="12f13-123">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="12f13-123">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="12f13-124">**SeeAlso**</span><span class="sxs-lookup"><span data-stu-id="12f13-124">**SeeAlso**</span></span>
<span data-ttu-id="12f13-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="12f13-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="12f13-126">Indica uma matriz de nomes ADsPath de objetos de diretório relevantes para esse objeto.</span><span class="sxs-lookup"><span data-stu-id="12f13-126">Indicates an array of ADsPath names of directory objects relevant to this object.</span></span>

<dt>

<span data-ttu-id="12f13-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="12f13-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="12f13-128">Tipo de dados de script: **Variant**</span><span class="sxs-lookup"><span data-stu-id="12f13-128">Scripting data type: **VARIANT**</span></span>
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


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="12f13-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="12f13-129">Examples</span></span>

<span data-ttu-id="12f13-130">O exemplo de código a seguir exibe os dados de localidade de um objeto de contêiner.</span><span class="sxs-lookup"><span data-stu-id="12f13-130">The following code example displays the locality data of a container object.</span></span> <span data-ttu-id="12f13-131">Ele assume que um objeto de localidade, chamado "mylocality", foi criado para o objeto de contêiner e as propriedades foram definidas.</span><span class="sxs-lookup"><span data-stu-id="12f13-131">It assumes that a locality object, named "myLocality", has been created for the container object and the properties have been set.</span></span>


```VB
Dim dom As IADsContainer
Dim loc As IADsLocality
On Error GoTo Cleanup
 
Set dom = getObject("LDAP://adsrv1/dc=Fabrikam, dc=Com")
Set loc = dom.GetObject("locality","L=myLocality")
Debug.Print loc.Name
Debug.Print loc.LocalityName
Debug.Print loc.Description
Debug.Print loc.PostalAddress
Debug.Print loc.SeeAlso

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set dom = Nothing
    Set loc = Nothing
```



## <a name="requirements"></a><span data-ttu-id="12f13-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12f13-132">Requirements</span></span>



| <span data-ttu-id="12f13-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="12f13-133">Requirement</span></span> | <span data-ttu-id="12f13-134">Valor</span><span class="sxs-lookup"><span data-stu-id="12f13-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12f13-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12f13-135">Minimum supported client</span></span><br/> | <span data-ttu-id="12f13-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12f13-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="12f13-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12f13-137">Minimum supported server</span></span><br/> | <span data-ttu-id="12f13-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12f13-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="12f13-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12f13-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="12f13-140"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="12f13-140"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="12f13-141">DLL</span><span class="sxs-lookup"><span data-stu-id="12f13-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12f13-142"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12f13-142"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="12f13-143">IID</span><span class="sxs-lookup"><span data-stu-id="12f13-143">IID</span></span><br/>                      | <span data-ttu-id="12f13-144">IID \_ IADsLocality é definido como A05E03A2-EFFE-11CF-8ABC-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="12f13-144">IID\_IADsLocality is defined as A05E03A2-EFFE-11CF-8ABC-00C04FD8D503</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="12f13-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="12f13-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12f13-146">**IADs**</span><span class="sxs-lookup"><span data-stu-id="12f13-146">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[<span data-ttu-id="12f13-147">**IADsLocality**</span><span class="sxs-lookup"><span data-stu-id="12f13-147">**IADsLocality**</span></span>](/windows/desktop/api/Iads/nn-iads-iadslocality)
</dt> <dt>

[<span data-ttu-id="12f13-148">Métodos de propriedade de interface</span><span class="sxs-lookup"><span data-stu-id="12f13-148">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





