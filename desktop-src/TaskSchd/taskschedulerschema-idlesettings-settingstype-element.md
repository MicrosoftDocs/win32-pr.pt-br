---
title: Elemento IdleSettings (settingstype)
description: Especifica como a Agendador de Tarefas executa tarefas quando o computador está em um estado ocioso.
ms.assetid: 23d57417-95a9-42e3-904c-7f0859fcda7c
keywords:
- Agendador de Tarefas do elemento IdleSettings
topic_type:
- apiref
api_name:
- IdleSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ae8b7953f31d7e9c6f01387d3136f01d8ab697a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086069"
---
# <a name="idlesettings-settingstype-element"></a><span data-ttu-id="1d4aa-104">Elemento IdleSettings (settingstype)</span><span class="sxs-lookup"><span data-stu-id="1d4aa-104">IdleSettings (settingsType) Element</span></span>

<span data-ttu-id="1d4aa-105">Especifica como a Agendador de Tarefas executa tarefas quando o computador está em um estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="1d4aa-105">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span> <span data-ttu-id="1d4aa-106">Para obter informações sobre condições ociosas, consulte [condições de ociosidade da tarefa](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="1d4aa-106">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

``` syntax
<xs:element name="IdleSettings"
    type="idleSettingsType"
    minOccurs="0"
 />
```

<span data-ttu-id="1d4aa-107">O elemento **IdleSettings** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1d4aa-107">The **IdleSettings** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1d4aa-108">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="1d4aa-108">Parent element</span></span>

| <span data-ttu-id="1d4aa-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="1d4aa-109">Element</span></span>                                                           | <span data-ttu-id="1d4aa-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="1d4aa-110">Derived from</span></span>                                                         | <span data-ttu-id="1d4aa-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="1d4aa-111">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d4aa-112">**Configurações**</span><span class="sxs-lookup"><span data-stu-id="1d4aa-112">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="1d4aa-113">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="1d4aa-113">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="1d4aa-114">Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="1d4aa-114">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |

## <a name="child-elements"></a><span data-ttu-id="1d4aa-115">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1d4aa-115">Child elements</span></span>

> [!NOTE]
> <span data-ttu-id="1d4aa-116">As configurações de *duração* e *WaitTimeout* são preteridas.</span><span class="sxs-lookup"><span data-stu-id="1d4aa-116">The *Duration* and *WaitTimeout* settings are deprecated.</span></span> <span data-ttu-id="1d4aa-117">Eles ainda estão presentes na interface do usuário Agendador de Tarefas, e seus métodos de interface ainda podem retornar valores válidos, mas não são mais usados.</span><span class="sxs-lookup"><span data-stu-id="1d4aa-117">They're still present in the Task Scheduler user interface, and their interface methods may still return valid values, but they're no longer used.</span></span>

| <span data-ttu-id="1d4aa-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="1d4aa-118">Element</span></span>                                                                                  | <span data-ttu-id="1d4aa-119">Type</span><span class="sxs-lookup"><span data-stu-id="1d4aa-119">Type</span></span>     | <span data-ttu-id="1d4aa-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="1d4aa-120">Description</span></span>                                                                                                              |
|------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d4aa-121">**RestartOnIdle**</span><span class="sxs-lookup"><span data-stu-id="1d4aa-121">**RestartOnIdle**</span></span>](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | <span data-ttu-id="1d4aa-122">booleano</span><span class="sxs-lookup"><span data-stu-id="1d4aa-122">boolean</span></span>  | <span data-ttu-id="1d4aa-123">Especifica se a tarefa é reiniciada quando o computador percorre uma condição ociosa mais de uma vez.</span><span class="sxs-lookup"><span data-stu-id="1d4aa-123">Specifies whether the task is restarted when the computer cycles into an idle condition more than once.</span></span><br/>       |
| [<span data-ttu-id="1d4aa-124">**StopOnIdleEnd**</span><span class="sxs-lookup"><span data-stu-id="1d4aa-124">**StopOnIdleEnd**</span></span>](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | <span data-ttu-id="1d4aa-125">booleano</span><span class="sxs-lookup"><span data-stu-id="1d4aa-125">boolean</span></span>  | <span data-ttu-id="1d4aa-126">Especifica que o Agendador de Tarefas interromperá a tarefa se a condição de ociosidade terminar antes de a tarefa ser concluída.</span><span class="sxs-lookup"><span data-stu-id="1d4aa-126">Specifies that the Task Scheduler will stop the task if the idle condition ends before the task is completed.</span></span><br/> |
| <span data-ttu-id="1d4aa-127">**Preterido**: [ **duração**](taskschedulerschema-duration-idlesettingstype-element.md)</span><span class="sxs-lookup"><span data-stu-id="1d4aa-127">**Deprecated**: [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md)</span></span>                | <span data-ttu-id="1d4aa-128">duration</span><span class="sxs-lookup"><span data-stu-id="1d4aa-128">duration</span></span> | <span data-ttu-id="1d4aa-129">Especifica por quanto tempo o computador deve estar em um estado ocioso antes que a tarefa seja executada.</span><span class="sxs-lookup"><span data-stu-id="1d4aa-129">Specifies how long the computer must be in an idle state before the task is run.</span></span><br/>                              |
| <span data-ttu-id="1d4aa-130">**Preterido**: [ **WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md)</span><span class="sxs-lookup"><span data-stu-id="1d4aa-130">**Deprecated**: [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md)</span></span>          | <span data-ttu-id="1d4aa-131">duration</span><span class="sxs-lookup"><span data-stu-id="1d4aa-131">duration</span></span> | <span data-ttu-id="1d4aa-132">Especifica a quantidade de tempo que o Agendador de Tarefas aguardará a ocorrência de uma condição ociosa.</span><span class="sxs-lookup"><span data-stu-id="1d4aa-132">Specifies the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span><br/>                |

## <a name="remarks"></a><span data-ttu-id="1d4aa-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d4aa-133">Remarks</span></span>

<span data-ttu-id="1d4aa-134">Para desenvolvimento de script, as configurações ociosas são especificadas usando a propriedade [**TaskSettings. IdleSettings**](tasksettings-idlesettings.md) .</span><span class="sxs-lookup"><span data-stu-id="1d4aa-134">For script development, idle settings are specified using the [**TaskSettings.IdleSettings**](tasksettings-idlesettings.md) property.</span></span>

<span data-ttu-id="1d4aa-135">Para desenvolvimento em C++, as configurações ociosas são especificadas usando a propriedade [**ITaskSettings:: IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings) .</span><span class="sxs-lookup"><span data-stu-id="1d4aa-135">For C++ development, idle settings are specified using the [**ITaskSettings::IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings) property.</span></span>

## <a name="examples"></a><span data-ttu-id="1d4aa-136">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1d4aa-136">Examples</span></span>

<span data-ttu-id="1d4aa-137">O XML a seguir define um elemento Settings que permite que Agendador de Tarefas Aguarde 24 horas para uma condição ociosa e, em seguida, permite que apenas 10 minutos {IdleDuration) iniciem a tarefa.</span><span class="sxs-lookup"><span data-stu-id="1d4aa-137">The following XML defines a settings element that allows Task Scheduler to wait 24 hours for an idle condition and then allows only 10 minutes {IdleDuration) to initiate the task.</span></span>

```XML
<Settings>
    <IdleSettings>
        <StopOnIdleEnd>false</StopOnIdleEnd>
        <RestartOnIdle>false</RestartOnIdle> 
        <!-- WaitTimeout and Duration have been deprecated -->
        <Duration>PT5M</Duration>
        <WaitTimeout>PT24H</WaitTimeout>
    </IdleSettings>       
</Settings>
```

## <a name="requirements"></a><span data-ttu-id="1d4aa-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d4aa-138">Requirements</span></span>

| <span data-ttu-id="1d4aa-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d4aa-139">Requirement</span></span> | <span data-ttu-id="1d4aa-140">Valor</span><span class="sxs-lookup"><span data-stu-id="1d4aa-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1d4aa-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d4aa-141">Minimum supported client</span></span><br/> | <span data-ttu-id="1d4aa-142">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1d4aa-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1d4aa-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d4aa-143">Minimum supported server</span></span><br/> | <span data-ttu-id="1d4aa-144">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1d4aa-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |

## <a name="see-also"></a><span data-ttu-id="1d4aa-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d4aa-145">See also</span></span>

[<span data-ttu-id="1d4aa-146">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="1d4aa-146">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)

[<span data-ttu-id="1d4aa-147">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="1d4aa-147">Task Scheduler</span></span>](task-scheduler-start-page.md)
