---
title: Elemento Task
description: Define a tarefa que é executada pelo serviço de Agendador de Tarefas.
ms.assetid: 103a332a-8620-4e0c-81b5-4782d85fc391
keywords:
- Elemento de tarefa Agendador de Tarefas
topic_type:
- apiref
api_name:
- Task
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38bac482f8546028d21db913e31dc4152f19f599
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824250"
---
# <a name="task-element"></a><span data-ttu-id="4c502-104">Elemento Task</span><span class="sxs-lookup"><span data-stu-id="4c502-104">Task Element</span></span>

<span data-ttu-id="4c502-105">Define a tarefa que é executada pelo serviço de Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="4c502-105">Defines the task that is performed by the Task Scheduler service.</span></span>

``` syntax
<xs:element name="Task"
    type="taskType"
>
    <xs:key name="PrincipalKey">
        <xs:selector
            xpath="td:Principals/td:Principal"
         />
        <xs:field
            xpath="@id"
         />
    </xs:key>
    <xs:keyref name="ContextKeyRef">
        <xs:selector
            xpath="td:Actions"
         />
        <xs:field
            xpath="@Context"
         />
    </xs:keyref>
    <xs:unique name="UniqueId">
        <xs:selector
            xpath="td:Principals/td:Principal|td:Triggers/td:BootTrigger|td:Triggers/td:RegistrationTrigger|td:Triggers/td:IdleTrigger|td:Triggers/td:TimeTrigger|td:Triggers/td:EventTrigger|td:Triggers/td:LogonTrigger|td:Triggers/td:SessionStateChangeTrigger|td:Triggers/td:CalendarTrigger|td:Actions/td:Exec|td:Actions/td:ComHandler|td:Actions/td:SendEmail"
         />
        <xs:field
            xpath="@id"
         />
    </xs:unique>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="4c502-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4c502-106">Child elements</span></span>



| <span data-ttu-id="4c502-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="4c502-107">Element</span></span>                                                                           | <span data-ttu-id="4c502-108">Type</span><span class="sxs-lookup"><span data-stu-id="4c502-108">Type</span></span>                                                                                 | <span data-ttu-id="4c502-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4c502-109">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c502-110">**Ações**</span><span class="sxs-lookup"><span data-stu-id="4c502-110">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)                   | [<span data-ttu-id="4c502-111">**ActionType**</span><span class="sxs-lookup"><span data-stu-id="4c502-111">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md)                   | <span data-ttu-id="4c502-112">Especifica as ações executadas pela tarefa.</span><span class="sxs-lookup"><span data-stu-id="4c502-112">Specifies the actions performed by the task.</span></span><br/>                                                                             |
| [<span data-ttu-id="4c502-113">**Dados**</span><span class="sxs-lookup"><span data-stu-id="4c502-113">**Data**</span></span>](taskschedulerschema-data-tasktype-element.md)                         | [<span data-ttu-id="4c502-114">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="4c502-114">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md)                         | <span data-ttu-id="4c502-115">Especifica os dados de adição associados à tarefa, mas, caso contrário, não são usados pelo serviço de Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="4c502-115">Specifies addition data that is associated with the task, but is otherwise unused by the Task Scheduler service.</span></span><br/>         |
| [<span data-ttu-id="4c502-116">**Principals**</span><span class="sxs-lookup"><span data-stu-id="4c502-116">**Principals**</span></span>](taskschedulerschema-principals-tasktype-element.md)             | [<span data-ttu-id="4c502-117">**principalsType**</span><span class="sxs-lookup"><span data-stu-id="4c502-117">**principalsType**</span></span>](taskschedulerschema-principalstype-complextype.md)             | <span data-ttu-id="4c502-118">Especifica os contextos de segurança que podem ser usados para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="4c502-118">Specifies the security contexts that can be used to run the task.</span></span><br/>                                                        |
| [<span data-ttu-id="4c502-119">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="4c502-119">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="4c502-120">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="4c502-120">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="4c502-121">Especifica informações administrativas sobre a tarefa, como o autor da tarefa e a data em que a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="4c502-121">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |
| [<span data-ttu-id="4c502-122">**Configurações**</span><span class="sxs-lookup"><span data-stu-id="4c502-122">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md)                 | [<span data-ttu-id="4c502-123">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="4c502-123">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md)                 | <span data-ttu-id="4c502-124">Especifica as configurações que o Agendador de Tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="4c502-124">Specifies the settings that the Task Scheduler uses to perform the task.</span></span><br/>                                                 |
| [<span data-ttu-id="4c502-125">**Gatilhos**</span><span class="sxs-lookup"><span data-stu-id="4c502-125">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md)                 | [<span data-ttu-id="4c502-126">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="4c502-126">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md)                 | <span data-ttu-id="4c502-127">Especifica os gatilhos que iniciam a tarefa.</span><span class="sxs-lookup"><span data-stu-id="4c502-127">Specifies the triggers that start the task.</span></span><br/>                                                                              |



## <a name="remarks"></a><span data-ttu-id="4c502-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c502-128">Remarks</span></span>

<span data-ttu-id="4c502-129">Para desenvolvimento em C++, consulte [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition).</span><span class="sxs-lookup"><span data-stu-id="4c502-129">For C++ development, see [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition).</span></span>

<span data-ttu-id="4c502-130">Para o desenvolvimento de scripts, consulte [**TaskDefinition**](taskdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="4c502-130">For script development, see [**TaskDefinition**](taskdefinition.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c502-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c502-131">Requirements</span></span>



| <span data-ttu-id="4c502-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c502-132">Requirement</span></span> | <span data-ttu-id="4c502-133">Valor</span><span class="sxs-lookup"><span data-stu-id="4c502-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4c502-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c502-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4c502-135">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4c502-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4c502-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c502-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4c502-137">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4c502-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





