---
title: Objeto IdleSettings
description: Objeto de script que especifica como a Agendador de Tarefas executa tarefas quando o computador está em uma condição ociosa.
ms.assetid: d303596a-0a84-4056-9f7a-5a9512852002
keywords:
- Agendador de Tarefas de objeto IdleSettings
- Agendador de Tarefas de objeto IdleSettings, descrito
topic_type:
- apiref
api_name:
- IdleSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 819ff226386f30483de96fac6213b35d7dd51a52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369470"
---
# <a name="idlesettings-object"></a><span data-ttu-id="036fb-105">Objeto IdleSettings</span><span class="sxs-lookup"><span data-stu-id="036fb-105">IdleSettings object</span></span>

<span data-ttu-id="036fb-106">Um objeto de script que especifica como a Agendador de Tarefas executa tarefas quando o computador está em uma condição ociosa.</span><span class="sxs-lookup"><span data-stu-id="036fb-106">A scripting object that specifies how the Task Scheduler performs tasks when the computer is in an idle condition.</span></span> <span data-ttu-id="036fb-107">Para obter informações sobre condições ociosas, consulte [condições de ociosidade da tarefa](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="036fb-107">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

## <a name="members"></a><span data-ttu-id="036fb-108">Membros</span><span class="sxs-lookup"><span data-stu-id="036fb-108">Members</span></span>

<span data-ttu-id="036fb-109">O objeto **IdleSettings** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="036fb-109">The **IdleSettings** object has these types of members:</span></span>

- [<span data-ttu-id="036fb-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="036fb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="036fb-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="036fb-111">Properties</span></span>

<span data-ttu-id="036fb-112">O objeto **IdleSettings** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="036fb-112">The **IdleSettings** object has these properties.</span></span>

> [!NOTE]
> <span data-ttu-id="036fb-113">As configurações *IdleDuration* e *WaitTimeout* são preteridas.</span><span class="sxs-lookup"><span data-stu-id="036fb-113">The *IdleDuration* and *WaitTimeout* settings are deprecated.</span></span> <span data-ttu-id="036fb-114">Eles ainda estão presentes na interface do usuário Agendador de Tarefas, e seus métodos de interface ainda podem retornar valores válidos, mas não são mais usados.</span><span class="sxs-lookup"><span data-stu-id="036fb-114">They're still present in the Task Scheduler user interface, and their interface methods may still return valid values, but they're no longer used.</span></span>

| <span data-ttu-id="036fb-115">Propriedade</span><span class="sxs-lookup"><span data-stu-id="036fb-115">Property</span></span>                                                       | <span data-ttu-id="036fb-116">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="036fb-116">Access type</span></span>           | <span data-ttu-id="036fb-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="036fb-117">Description</span></span>                                                                                                                                                     |
|:---------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="036fb-118">**RestartOnIdle**</span><span class="sxs-lookup"><span data-stu-id="036fb-118">**RestartOnIdle**</span></span>](idlesettings-restartonidle.md)<br/> | <span data-ttu-id="036fb-119">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="036fb-119">Read/write</span></span><br/> | <span data-ttu-id="036fb-120">Obtém ou define um valor booliano que indica se a tarefa é reiniciada quando o computador entra em uma condição ociosa mais de uma vez.</span><span class="sxs-lookup"><span data-stu-id="036fb-120">Gets or sets a Boolean value that indicates whether the task is restarted when the computer cycles into an idle condition more than once.</span></span><br/>            |
| [<span data-ttu-id="036fb-121">**StopOnIdleEnd**</span><span class="sxs-lookup"><span data-stu-id="036fb-121">**StopOnIdleEnd**</span></span>](idlesettings-stoponidleend.md)<br/> | <span data-ttu-id="036fb-122">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="036fb-122">Read/write</span></span><br/> | <span data-ttu-id="036fb-123">Obtém ou define um valor booliano que indica que o Agendador de Tarefas encerrará a tarefa se a condição de ociosidade terminar antes de a tarefa ser concluída.</span><span class="sxs-lookup"><span data-stu-id="036fb-123">Gets or sets a Boolean value that indicates that the Task Scheduler will terminate the task if the idle condition ends before the task is completed.</span></span><br/> |
| <span data-ttu-id="036fb-124">**Preterido**: [ **IdleDuration**](idlesettings-idleduration.md)</span><span class="sxs-lookup"><span data-stu-id="036fb-124">**Deprecated**: [**IdleDuration**](idlesettings-idleduration.md)</span></span><br/>   | <span data-ttu-id="036fb-125">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="036fb-125">Read/write</span></span><br/> | <span data-ttu-id="036fb-126">Obtém ou define um valor que indica a quantidade de tempo que o computador deve estar em um estado ocioso antes que a tarefa seja executada.</span><span class="sxs-lookup"><span data-stu-id="036fb-126">Gets or sets a value that indicates the amount of time that the computer must be in an idle state before the task is run.</span></span><br/>                            |
| <span data-ttu-id="036fb-127">**Preterido**: [ **WaitTimeout**](idlesettings-waittimeout.md)</span><span class="sxs-lookup"><span data-stu-id="036fb-127">**Deprecated**: [**WaitTimeout**](idlesettings-waittimeout.md)</span></span><br/>     | <span data-ttu-id="036fb-128">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="036fb-128">Read/write</span></span><br/> | <span data-ttu-id="036fb-129">Obtém ou define um valor que indica a quantidade de tempo que o Agendador de Tarefas aguardará a ocorrência de uma condição ociosa.</span><span class="sxs-lookup"><span data-stu-id="036fb-129">Gets or sets a value that indicates the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span><br/>                             |

## <a name="remarks"></a><span data-ttu-id="036fb-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="036fb-130">Remarks</span></span>

<span data-ttu-id="036fb-131">Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="036fb-131">When reading or writing XML for a task, this setting is specified in the [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="036fb-132">Se uma tarefa for disparada por um gatilho ocioso, a propriedade [**IdleSettings. WaitTimeout**](idlesettings-waittimeout.md) será ignorada.</span><span class="sxs-lookup"><span data-stu-id="036fb-132">If a task is triggered by an idle trigger, then the [**IdleSettings.WaitTimeout**](idlesettings-waittimeout.md) property is ignored.</span></span>

> [!NOTE]
> <span data-ttu-id="036fb-133">*IdleSettings. IdleDuration* e *IdleSettings. WaitTimeout* são preteridos.</span><span class="sxs-lookup"><span data-stu-id="036fb-133">*IdleSettings.IdleDuration* and *IdleSettings.WaitTimeout* are deprecated.</span></span>

## <a name="requirements"></a><span data-ttu-id="036fb-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="036fb-134">Requirements</span></span>

| <span data-ttu-id="036fb-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="036fb-135">Requirement</span></span> | <span data-ttu-id="036fb-136">Valor</span><span class="sxs-lookup"><span data-stu-id="036fb-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="036fb-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="036fb-137">Minimum supported client</span></span><br/> | <span data-ttu-id="036fb-138">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="036fb-138">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="036fb-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="036fb-139">Minimum supported server</span></span><br/> | <span data-ttu-id="036fb-140">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="036fb-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="036fb-141">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="036fb-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="036fb-142"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="036fb-142"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="036fb-143">DLL</span><span class="sxs-lookup"><span data-stu-id="036fb-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="036fb-144"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="036fb-144"><dt>Taskschd.dll</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="036fb-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="036fb-145">See also</span></span>

[<span data-ttu-id="036fb-146">Objetos Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="036fb-146">Task Scheduler Objects</span></span>](task-scheduler-objects.md)

[<span data-ttu-id="036fb-147">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="036fb-147">Task Scheduler</span></span>](task-scheduler-start-page.md)
