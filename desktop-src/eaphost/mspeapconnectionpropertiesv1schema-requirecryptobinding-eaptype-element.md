---
title: Elemento RequireCryptoBinding (EapType)
description: Indica se é para autenticar com servidores que dão suporte a cryptobinding.
ms.assetid: 6b6a131d-8fce-4a5c-a649-891c4617b0f2
keywords:
- Elemento RequireCryptoBinding EAPHost
topic_type:
- apiref
api_name:
- RequireCryptoBinding
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 63ee456f87205346a935ad047cb8db9828febba6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369829"
---
# <a name="requirecryptobinding-eaptype-element"></a><span data-ttu-id="3038d-104">Elemento RequireCryptoBinding (EapType)</span><span class="sxs-lookup"><span data-stu-id="3038d-104">RequireCryptoBinding (EapType) Element</span></span>

<span data-ttu-id="3038d-105">O elemento **RequireCryptoBinding (EapType)** indica se deve ser autenticado com servidores que dão suporte a cryptobinding.</span><span class="sxs-lookup"><span data-stu-id="3038d-105">The **RequireCryptoBinding (EapType)** element indicates whether to authenticate with servers that support cryptobinding.</span></span>

``` syntax
<xs:element name="RequireCryptoBinding"
    type="boolean"
 />
```

<span data-ttu-id="3038d-106">O elemento **RequireCryptoBinding** é definido pelo elemento [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3038d-106">The **RequireCryptoBinding** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="3038d-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="3038d-107">Remarks</span></span>

<span data-ttu-id="3038d-108">Se o elemento **RequireCryptoBinding** for true, o PEAP será autenticado com servidores que não dão suporte a cryptobinding; Se for FALSE, o PEAP será autenticado somente com servidores que dão suporte a cryptobinding.</span><span class="sxs-lookup"><span data-stu-id="3038d-108">If the **RequireCryptoBinding** element is TRUE, then PEAP will authenticate with servers that don't support cryptobinding; if FALSE, then PEAP will only authenticate with servers that support cryptobinding.</span></span> <span data-ttu-id="3038d-109">O elemento **RequireCryptoBinding** é opcional.</span><span class="sxs-lookup"><span data-stu-id="3038d-109">The **RequireCryptoBinding** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="3038d-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3038d-110">Requirements</span></span>



| <span data-ttu-id="3038d-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="3038d-111">Requirement</span></span> | <span data-ttu-id="3038d-112">Valor</span><span class="sxs-lookup"><span data-stu-id="3038d-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3038d-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3038d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="3038d-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3038d-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3038d-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3038d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="3038d-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3038d-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3038d-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="3038d-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="3038d-118">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="3038d-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3038d-119">**EapType**</span><span class="sxs-lookup"><span data-stu-id="3038d-119">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="3038d-120">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="3038d-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3038d-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="3038d-121">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="3038d-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="3038d-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="3038d-123">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="3038d-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="3038d-124">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="3038d-124">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="3038d-125">Elementos do esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="3038d-125">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





