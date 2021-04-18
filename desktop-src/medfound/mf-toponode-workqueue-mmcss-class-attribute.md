---
description: Especifica uma tarefa do serviço de Agendador de classes de multimídia (MMCSS) para uma ramificação de topologia.
ms.assetid: 8668d0f1-9d54-4c56-bb19-09498252bec4
title: Atributo MF_TOPONODE_WORKQUEUE_MMCSS_CLASS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 824c9dbdc9b12bbc8fead9ab6ae722fca1e6643a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766559"
---
# <a name="mf_toponode_workqueue_mmcss_class-attribute"></a><span data-ttu-id="be364-103">\_Atributo de classe MF TOPONODE \_ fila \_ MMCSS \_</span><span class="sxs-lookup"><span data-stu-id="be364-103">MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS attribute</span></span>

<span data-ttu-id="be364-104">Especifica uma tarefa do [serviço de Agendador de classes de multimídia](../procthread/multimedia-class-scheduler-service.md) (MMCSS) para uma ramificação de topologia.</span><span class="sxs-lookup"><span data-stu-id="be364-104">Specifies a [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) task for a topology branch.</span></span>

## <a name="data-type"></a><span data-ttu-id="be364-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="be364-105">Data type</span></span>

<span data-ttu-id="be364-106">Cadeia de caracteres largos</span><span class="sxs-lookup"><span data-stu-id="be364-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="be364-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="be364-107">Remarks</span></span>

<span data-ttu-id="be364-108">Esse atributo se aplica a nós de origem (**\_ nó de \_ SOURCESTREAM \_ de topologia MF**).</span><span class="sxs-lookup"><span data-stu-id="be364-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="be364-109">Esse atributo é opcional.</span><span class="sxs-lookup"><span data-stu-id="be364-109">This attribute is optional.</span></span>

<span data-ttu-id="be364-110">Esse atributo requer o atributo de [ID de fila de TOPONODE do MF \_ \_ \_ ](mf-toponode-workqueue-id-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="be364-110">This attribute requires the [MF\_TOPONODE\_WORKQUEUE\_ID](mf-toponode-workqueue-id-attribute.md) attribute.</span></span> <span data-ttu-id="be364-111">Se você definir esse atributo, defina também o atributo de **\_ ID de \_ fila \_ de teleTOPONODE MF** definido no mesmo nó.</span><span class="sxs-lookup"><span data-stu-id="be364-111">If you set this attribute, also set the **MF\_TOPONODE\_WORKQUEUE\_ID** attribute is set on the same node.</span></span>

<span data-ttu-id="be364-112">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="be364-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="be364-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be364-113">Requirements</span></span>



| <span data-ttu-id="be364-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="be364-114">Requirement</span></span> | <span data-ttu-id="be364-115">Valor</span><span class="sxs-lookup"><span data-stu-id="be364-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="be364-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be364-116">Minimum supported client</span></span><br/> | <span data-ttu-id="be364-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="be364-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="be364-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be364-118">Minimum supported server</span></span><br/> | <span data-ttu-id="be364-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="be364-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="be364-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="be364-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="be364-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="be364-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be364-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="be364-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be364-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="be364-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="be364-124">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="be364-124">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="be364-125">**IMFAttributes:: SetString**</span><span class="sxs-lookup"><span data-stu-id="be364-125">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="be364-126">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="be364-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="be364-127">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span><span class="sxs-lookup"><span data-stu-id="be364-127">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="be364-128">**\_ID da \_ fila de TOPONODE MF \_**</span><span class="sxs-lookup"><span data-stu-id="be364-128">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)
</dt> <dt>

[<span data-ttu-id="be364-129">**\_TaskId TOPONODE \_ fila \_ de \_ tarefas do MMCSS**</span><span class="sxs-lookup"><span data-stu-id="be364-129">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID**</span></span>](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[<span data-ttu-id="be364-130">Atributos de nó de topologia</span><span class="sxs-lookup"><span data-stu-id="be364-130">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="be364-131">Filas de trabalho</span><span class="sxs-lookup"><span data-stu-id="be364-131">Work Queues</span></span>](work-queues.md)
</dt> </dl>

 

 
