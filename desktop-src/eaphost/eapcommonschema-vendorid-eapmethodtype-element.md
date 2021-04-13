---
title: Elemento Vendor (EapMethodType)
description: Refere-se ao fornecedor que definiu o método se o elemento Type (EapMethodType) for 254 (um método EAP expandido).
ms.assetid: 14992940-2fe5-4f85-91c0-1f61345ee90f
keywords:
- Elemento Vendor EAPHost
topic_type:
- apiref
api_name:
- VendorId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9091cdbd7620baf6ec5dc893bd2100b2f04585ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499412"
---
# <a name="vendorid-eapmethodtype-element"></a><span data-ttu-id="b57f6-104">Elemento Vendor (EapMethodType)</span><span class="sxs-lookup"><span data-stu-id="b57f6-104">VendorId (EapMethodType) Element</span></span>

<span data-ttu-id="b57f6-105">O elemento **Vendor (EapMethodType)** refere-se ao fornecedor que definiu o método se o elemento [**Type (EapMethodType)**](eapcommonschema-type-eapmethodtype-element.md) for 254 (um método EAP expandido).</span><span class="sxs-lookup"><span data-stu-id="b57f6-105">The **VendorId (EapMethodType)** element refers to the vendor who defined the method if the [**Type (EapMethodType)**](eapcommonschema-type-eapmethodtype-element.md) element is 254 (an expanded EAP method).</span></span>

<span data-ttu-id="b57f6-106">O **VendorID** é opcional.</span><span class="sxs-lookup"><span data-stu-id="b57f6-106">The **VendorId** is optional.</span></span> <span data-ttu-id="b57f6-107">Se usado, o **VendorID** é um número exclusivo emitido pela IANA (Internet Assigned Numbers Authority).</span><span class="sxs-lookup"><span data-stu-id="b57f6-107">If used, the **VendorId** is a unique number issued by Internet Assigned Numbers Authority (IANA).</span></span>

``` syntax
<xs:element name="VendorId"
    type="unsignedInt"
 />
```

<span data-ttu-id="b57f6-108">O elemento **VendorID** é definido pelo tipo complexo [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b57f6-108">The **VendorId** element is defined by the [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="b57f6-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="b57f6-109">Remarks</span></span>

<span data-ttu-id="b57f6-110">Os elementos [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) e **VendorID** não precisam ser os mesmos para um método específico.</span><span class="sxs-lookup"><span data-stu-id="b57f6-110">The [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) and **VendorId** elements do not need to be the same for a particular method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b57f6-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b57f6-111">Requirements</span></span>



| <span data-ttu-id="b57f6-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="b57f6-112">Requirement</span></span> | <span data-ttu-id="b57f6-113">Valor</span><span class="sxs-lookup"><span data-stu-id="b57f6-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b57f6-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b57f6-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b57f6-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b57f6-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b57f6-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b57f6-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b57f6-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b57f6-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b57f6-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="b57f6-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="b57f6-119">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="b57f6-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b57f6-120">**EapMethodType**</span><span class="sxs-lookup"><span data-stu-id="b57f6-120">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[<span data-ttu-id="b57f6-121">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="b57f6-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="b57f6-122">Esquema eapcommon</span><span class="sxs-lookup"><span data-stu-id="b57f6-122">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





