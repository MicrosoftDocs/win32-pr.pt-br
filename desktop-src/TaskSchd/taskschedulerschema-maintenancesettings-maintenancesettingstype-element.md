---
title: Elemento MaintenanceSettings (maintenanceSettingsType)
description: Especifica como a Agendador de Tarefas executa tarefas durante a manutenção automática.
ms.assetid: 6A204980-851D-4487-A6CC-01BE262A517A
keywords:
- Agendador de Tarefas do elemento MaintenanceSettings
topic_type:
- apiref
api_name:
- MaintenanceSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca68876d8742ea04faa972d2ea7fd5f4b2071ffc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086068"
---
# <a name="maintenancesettings-maintenancesettingstype-element"></a><span data-ttu-id="e412e-104">Elemento MaintenanceSettings (maintenanceSettingsType)</span><span class="sxs-lookup"><span data-stu-id="e412e-104">MaintenanceSettings (maintenanceSettingsType) Element</span></span>

<span data-ttu-id="e412e-105">Especifica como a Agendador de Tarefas executa tarefas durante a manutenção automática.</span><span class="sxs-lookup"><span data-stu-id="e412e-105">Specifies how the Task Scheduler performs tasks during Automatic maintenance.</span></span>

``` syntax
<xs:element name="MaintenanceSettings"
    type="maintenanceSettingsType"
    minOccurs="0"
 />
```

<span data-ttu-id="e412e-106">O elemento **MaintenanceSettings** é definido pelo tipo complexo [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e412e-106">The **MaintenanceSettings** element is defined by the [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e412e-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="e412e-107">Parent element</span></span>



| <span data-ttu-id="e412e-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="e412e-108">Element</span></span>                                                           | <span data-ttu-id="e412e-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="e412e-109">Derived from</span></span>                                                         | <span data-ttu-id="e412e-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="e412e-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="e412e-111">**Configurações**</span><span class="sxs-lookup"><span data-stu-id="e412e-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="e412e-112">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="e412e-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="e412e-113">Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="e412e-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="e412e-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="e412e-114">Child elements</span></span>



| <span data-ttu-id="e412e-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="e412e-115">Element</span></span>                                                    | <span data-ttu-id="e412e-116">Type</span><span class="sxs-lookup"><span data-stu-id="e412e-116">Type</span></span>    | <span data-ttu-id="e412e-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="e412e-117">Description</span></span>                                                                                                                                                                                     |
|------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e412e-118">**Prazo**</span><span class="sxs-lookup"><span data-stu-id="e412e-118">**Deadline**</span></span>](taskschedulerschema-deadline-element.md)   |         | <span data-ttu-id="e412e-119">Especifica o período de tempo após o qual o Agendador de tarefas tentará iniciar a tarefa durante a manutenção automática de emergência, se ela não for concluída durante a manutenção regular.</span><span class="sxs-lookup"><span data-stu-id="e412e-119">Specifies the amount of time after which the Task scheduler will attempt to start task during emergency Automatic maintenance, if it failed to complete during regular maintenance.</span></span> <br/> |
| [<span data-ttu-id="e412e-120">**Exclusivo**</span><span class="sxs-lookup"><span data-stu-id="e412e-120">**Exclusive**</span></span>](taskschedulerschema-exclusive-element.md) | <span data-ttu-id="e412e-121">booleano</span><span class="sxs-lookup"><span data-stu-id="e412e-121">boolean</span></span> | <span data-ttu-id="e412e-122">Se definido como true, a tarefa será iniciada exclusivamente entre outras tarefas de manutenção.</span><span class="sxs-lookup"><span data-stu-id="e412e-122">If set to true, the task will be started exclusively among other maintenance tasks.</span></span> <br/>                                                                                                 |
| [<span data-ttu-id="e412e-123">**Período**</span><span class="sxs-lookup"><span data-stu-id="e412e-123">**Period**</span></span>](taskschedulerschema-period-element.md)       |         | <span data-ttu-id="e412e-124">Especifica com que frequência a tarefa precisa ser iniciada durante a manutenção automática.</span><span class="sxs-lookup"><span data-stu-id="e412e-124">Specifies how often the task needs to be started during Automatic maintenance.</span></span> <br/>                                                                                                      |



## <a name="remarks"></a><span data-ttu-id="e412e-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="e412e-125">Remarks</span></span>

<span data-ttu-id="e412e-126">Para a programação C++, essa configuração ociosa é especificada usando a propriedade [**ITaskSettings3:: MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings) .</span><span class="sxs-lookup"><span data-stu-id="e412e-126">For C++ programming, this idle setting is specified using the [**ITaskSettings3::MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings) property.</span></span>

## <a name="examples"></a><span data-ttu-id="e412e-127">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e412e-127">Examples</span></span>

<span data-ttu-id="e412e-128">O XML a seguir define um elemento Settings que instrui Agendador de Tarefas a executar a tarefa uma vez em 5 dias durante a manutenção automática regular e, se houver falha por 15 dias, começar a tentar a tarefa durante a manutenção automática de emergência.</span><span class="sxs-lookup"><span data-stu-id="e412e-128">The following XML defines a settings element that instructs Task Scheduler to execute task once in 5 days during regular Automatic maintenance and if failed for 15 days, start attempting the task during the emergency Automatic maintenance.</span></span>


```XML
<Settings>
    <MaintenanceSettings>
        <Period>P5D</Period>
        <Deadline>P15D</Deadline>
    </MaintenanceSettings>       
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="e412e-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e412e-129">Requirements</span></span>



| <span data-ttu-id="e412e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e412e-130">Requirement</span></span> | <span data-ttu-id="e412e-131">Valor</span><span class="sxs-lookup"><span data-stu-id="e412e-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e412e-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e412e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e412e-133">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e412e-133">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="e412e-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e412e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e412e-135">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e412e-135">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e412e-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="e412e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e412e-137">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="e412e-137">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="e412e-138">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="e412e-138">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





