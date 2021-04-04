---
title: Elemento EnableQuarantineChecks (EapType)
description: Saiba mais sobre o elemento EnableQuarantineChecks (EapType). Esse elemento indica se as verificações de NAP (proteção de acesso à rede) devem ser executadas.
ms.assetid: bd5c7efc-f857-4e21-9cd8-0a1cbe5a87d8
keywords:
- Elemento EnableQuarantineChecks EAPHost
topic_type:
- apiref
api_name:
- EnableQuarantineChecks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0becd1add038bb91307095eaf5cd0743d383632b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917696"
---
# <a name="enablequarantinechecks-eaptype-element"></a><span data-ttu-id="fd09b-105">Elemento EnableQuarantineChecks (EapType)</span><span class="sxs-lookup"><span data-stu-id="fd09b-105">EnableQuarantineChecks (EapType) Element</span></span>

<span data-ttu-id="fd09b-106">O elemento **EnableQuarantineChecks (EapType)** indica se as verificações de NAP (proteção de acesso à rede) devem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="fd09b-106">The **EnableQuarantineChecks (EapType)** element indicates whether to perform Network Access Protection (NAP) checks.</span></span>

``` syntax
<xs:element name="EnableQuarantineChecks"
    type="boolean"
 />
```

<span data-ttu-id="fd09b-107">O elemento **EnableQuarantineChecks** é definido pelo elemento [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="fd09b-107">The **EnableQuarantineChecks** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd09b-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd09b-108">Remarks</span></span>

<span data-ttu-id="fd09b-109">Se o elemento **EnableQuarantineChecks** for true, o PEAP executará verificações de NAP; Se for FALSE, o PEAP não executará verificações de NAP.</span><span class="sxs-lookup"><span data-stu-id="fd09b-109">If the **EnableQuarantineChecks** element is TRUE, then PEAP will perform NAP checks; if FALSE, PEAP will not perform NAP checks.</span></span> <span data-ttu-id="fd09b-110">O elemento **EnableQuarantineChecks** é opcional.</span><span class="sxs-lookup"><span data-stu-id="fd09b-110">The **EnableQuarantineChecks** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd09b-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd09b-111">Requirements</span></span>



| <span data-ttu-id="fd09b-112">Função</span><span class="sxs-lookup"><span data-stu-id="fd09b-112">Role</span></span> | <span data-ttu-id="fd09b-113">Versão mínima do sistema operacional com suporte</span><span class="sxs-lookup"><span data-stu-id="fd09b-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="fd09b-114">Cliente</span><span class="sxs-lookup"><span data-stu-id="fd09b-114">Client</span></span><br/> | <span data-ttu-id="fd09b-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fd09b-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fd09b-116">Servidor</span><span class="sxs-lookup"><span data-stu-id="fd09b-116">Server</span></span><br/> | <span data-ttu-id="fd09b-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fd09b-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fd09b-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd09b-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="fd09b-119">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="fd09b-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="fd09b-120">**EapType**</span><span class="sxs-lookup"><span data-stu-id="fd09b-120">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="fd09b-121">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="fd09b-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="fd09b-122">**EapType**</span><span class="sxs-lookup"><span data-stu-id="fd09b-122">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="fd09b-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="fd09b-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="fd09b-124">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="fd09b-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="fd09b-125">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="fd09b-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="fd09b-126">Elementos do esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="fd09b-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





