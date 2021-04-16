---
title: Método RegisteredTask. getruntimes
description: Para scripts, obtém as horas em que a tarefa registrada está agendada para ser executada durante um período especificado.
ms.assetid: fc3d93eb-3186-419f-9f6f-7d54f8ade1ad
keywords:
- Método getruntimes Agendador de Tarefas
- Método getruntimes Agendador de Tarefas, objeto RegisteredTask
- Objeto RegisteredTask Agendador de Tarefas, método getruntimes
topic_type:
- apiref
api_name:
- RegisteredTask.GetRunTimes
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c15aba82c5515578a3c58a485e47718d09176483
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499616"
---
# <a name="registeredtaskgetruntimes-method"></a><span data-ttu-id="6b45f-106">Método RegisteredTask. getruntimes</span><span class="sxs-lookup"><span data-stu-id="6b45f-106">RegisteredTask.GetRunTimes method</span></span>

<span data-ttu-id="6b45f-107">Para scripts, obtém as horas em que a tarefa registrada está agendada para ser executada durante um período especificado.</span><span class="sxs-lookup"><span data-stu-id="6b45f-107">For scripting, gets the times that the registered task is scheduled to run during a specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b45f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6b45f-108">Syntax</span></span>


```VB
RegisteredTask.GetRunTimes( _
  ByVal begin, _
  ByVal end, _
  ByRef count, _
  ByRef rgstTaskTimes _
)
```



## <a name="parameters"></a><span data-ttu-id="6b45f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b45f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b45f-110">*Iniciar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6b45f-110">*begin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b45f-111">A hora de início da consulta.</span><span class="sxs-lookup"><span data-stu-id="6b45f-111">The starting time for the query.</span></span>

</dd> <dt>

<span data-ttu-id="6b45f-112">*fim* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6b45f-112">*end* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b45f-113">A hora de término da consulta.</span><span class="sxs-lookup"><span data-stu-id="6b45f-113">The ending time for the query.</span></span>

</dd> <dt>

<span data-ttu-id="6b45f-114">*contagem* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="6b45f-114">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b45f-115">O número de horas agendadas em que a tarefa será executada.</span><span class="sxs-lookup"><span data-stu-id="6b45f-115">The number of scheduled times the task will run.</span></span>

</dd> <dt>

<span data-ttu-id="6b45f-116">*rgstTaskTimes* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6b45f-116">*rgstTaskTimes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b45f-117">Os horários agendados em que a tarefa será executada.</span><span class="sxs-lookup"><span data-stu-id="6b45f-117">The scheduled times that the task will run.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b45f-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6b45f-118">Return value</span></span>

<span data-ttu-id="6b45f-119">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6b45f-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b45f-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b45f-120">Remarks</span></span>

<span data-ttu-id="6b45f-121">Se a tarefa registrada contiver gatilhos que são desabilitados individualmente, esses gatilhos ainda afetarão o próximo tempo de execução agendado que é retornado, embora estejam desabilitados.</span><span class="sxs-lookup"><span data-stu-id="6b45f-121">If the registered task contains triggers that are individually disabled, these triggers will still affect the next scheduled run time that is returned even though they are disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b45f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b45f-122">Requirements</span></span>



| <span data-ttu-id="6b45f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b45f-123">Requirement</span></span> | <span data-ttu-id="6b45f-124">Valor</span><span class="sxs-lookup"><span data-stu-id="6b45f-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b45f-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b45f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6b45f-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6b45f-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6b45f-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b45f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6b45f-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6b45f-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6b45f-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6b45f-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="6b45f-130"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6b45f-130"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6b45f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="6b45f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b45f-132"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b45f-132"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b45f-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b45f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b45f-134">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="6b45f-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="6b45f-135">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="6b45f-135">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





