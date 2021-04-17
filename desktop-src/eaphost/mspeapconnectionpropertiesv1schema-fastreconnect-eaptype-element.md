---
title: Elemento FastReconnect (EapType)
description: Saiba mais sobre o elemento FastReconnect (EapType). Esse elemento indica se uma reconexão rápida deve ser executada.
ms.assetid: 075285b0-7b1b-4d3c-af27-a718f3c20394
keywords:
- Elemento FastReconnect EAPHost
topic_type:
- apiref
api_name:
- FastReconnect
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2214519db68b8c95b0e0efa91d68a7cd667b5f87
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105764058"
---
# <a name="fastreconnect-eaptype-element"></a><span data-ttu-id="5a70a-105">Elemento FastReconnect (EapType)</span><span class="sxs-lookup"><span data-stu-id="5a70a-105">FastReconnect (EapType) Element</span></span>

<span data-ttu-id="5a70a-106">O elemento **FastReconnect (EapType)** indica se uma reconexão rápida deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="5a70a-106">The **FastReconnect (EapType)** element indicates whether to perform a fast reconnect.</span></span>

``` syntax
<xs:element name="FastReconnect"
    type="boolean"
 />
```

<span data-ttu-id="5a70a-107">O elemento **FastReconnect** é definido pelo elemento [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5a70a-107">The **FastReconnect** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a70a-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a70a-108">Remarks</span></span>

<span data-ttu-id="5a70a-109">Se o elemento **FastReconnect** for true, o PEAP tentará executar uma reconexão rápida; Se for FALSE, o PEAP executará a autenticação completa.</span><span class="sxs-lookup"><span data-stu-id="5a70a-109">If the **FastReconnect** element is TRUE, then PEAP attempts to perform a fast reconnect; if FALSE, PEAP performs the full authentication.</span></span> <span data-ttu-id="5a70a-110">O elemento **FastReconnect** é opcional.</span><span class="sxs-lookup"><span data-stu-id="5a70a-110">The **FastReconnect** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a70a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a70a-111">Requirements</span></span>



| <span data-ttu-id="5a70a-112">Função</span><span class="sxs-lookup"><span data-stu-id="5a70a-112">Role</span></span> | <span data-ttu-id="5a70a-113">Versão mínima do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="5a70a-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="5a70a-114">Cliente</span><span class="sxs-lookup"><span data-stu-id="5a70a-114">Client</span></span><br/> | <span data-ttu-id="5a70a-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5a70a-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5a70a-116">Servidor</span><span class="sxs-lookup"><span data-stu-id="5a70a-116">Server</span></span><br/> | <span data-ttu-id="5a70a-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5a70a-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5a70a-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a70a-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="5a70a-119">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="5a70a-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="5a70a-120">**EapType**</span><span class="sxs-lookup"><span data-stu-id="5a70a-120">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="5a70a-121">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="5a70a-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="5a70a-122">**EapType**</span><span class="sxs-lookup"><span data-stu-id="5a70a-122">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="5a70a-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="5a70a-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="5a70a-124">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="5a70a-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="5a70a-125">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="5a70a-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="5a70a-126">Elementos do esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="5a70a-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





