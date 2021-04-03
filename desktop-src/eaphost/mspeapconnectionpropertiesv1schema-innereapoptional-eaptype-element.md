---
title: Elemento InnerEapOptional (EapType)
description: Saiba mais sobre o elemento InnerEapOptional (EapType). Este elemento indica se o acesso de convidado deve ser realizado.
ms.assetid: 2d314c89-5415-407f-84c3-c4c5c8957b39
keywords:
- Elemento InnerEapOptional EAPHost
topic_type:
- apiref
api_name:
- InnerEapOptional
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be63845f389936656172b4cbb4e42de659bbf0e1
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084890"
---
# <a name="innereapoptional-eaptype-element"></a><span data-ttu-id="aa409-105">Elemento InnerEapOptional (EapType)</span><span class="sxs-lookup"><span data-stu-id="aa409-105">InnerEapOptional (EapType) Element</span></span>

<span data-ttu-id="aa409-106">O elemento **InnerEapOptional (EapType)** indica se o acesso ao convidado deve ser realizado.</span><span class="sxs-lookup"><span data-stu-id="aa409-106">The **InnerEapOptional (EapType)** element indicates whether to perform GUEST access.</span></span>

``` syntax
<xs:element name="InnerEapOptional"
    type="boolean"
 />
```

<span data-ttu-id="aa409-107">O elemento **InnerEapOptional** é definido pelo elemento [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="aa409-107">The **InnerEapOptional** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa409-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa409-108">Remarks</span></span>

<span data-ttu-id="aa409-109">Se o elemento **InnerEapOptional** for true, o elemento [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) deverá estar presente e descrever o método interno e sua configuração; Se for FALSE, o PEAP executará o acesso de convidado.</span><span class="sxs-lookup"><span data-stu-id="aa409-109">If the **InnerEapOptional** element is TRUE, then the [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) element must be present and describe the inner method and it's configuration; if FALSE, then PEAP will perform GUEST access.</span></span> <span data-ttu-id="aa409-110">O elemento **InnerEapOptional** é opcional.</span><span class="sxs-lookup"><span data-stu-id="aa409-110">The **InnerEapOptional** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa409-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa409-111">Requirements</span></span>



| <span data-ttu-id="aa409-112">Função</span><span class="sxs-lookup"><span data-stu-id="aa409-112">Role</span></span> | <span data-ttu-id="aa409-113">Versão mínima do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="aa409-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="aa409-114">Cliente</span><span class="sxs-lookup"><span data-stu-id="aa409-114">Client</span></span><br/> | <span data-ttu-id="aa409-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aa409-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="aa409-116">Servidor</span><span class="sxs-lookup"><span data-stu-id="aa409-116">Server</span></span><br/> | <span data-ttu-id="aa409-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aa409-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aa409-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa409-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="aa409-119">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="aa409-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="aa409-120">**EapType**</span><span class="sxs-lookup"><span data-stu-id="aa409-120">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="aa409-121">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="aa409-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="aa409-122">**EapType**</span><span class="sxs-lookup"><span data-stu-id="aa409-122">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="aa409-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="aa409-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="aa409-124">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="aa409-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="aa409-125">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="aa409-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="aa409-126">Elementos do esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="aa409-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





