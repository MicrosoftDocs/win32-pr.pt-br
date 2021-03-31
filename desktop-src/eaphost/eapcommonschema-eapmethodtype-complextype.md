---
title: Tipo complexo EapMethodType
description: Define os elementos que identificam exclusivamente um único tipo de método EAP, VendorID, VendorID e AuthorId.
ms.assetid: 3ef96187-7376-438d-9d47-a87d5a6c9b8b
keywords:
- EapMethodType tipo complexo EAPHost
topic_type:
- apiref
api_name:
- EapMethodType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cea2448111266696398d1581aaecdbec2fb5859e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644735"
---
# <a name="eapmethodtype-complex-type"></a><span data-ttu-id="b3283-104">Tipo complexo EapMethodType</span><span class="sxs-lookup"><span data-stu-id="b3283-104">EapMethodType Complex Type</span></span>

<span data-ttu-id="b3283-105">O tipo complexo **EapMethodType** define os elementos que identificam exclusivamente um único método EAP: [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md), [**VendorName**](eapcommonschema-vendortype-eapmethodtype-element.md)e [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md).</span><span class="sxs-lookup"><span data-stu-id="b3283-105">The **EapMethodType** complex type defines the elements that uniquely identify a single EAP method: [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md), [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md), and [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md).</span></span>

<span data-ttu-id="b3283-106">[**Type**](eapcommonschema-type-eapmethodtype-element.md) e [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) são elementos obrigatórios, enquanto [**VendorName**](eapcommonschema-vendortype-eapmethodtype-element.md) e [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) são necessários somente quando o elemento **Type** é 254 (um método EAP expandido).</span><span class="sxs-lookup"><span data-stu-id="b3283-106">[**Type**](eapcommonschema-type-eapmethodtype-element.md) and [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) are mandatory elements, whereas [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) and [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) are required only when the **Type** element is 254 (an expanded EAP method).</span></span>

``` syntax
<xs:complexType name="EapMethodType">
    <xs:sequence>
        <xs:element name="Type"
            type="unsignedByte"
         />
        <xs:element name="VendorId"
            type="unsignedInt"
            default="0"
            minOccurs="0"
         />
        <xs:element name="VendorType"
            type="unsignedInt"
            default="0"
            minOccurs="0"
         />
        <xs:element name="AuthorId"
            type="unsignedInt"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="b3283-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="b3283-107">Child elements</span></span>



| <span data-ttu-id="b3283-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="b3283-108">Element</span></span>                                                                | <span data-ttu-id="b3283-109">Type</span><span class="sxs-lookup"><span data-stu-id="b3283-109">Type</span></span>         | <span data-ttu-id="b3283-110">Description</span><span class="sxs-lookup"><span data-stu-id="b3283-110">Description</span></span>                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b3283-111">**AuthorId**</span><span class="sxs-lookup"><span data-stu-id="b3283-111">**AuthorId**</span></span>](eapcommonschema-authorid-eapmethodtype-element.md)     | <span data-ttu-id="b3283-112">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b3283-112">unsignedInt</span></span>  | <span data-ttu-id="b3283-113">Refere-se ao autor do método.</span><span class="sxs-lookup"><span data-stu-id="b3283-113">Refers to the method author.</span></span> <br/>                                                                                                                                                                                                                 |
| [<span data-ttu-id="b3283-114">**Escreva**</span><span class="sxs-lookup"><span data-stu-id="b3283-114">**Type**</span></span>](eapcommonschema-type-eapmethodtype-element.md)             | <span data-ttu-id="b3283-115">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="b3283-115">unsignedByte</span></span> | <span data-ttu-id="b3283-116">Refere-se ao tipo de método EAP.</span><span class="sxs-lookup"><span data-stu-id="b3283-116">Refers to the EAP method type.</span></span> <br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="b3283-117">**VendorId**</span><span class="sxs-lookup"><span data-stu-id="b3283-117">**VendorId**</span></span>](eapcommonschema-vendorid-eapmethodtype-element.md)     | <span data-ttu-id="b3283-118">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b3283-118">unsignedInt</span></span>  | <span data-ttu-id="b3283-119">Refere-se ao fornecedor que definiu o método – se o elemento [**Type**](eapcommonschema-type-eapmethodtype-element.md) for 254 (um método EAP expandido).</span><span class="sxs-lookup"><span data-stu-id="b3283-119">Refers to the vendor who defined the method - if the [**Type**](eapcommonschema-type-eapmethodtype-element.md) element is 254 (an expanded EAP method).</span></span> <span data-ttu-id="b3283-120">O [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) é opcional.</span><span class="sxs-lookup"><span data-stu-id="b3283-120">The [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) is optional.</span></span> <br/> |
| [<span data-ttu-id="b3283-121">**Nome_do_Fornecedor**</span><span class="sxs-lookup"><span data-stu-id="b3283-121">**VendorType**</span></span>](eapcommonschema-vendortype-eapmethodtype-element.md) | <span data-ttu-id="b3283-122">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b3283-122">unsignedInt</span></span>  | <span data-ttu-id="b3283-123">É o tipo definido pelo fornecedor para o método.</span><span class="sxs-lookup"><span data-stu-id="b3283-123">Is the vendor defined type for the method.</span></span> <span data-ttu-id="b3283-124">O [**VendorName**](eapcommonschema-vendortype-eapmethodtype-element.md) é opcional.</span><span class="sxs-lookup"><span data-stu-id="b3283-124">The [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) is optional.</span></span> <br/>                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="b3283-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3283-125">Remarks</span></span>

<span data-ttu-id="b3283-126">Os elementos [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) e [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) não precisam ser os mesmos para um método específico.</span><span class="sxs-lookup"><span data-stu-id="b3283-126">The [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) and [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) elements do not need to be the same for a particular method.</span></span>

<span data-ttu-id="b3283-127">Os elementos [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md), [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) e [**VendorName**](eapcommonschema-vendortype-eapmethodtype-element.md) são cada um deles um número exclusivo emitido pela IANA (Internet Assigned Numbers Authority).</span><span class="sxs-lookup"><span data-stu-id="b3283-127">The [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md), [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) and [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) elements are each a unique number issued by the Internet Assigned Numbers Authority (IANA).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3283-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3283-128">Requirements</span></span>



| <span data-ttu-id="b3283-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3283-129">Requirement</span></span> | <span data-ttu-id="b3283-130">Valor</span><span class="sxs-lookup"><span data-stu-id="b3283-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b3283-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3283-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b3283-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b3283-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b3283-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3283-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b3283-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b3283-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b3283-135">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b3283-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3283-136">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="b3283-136">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="b3283-137">Esquema eapcommon</span><span class="sxs-lookup"><span data-stu-id="b3283-137">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





