---
description: Especifica a prioridade de thread relativa para uma ramificação da topologia.
ms.assetid: 7BCD2EE0-94FB-4438-9B6A-7B26DBFB5978
title: Atributo MF_TOPONODE_WORKQUEUE_MMCSS_PRIORITY (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0667c91054f8711b8825cf421a2ee565b9161f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090864"
---
# <a name="mf_toponode_workqueue_mmcss_priority-attribute"></a><span data-ttu-id="87f48-103">\_Atributo de \_ prioridade MF TOPONODE fila do \_ MMCSS \_</span><span class="sxs-lookup"><span data-stu-id="87f48-103">MF\_TOPONODE\_WORKQUEUE\_MMCSS\_PRIORITY attribute</span></span>

<span data-ttu-id="87f48-104">Especifica a prioridade de thread relativa para uma ramificação da topologia.</span><span class="sxs-lookup"><span data-stu-id="87f48-104">Specifies the relative thread priority for a branch of the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="87f48-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="87f48-105">Data type</span></span>

<span data-ttu-id="87f48-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="87f48-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="87f48-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="87f48-107">Remarks</span></span>

<span data-ttu-id="87f48-108">Esse atributo se aplica a nós de origem (**\_ nó de \_ SOURCESTREAM \_ de topologia MF**).</span><span class="sxs-lookup"><span data-stu-id="87f48-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="87f48-109">O atributo é opcional.</span><span class="sxs-lookup"><span data-stu-id="87f48-109">The attribute is optional.</span></span>

<span data-ttu-id="87f48-110">Esse atributo requer os atributos de classe [MF \_ TOPONODE \_ fila \_ ](mf-toponode-workqueue-id-attribute.md) e [MF \_ TOPONODE \_ fila do \_ MMCSS \_ ](mf-toponode-workqueue-mmcss-class-attribute.md) no mesmo nó.</span><span class="sxs-lookup"><span data-stu-id="87f48-110">This attribute requires the [MF\_TOPONODE\_WORKQUEUE\_ID](mf-toponode-workqueue-id-attribute.md) and [MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS](mf-toponode-workqueue-mmcss-class-attribute.md) attributes on the same node.</span></span>

<span data-ttu-id="87f48-111">O valor do atributo é a prioridade de thread relativa da fila de trabalho para essa ramificação da topologia.</span><span class="sxs-lookup"><span data-stu-id="87f48-111">The value of the attribute is the relative thread priority of the work queue for this branch of the topology.</span></span> <span data-ttu-id="87f48-112">O [serviço do Agendador de classes de multimídia](../procthread/multimedia-class-scheduler-service.md) (MMCSS) usa a prioridade relativa quando define a prioridade do thread.</span><span class="sxs-lookup"><span data-stu-id="87f48-112">The [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) uses the relative priority when it sets the thread priority.</span></span> <span data-ttu-id="87f48-113">Para obter mais informações, consulte [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).</span><span class="sxs-lookup"><span data-stu-id="87f48-113">For more information, see [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).</span></span>

<span data-ttu-id="87f48-114">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="87f48-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="87f48-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87f48-115">Requirements</span></span>



| <span data-ttu-id="87f48-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="87f48-116">Requirement</span></span> | <span data-ttu-id="87f48-117">Valor</span><span class="sxs-lookup"><span data-stu-id="87f48-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="87f48-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87f48-118">Minimum supported client</span></span><br/> | <span data-ttu-id="87f48-119">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="87f48-119">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="87f48-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87f48-120">Minimum supported server</span></span><br/> | <span data-ttu-id="87f48-121">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="87f48-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="87f48-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="87f48-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="87f48-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="87f48-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87f48-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="87f48-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87f48-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="87f48-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="87f48-126">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="87f48-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="87f48-127">Aprimoramentos na fila de trabalho e threading</span><span class="sxs-lookup"><span data-stu-id="87f48-127">Work Queue and Threading Improvements</span></span>](media-foundation-work-queue-and-threading-improvements.md)
</dt> <dt>

[<span data-ttu-id="87f48-128">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="87f48-128">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="87f48-129">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span><span class="sxs-lookup"><span data-stu-id="87f48-129">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="87f48-130">**\_ID da \_ fila de TOPONODE MF \_**</span><span class="sxs-lookup"><span data-stu-id="87f48-130">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)
</dt> <dt>

[<span data-ttu-id="87f48-131">**\_TaskId TOPONODE \_ fila \_ de \_ tarefas do MMCSS**</span><span class="sxs-lookup"><span data-stu-id="87f48-131">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID**</span></span>](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> </dl>

 

 
