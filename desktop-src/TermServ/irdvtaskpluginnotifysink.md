---
title: Interface IRDVTaskPluginNotifySink
description: A interface IRDVTaskPluginNotifySink é usada pelo agente de tarefa para se comunicar com o agente de gatilho.
ms.assetid: ccf19693-d3cc-4cf7-af35-947be047beeb
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IRDVTaskPluginNotifySink
- Serviços de Área de Trabalho Remota da interface IRDVTaskPluginNotifySink, descrita
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0dadaf387fcf6e8381404440e0d31dd210b9f8a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644792"
---
# <a name="irdvtaskpluginnotifysink-interface"></a><span data-ttu-id="28e0e-105">Interface IRDVTaskPluginNotifySink</span><span class="sxs-lookup"><span data-stu-id="28e0e-105">IRDVTaskPluginNotifySink interface</span></span>

<span data-ttu-id="28e0e-106">A interface **IRDVTaskPluginNotifySink** é usada pelo agente de tarefa para se comunicar com o agente de gatilho.</span><span class="sxs-lookup"><span data-stu-id="28e0e-106">The **IRDVTaskPluginNotifySink** interface is used by the task agent to communicate with the trigger agent.</span></span> <span data-ttu-id="28e0e-107">Um ponteiro para essa interface é passado para o agente de tarefa no método [**IRDVTaskPlugin:: Initialize**](irdvtaskplugin-initialize.md) .</span><span class="sxs-lookup"><span data-stu-id="28e0e-107">A pointer to this interface is passed to the task agent in the [**IRDVTaskPlugin::Initialize**](irdvtaskplugin-initialize.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="28e0e-108">Membros</span><span class="sxs-lookup"><span data-stu-id="28e0e-108">Members</span></span>

<span data-ttu-id="28e0e-109">A interface **IRDVTaskPluginNotifySink** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="28e0e-109">The **IRDVTaskPluginNotifySink** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="28e0e-110">**IRDVTaskPluginNotifySink** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="28e0e-110">**IRDVTaskPluginNotifySink** also has these types of members:</span></span>

-   [<span data-ttu-id="28e0e-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="28e0e-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="28e0e-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="28e0e-112">Methods</span></span>

<span data-ttu-id="28e0e-113">A interface **IRDVTaskPluginNotifySink** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="28e0e-113">The **IRDVTaskPluginNotifySink** interface has these methods.</span></span>



| <span data-ttu-id="28e0e-114">Método</span><span class="sxs-lookup"><span data-stu-id="28e0e-114">Method</span></span>                                                                  | <span data-ttu-id="28e0e-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="28e0e-115">Description</span></span>                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="28e0e-116">**DeleteSchedule**</span><span class="sxs-lookup"><span data-stu-id="28e0e-116">**DeleteSchedule**</span></span>](irdvtaskpluginnotifysink-deleteschedule.md)       | <span data-ttu-id="28e0e-117">Chamado pelo agente de tarefa para excluir uma tarefa agendada.</span><span class="sxs-lookup"><span data-stu-id="28e0e-117">Called by the task agent to delete a scheduled task.</span></span><br/>                   |
| [<span data-ttu-id="28e0e-118">**OnTaskStateChange**</span><span class="sxs-lookup"><span data-stu-id="28e0e-118">**OnTaskStateChange**</span></span>](irdvtaskpluginnotifysink-ontaskstatechange.md) | <span data-ttu-id="28e0e-119">Usado para notificar o agente de disparo de que o estado de uma tarefa foi alterado.</span><span class="sxs-lookup"><span data-stu-id="28e0e-119">Used to notify the trigger agent that the state of a task has changed.</span></span><br/> |
| [<span data-ttu-id="28e0e-120">**Onterminado**</span><span class="sxs-lookup"><span data-stu-id="28e0e-120">**OnTerminated**</span></span>](irdvtaskpluginnotifysink-onterminated.md)           | <span data-ttu-id="28e0e-121">Chamado pelo agente de tarefa para solicitar que o agente de tarefa seja desligado.</span><span class="sxs-lookup"><span data-stu-id="28e0e-121">Called by the task agent to request that the task agent be shut down.</span></span><br/>  |
| [<span data-ttu-id="28e0e-122">**ScheduleTask**</span><span class="sxs-lookup"><span data-stu-id="28e0e-122">**ScheduleTask**</span></span>](irdvtaskpluginnotifysink-scheduletask.md)           | <span data-ttu-id="28e0e-123">Chamado pelo agente de tarefa para agendar uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="28e0e-123">Called by the task agent to schedule a task.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="28e0e-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="28e0e-124">Remarks</span></span>

<span data-ttu-id="28e0e-125">Embora essa interface tenha suporte nos sistemas operacionais identificados nos requisitos abaixo, ela só será usada se a máquina virtual estiver hospedada no Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="28e0e-125">Although this interface is supported on the operating systems identified in the Requirements below, it will only be used if the virtual machine is hosted on Windows Server 2012.</span></span>

## <a name="requirements"></a><span data-ttu-id="28e0e-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28e0e-126">Requirements</span></span>



| <span data-ttu-id="28e0e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="28e0e-127">Requirement</span></span> | <span data-ttu-id="28e0e-128">Valor</span><span class="sxs-lookup"><span data-stu-id="28e0e-128">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="28e0e-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28e0e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="28e0e-130">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="28e0e-130">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="28e0e-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28e0e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="28e0e-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="28e0e-132">Windows Server 2008 R2</span></span><br/> |



 

