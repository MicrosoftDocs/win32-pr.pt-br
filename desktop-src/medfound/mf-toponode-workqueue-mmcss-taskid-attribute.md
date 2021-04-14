---
description: Especifica um identificador de tarefa do serviço de Agendador de classes de multimídia (MMCSS) para uma ramificação de topologia.
ms.assetid: ccecc1e6-2d30-4e89-849f-c3acad97f312
title: Atributo MF_TOPONODE_WORKQUEUE_MMCSS_TASKID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53af119c58d725d42ec5737ffd9bf96286a65ac1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502108"
---
# <a name="mf_toponode_workqueue_mmcss_taskid-attribute"></a><span data-ttu-id="68f45-103">\_Atributo TOPONODE da \_ fila de \_ \_ tarefas do MF MMCSS</span><span class="sxs-lookup"><span data-stu-id="68f45-103">MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID attribute</span></span>

<span data-ttu-id="68f45-104">Especifica um identificador de tarefa do serviço de Agendador de classes de multimídia (MMCSS) para uma ramificação de topologia.</span><span class="sxs-lookup"><span data-stu-id="68f45-104">Specifies a Multimedia Class Scheduler Service (MMCSS) task identifier for a topology branch.</span></span>

## <a name="data-type"></a><span data-ttu-id="68f45-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="68f45-105">Data type</span></span>

<span data-ttu-id="68f45-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="68f45-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="68f45-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="68f45-107">Remarks</span></span>

<span data-ttu-id="68f45-108">Esse atributo se aplica a nós de origem (**\_ nó de \_ SOURCESTREAM \_ de topologia MF**).</span><span class="sxs-lookup"><span data-stu-id="68f45-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="68f45-109">Esse atributo é opcional.</span><span class="sxs-lookup"><span data-stu-id="68f45-109">This attribute is optional.</span></span>

<span data-ttu-id="68f45-110">Esse atributo é ignorado, a menos que os seguintes atributos também sejam definidos:</span><span class="sxs-lookup"><span data-stu-id="68f45-110">This attribute is ignored unless the following attributes are also set:</span></span>

-   [<span data-ttu-id="68f45-111">**\_ID da \_ fila de TOPONODE MF \_**</span><span class="sxs-lookup"><span data-stu-id="68f45-111">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)
-   [<span data-ttu-id="68f45-112">**\_classe TOPONODE do MF \_ fila do \_ MMCSS \_**</span><span class="sxs-lookup"><span data-stu-id="68f45-112">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**</span></span>](mf-toponode-workqueue-mmcss-class-attribute.md)

<span data-ttu-id="68f45-113">Se o aplicativo registrar um de seus próprios threads com o MMCSS, você poderá usar esse atributo para associar a fila de trabalho de topologia ao grupo do MMCSS do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="68f45-113">If the application registers one of its own threads with MMCSS, you can use this attribute to associate the topology work queue with the application's MMCSS group.</span></span> <span data-ttu-id="68f45-114">Defina o valor do atributo igual ao identificador da tarefa que o aplicativo recebeu quando registrado com o MMCSS.</span><span class="sxs-lookup"><span data-stu-id="68f45-114">Set the attribute value equal to the task identifier that the application received when it registered with MMCSS.</span></span> <span data-ttu-id="68f45-115">(O identificador de tarefa é retornado no parâmetro *TaskIndex* da função [**AvSetMmThreadCharacteristics**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) .</span><span class="sxs-lookup"><span data-stu-id="68f45-115">(The task identifier is returned in the *TaskIndex* parameter of the [**AvSetMmThreadCharacteristics**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) function.</span></span> <span data-ttu-id="68f45-116">Para obter mais informações, consulte o tópico [processo e funções de thread](../procthread/process-and-thread-functions.md).)</span><span class="sxs-lookup"><span data-stu-id="68f45-116">For more information, see the topic [Process and Thread Functions](../procthread/process-and-thread-functions.md).)</span></span>

<span data-ttu-id="68f45-117">Se você quiser que o MMCSS atribua um novo identificador de tarefa para a topologia, defina o atributo de [**\_ classe MF TOPONODE \_ fila do \_ MMCSS \_**](mf-toponode-workqueue-mmcss-class-attribute.md) , mas não defina o atributo **MF TOPONODE da fila de \_ \_ \_ \_ tarefas do MMCSS** .</span><span class="sxs-lookup"><span data-stu-id="68f45-117">If you want MMCSS to assign a new task identifier for the topology, set the [**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**](mf-toponode-workqueue-mmcss-class-attribute.md) attribute, but do not set the **MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID** attribute.</span></span>

<span data-ttu-id="68f45-118">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="68f45-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="68f45-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68f45-119">Requirements</span></span>



| <span data-ttu-id="68f45-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="68f45-120">Requirement</span></span> | <span data-ttu-id="68f45-121">Valor</span><span class="sxs-lookup"><span data-stu-id="68f45-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68f45-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68f45-122">Minimum supported client</span></span><br/> | <span data-ttu-id="68f45-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="68f45-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="68f45-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68f45-124">Minimum supported server</span></span><br/> | <span data-ttu-id="68f45-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="68f45-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="68f45-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="68f45-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="68f45-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="68f45-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68f45-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="68f45-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68f45-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="68f45-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="68f45-130">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="68f45-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="68f45-131">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="68f45-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="68f45-132">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="68f45-132">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="68f45-133">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span><span class="sxs-lookup"><span data-stu-id="68f45-133">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="68f45-134">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="68f45-134">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="68f45-135">Filas de trabalho</span><span class="sxs-lookup"><span data-stu-id="68f45-135">Work Queues</span></span>](work-queues.md)
</dt> </dl>

 

 
