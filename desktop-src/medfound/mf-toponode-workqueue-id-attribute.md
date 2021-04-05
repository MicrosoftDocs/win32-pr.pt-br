---
description: Especifica uma fila de trabalho para uma ramificação de topologia.
ms.assetid: 5bc7e2db-cfd2-4b94-b4d6-fe2b9ea9daf8
title: Atributo MF_TOPONODE_WORKQUEUE_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9acda95895a1812f6cebbe64cbf3cd3bcdea4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090865"
---
# <a name="mf_toponode_workqueue_id-attribute"></a><span data-ttu-id="980bc-103">\_Atributo de \_ ID de fila de TOPONODE MF \_</span><span class="sxs-lookup"><span data-stu-id="980bc-103">MF\_TOPONODE\_WORKQUEUE\_ID attribute</span></span>

<span data-ttu-id="980bc-104">Especifica uma fila de trabalho para uma ramificação de topologia.</span><span class="sxs-lookup"><span data-stu-id="980bc-104">Specifies a work queue for a topology branch.</span></span>

## <a name="data-type"></a><span data-ttu-id="980bc-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="980bc-105">Data type</span></span>

<span data-ttu-id="980bc-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="980bc-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="980bc-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="980bc-107">Remarks</span></span>

<span data-ttu-id="980bc-108">Esse atributo se aplica a nós de origem (**\_ nó de \_ SOURCESTREAM \_ de topologia MF**).</span><span class="sxs-lookup"><span data-stu-id="980bc-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="980bc-109">O atributo é opcional.</span><span class="sxs-lookup"><span data-stu-id="980bc-109">The attribute is optional.</span></span>

<span data-ttu-id="980bc-110">O valor do atributo é um identificador definido pelo aplicativo para a fila de trabalho.</span><span class="sxs-lookup"><span data-stu-id="980bc-110">The value of the attribute is an application-defined identifier for the work queue.</span></span>

<span data-ttu-id="980bc-111">Os aplicativos podem usar esse atributo para atribuir filas de trabalho a ramificações da topologia.</span><span class="sxs-lookup"><span data-stu-id="980bc-111">Applications can use this attribute to assign work queues to branches of the topology.</span></span> <span data-ttu-id="980bc-112">Cada nó de origem na topologia define uma ramificação.</span><span class="sxs-lookup"><span data-stu-id="980bc-112">Each source node in the topology defines one branch.</span></span> <span data-ttu-id="980bc-113">A ramificação inclui todos os nós de topologia que recebem dados desse nó.</span><span class="sxs-lookup"><span data-stu-id="980bc-113">The branch includes every topology node that receives data from that node.</span></span>

<span data-ttu-id="980bc-114">Se você definir esse atributo, chame o método [**IMFWorkQueueServices:: BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) na topologia resolvida.</span><span class="sxs-lookup"><span data-stu-id="980bc-114">If you set this attribute, call the [**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) method on the resolved topology.</span></span> <span data-ttu-id="980bc-115">Várias ramificações na topologia podem compartilhar a mesma fila de trabalho e as filas de trabalho podem ser reutilizadas entre as topologias.</span><span class="sxs-lookup"><span data-stu-id="980bc-115">Multiple branches in the topology can share the same work queue, and work queues can be re-used across topologies.</span></span>

> [!Note]  
> <span data-ttu-id="980bc-116">O valor desse atributo não é o mesmo que o identificador retornado pela função [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) .</span><span class="sxs-lookup"><span data-stu-id="980bc-116">The value of this attribute is not the same as the identifier that is returned by the [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) function.</span></span> <span data-ttu-id="980bc-117">O valor do atributo é um identificador definido pelo aplicativo e é usado para associar branches de topologia com filas de trabalho.</span><span class="sxs-lookup"><span data-stu-id="980bc-117">The value of the attribute is an application-defined identifier, and is used to associate topology branches with work queues.</span></span> <span data-ttu-id="980bc-118">Quando a sessão de mídia aloca uma nova fila de trabalho, ela armazena o identificador de fila de trabalho real internamente.</span><span class="sxs-lookup"><span data-stu-id="980bc-118">When the Media Session allocates a new work queue, it stores the actual work-queue identifier internally.</span></span>

 

<span data-ttu-id="980bc-119">Se esse atributo for definido, o aplicativo também poderá atribuir a ramificação a uma tarefa do serviço de Agendador de classes de multimídia (MMCSS), definindo o atributo de [**\_ classe MF TOPONODE \_ fila do \_ MMCSS \_**](mf-toponode-workqueue-mmcss-class-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="980bc-119">If this attribute it set, the application can also assign the branch to a Multimedia Class Scheduler Service (MMCSS) task, by setting the [**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**](mf-toponode-workqueue-mmcss-class-attribute.md) attribute.</span></span>

<span data-ttu-id="980bc-120">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="980bc-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="980bc-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="980bc-121">Requirements</span></span>



| <span data-ttu-id="980bc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="980bc-122">Requirement</span></span> | <span data-ttu-id="980bc-123">Valor</span><span class="sxs-lookup"><span data-stu-id="980bc-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="980bc-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="980bc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="980bc-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="980bc-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="980bc-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="980bc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="980bc-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="980bc-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="980bc-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="980bc-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="980bc-129"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="980bc-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="980bc-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="980bc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="980bc-131">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="980bc-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="980bc-132">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="980bc-132">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="980bc-133">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="980bc-133">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="980bc-134">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="980bc-134">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="980bc-135">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span><span class="sxs-lookup"><span data-stu-id="980bc-135">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="980bc-136">**\_classe TOPONODE do MF \_ fila do \_ MMCSS \_**</span><span class="sxs-lookup"><span data-stu-id="980bc-136">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**</span></span>](mf-toponode-workqueue-mmcss-class-attribute.md)
</dt> <dt>

[<span data-ttu-id="980bc-137">**\_TaskId TOPONODE \_ fila \_ de \_ tarefas do MMCSS**</span><span class="sxs-lookup"><span data-stu-id="980bc-137">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID**</span></span>](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[<span data-ttu-id="980bc-138">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="980bc-138">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="980bc-139">Filas de trabalho</span><span class="sxs-lookup"><span data-stu-id="980bc-139">Work Queues</span></span>](work-queues.md)
</dt> </dl>

 

 




