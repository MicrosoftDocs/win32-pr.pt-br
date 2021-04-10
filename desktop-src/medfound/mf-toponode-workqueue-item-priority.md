---
description: Especifica a prioridade de item de trabalho para uma ramificação da topologia.
ms.assetid: B2FA1151-08D3-46F9-A38D-AC8908EFA6A2
title: Atributo MF_TOPONODE_WORKQUEUE_ITEM_PRIORITY (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5f7df6630e41a32eeb069c2a07b8030da79929
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164759"
---
# <a name="mf_toponode_workqueue_item_priority-attribute"></a><span data-ttu-id="b7a9d-103">\_Atributo de \_ prioridade do item da fila de TOPONODE MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="b7a9d-103">MF\_TOPONODE\_WORKQUEUE\_ITEM\_PRIORITY attribute</span></span>

<span data-ttu-id="b7a9d-104">Especifica a prioridade de item de trabalho para uma ramificação da topologia.</span><span class="sxs-lookup"><span data-stu-id="b7a9d-104">Specifies the work-item priority for a branch of the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="b7a9d-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b7a9d-105">Data type</span></span>

<span data-ttu-id="b7a9d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b7a9d-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b7a9d-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7a9d-107">Remarks</span></span>

<span data-ttu-id="b7a9d-108">Esse atributo se aplica a nós de origem (**\_ nó de \_ SOURCESTREAM \_ de topologia MF**).</span><span class="sxs-lookup"><span data-stu-id="b7a9d-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="b7a9d-109">O atributo é opcional.</span><span class="sxs-lookup"><span data-stu-id="b7a9d-109">The attribute is optional.</span></span>

<span data-ttu-id="b7a9d-110">Esse atributo requer o atributo de ID de fila de TOPONODE do MF no mesmo nó. [ \_ \_ \_ ](mf-toponode-workqueue-id-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="b7a9d-110">This attribute requires the [MF\_TOPONODE\_WORKQUEUE\_ID](mf-toponode-workqueue-id-attribute.md) attribute on the same node.</span></span>

<span data-ttu-id="b7a9d-111">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b7a9d-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7a9d-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7a9d-112">Requirements</span></span>



| <span data-ttu-id="b7a9d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7a9d-113">Requirement</span></span> | <span data-ttu-id="b7a9d-114">Valor</span><span class="sxs-lookup"><span data-stu-id="b7a9d-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b7a9d-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7a9d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b7a9d-116">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b7a9d-116">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b7a9d-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7a9d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b7a9d-118">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b7a9d-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b7a9d-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b7a9d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7a9d-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7a9d-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7a9d-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7a9d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7a9d-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b7a9d-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b7a9d-123">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="b7a9d-123">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="b7a9d-124">Aprimoramentos na fila de trabalho e threading</span><span class="sxs-lookup"><span data-stu-id="b7a9d-124">Work Queue and Threading Improvements</span></span>](media-foundation-work-queue-and-threading-improvements.md)
</dt> <dt>

[<span data-ttu-id="b7a9d-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="b7a9d-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="b7a9d-126">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span><span class="sxs-lookup"><span data-stu-id="b7a9d-126">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="b7a9d-127">**\_ID da \_ fila de TOPONODE MF \_**</span><span class="sxs-lookup"><span data-stu-id="b7a9d-127">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)
</dt> </dl>

 

 




