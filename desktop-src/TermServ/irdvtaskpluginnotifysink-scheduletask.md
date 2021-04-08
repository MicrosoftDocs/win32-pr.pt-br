---
title: Método IRDVTaskPluginNotifySink ScheduleTask
description: Chamado pelo agente de tarefa para agendar uma tarefa.
ms.assetid: 06793439-cf16-40ca-8a91-08acc22c73ed
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ScheduleTask
- Método ScheduleTask Serviços de Área de Trabalho Remota, interface IRDVTaskPluginNotifySink
- Serviços de Área de Trabalho Remota de interface IRDVTaskPluginNotifySink, método ScheduleTask
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.ScheduleTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9bde92992eec9c4ab3d4151c59e6d687ec2f3fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824761"
---
# <a name="irdvtaskpluginnotifysinkscheduletask-method"></a><span data-ttu-id="86ed8-106">Método IRDVTaskPluginNotifySink:: ScheduleTask</span><span class="sxs-lookup"><span data-stu-id="86ed8-106">IRDVTaskPluginNotifySink::ScheduleTask method</span></span>

<span data-ttu-id="86ed8-107">Chamado pelo agente de tarefa para agendar uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="86ed8-107">Called by the task agent to schedule a task.</span></span>

## <a name="syntax"></a><span data-ttu-id="86ed8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="86ed8-108">Syntax</span></span>


```C++
HRESULT ScheduleTask(
  [in] FILETIME        ftStartTime,
  [in] FILETIME        ftEndTime,
  [in] FILETIME        ftDeadline,
  [in] BSTR            bstrLabel,
  [in] BSTR            bstrIdentifier,
  [in] SAFEARRAY(BYTE) saContext
);
```



## <a name="parameters"></a><span data-ttu-id="86ed8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="86ed8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86ed8-110">*ftStartTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="86ed8-110">*ftStartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86ed8-111">Tipo: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span><span class="sxs-lookup"><span data-stu-id="86ed8-111">Type: **[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span></span>

<span data-ttu-id="86ed8-112">A hora de início da tarefa mais antiga, em UTC.</span><span class="sxs-lookup"><span data-stu-id="86ed8-112">The earliest task start time, in UTC.</span></span>

</dd> <dt>

<span data-ttu-id="86ed8-113">*ftEndTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="86ed8-113">*ftEndTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86ed8-114">Tipo: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span><span class="sxs-lookup"><span data-stu-id="86ed8-114">Type: **[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span></span>

<span data-ttu-id="86ed8-115">A hora de término da tarefa, em UTC.</span><span class="sxs-lookup"><span data-stu-id="86ed8-115">The task end time, in UTC.</span></span> <span data-ttu-id="86ed8-116">Passe um [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) definido para todos os zeros se nenhuma hora de término for especificada.</span><span class="sxs-lookup"><span data-stu-id="86ed8-116">Pass a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) set to all zeros if no end time is specified.</span></span>

</dd> <dt>

<span data-ttu-id="86ed8-117">*ftDeadline* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="86ed8-117">*ftDeadline* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86ed8-118">Tipo: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span><span class="sxs-lookup"><span data-stu-id="86ed8-118">Type: **[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**</span></span>

<span data-ttu-id="86ed8-119">A data limite da tarefa, em UTC.</span><span class="sxs-lookup"><span data-stu-id="86ed8-119">The task deadline, in UTC.</span></span> <span data-ttu-id="86ed8-120">Isso é usado para definir a prioridade para várias tarefas que estão dentro de sua janela inicial.</span><span class="sxs-lookup"><span data-stu-id="86ed8-120">This is used to set priority for multiple tasks that are within their start window.</span></span> <span data-ttu-id="86ed8-121">Se mais de uma tarefa deve ser iniciada, aquela com o prazo mais antigo será iniciada primeiro.</span><span class="sxs-lookup"><span data-stu-id="86ed8-121">If more than one task should be started, the one with the earliest deadline will be started first.</span></span>

</dd> <dt>

<span data-ttu-id="86ed8-122">*bstrLabel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="86ed8-122">*bstrLabel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86ed8-123">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="86ed8-123">Type: **BSTR**</span></span>

<span data-ttu-id="86ed8-124">O rótulo da tarefa.</span><span class="sxs-lookup"><span data-stu-id="86ed8-124">The label for the task.</span></span> <span data-ttu-id="86ed8-125">Isso é passado para o método [**StartTask**](irdvtaskplugin-starttask.md) .</span><span class="sxs-lookup"><span data-stu-id="86ed8-125">This is passed to the [**StartTask**](irdvtaskplugin-starttask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="86ed8-126">*bstrIdentifier* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="86ed8-126">*bstrIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86ed8-127">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="86ed8-127">Type: **BSTR**</span></span>

<span data-ttu-id="86ed8-128">O identificador da tarefa.</span><span class="sxs-lookup"><span data-stu-id="86ed8-128">The identifier of the task.</span></span> <span data-ttu-id="86ed8-129">Isso é passado para o método [**StartTask**](irdvtaskplugin-starttask.md) .</span><span class="sxs-lookup"><span data-stu-id="86ed8-129">This is passed to the [**StartTask**](irdvtaskplugin-starttask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="86ed8-130">*saContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="86ed8-130">*saContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86ed8-131">Tipo: **SafeArray (Byte)**</span><span class="sxs-lookup"><span data-stu-id="86ed8-131">Type: **SAFEARRAY(BYTE)**</span></span>

<span data-ttu-id="86ed8-132">Dados opcionais para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="86ed8-132">Optional data for the task.</span></span> <span data-ttu-id="86ed8-133">Isso é passado para o método [**StartTask**](irdvtaskplugin-starttask.md) .</span><span class="sxs-lookup"><span data-stu-id="86ed8-133">This is passed to the [**StartTask**](irdvtaskplugin-starttask.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86ed8-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="86ed8-134">Return value</span></span>

<span data-ttu-id="86ed8-135">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="86ed8-135">Type: **HRESULT**</span></span>

<span data-ttu-id="86ed8-136">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="86ed8-136">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="86ed8-137">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="86ed8-137">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="86ed8-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86ed8-138">Requirements</span></span>



| <span data-ttu-id="86ed8-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="86ed8-139">Requirement</span></span> | <span data-ttu-id="86ed8-140">Valor</span><span class="sxs-lookup"><span data-stu-id="86ed8-140">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="86ed8-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86ed8-141">Minimum supported client</span></span><br/> | <span data-ttu-id="86ed8-142">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="86ed8-142">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="86ed8-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86ed8-143">Minimum supported server</span></span><br/> | <span data-ttu-id="86ed8-144">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="86ed8-144">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="86ed8-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="86ed8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86ed8-146">**IRDVTaskPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="86ed8-146">**IRDVTaskPluginNotifySink**</span></span>](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

