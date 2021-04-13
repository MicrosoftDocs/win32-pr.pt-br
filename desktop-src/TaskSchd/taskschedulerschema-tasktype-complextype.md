---
title: Tipo complexo de taskType (Agendador de Tarefas)
description: Define os elementos filho e as informações de sequenciamento para o elemento Task.
ms.assetid: 622b2bf4-c7e0-403c-bd6c-99b687c1d439
keywords:
- tipo complexo de taskType Agendador de Tarefas
topic_type:
- apiref
api_name:
- taskType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e86174920c28614f6c871e3f0bb0bc322243009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455499"
---
# <a name="tasktype-complex-type"></a><span data-ttu-id="a0e3f-104">Tipo complexo de taskType</span><span class="sxs-lookup"><span data-stu-id="a0e3f-104">taskType Complex Type</span></span>

<span data-ttu-id="a0e3f-105">Define os elementos filho e as informações de sequenciamento para o elemento [**Task**](taskschedulerschema-task-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a0e3f-105">Defines the child elements and sequencing information for the [**Task**](taskschedulerschema-task-element.md) element.</span></span>

``` syntax
<xs:complexType name="taskType">
    <xs:all>
        <xs:element name="RegistrationInfo"
            type="registrationInfoType"
            minOccurs="0"
         />
        <xs:element name="Triggers"
            type="triggersType"
            minOccurs="0"
         />
        <xs:element name="Settings"
            type="settingsType"
            minOccurs="0"
         />
        <xs:element name="Data"
            type="dataType"
            minOccurs="0"
         />
        <xs:element name="Principals"
            type="principalsType"
            minOccurs="0"
         />
        <xs:element name="Actions"
            type="actionsType"
         />
    </xs:all>
    <xs:attribute name="version"
        type="versionType"
        use="optional"
        fixed="1.3"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a0e3f-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a0e3f-106">Child elements</span></span>



| <span data-ttu-id="a0e3f-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="a0e3f-107">Element</span></span>                                                                           | <span data-ttu-id="a0e3f-108">Type</span><span class="sxs-lookup"><span data-stu-id="a0e3f-108">Type</span></span>                                                                                 | <span data-ttu-id="a0e3f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="a0e3f-109">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0e3f-110">**Ações**</span><span class="sxs-lookup"><span data-stu-id="a0e3f-110">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)                   | [<span data-ttu-id="a0e3f-111">**ActionType**</span><span class="sxs-lookup"><span data-stu-id="a0e3f-111">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md)                   | <span data-ttu-id="a0e3f-112">Especifica as ações executadas pela tarefa.</span><span class="sxs-lookup"><span data-stu-id="a0e3f-112">Specifies the actions performed by the task.</span></span><br/>                                                                             |
| [<span data-ttu-id="a0e3f-113">**Dados**</span><span class="sxs-lookup"><span data-stu-id="a0e3f-113">**Data**</span></span>](taskschedulerschema-data-tasktype-element.md)                         | [<span data-ttu-id="a0e3f-114">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="a0e3f-114">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md)                         | <span data-ttu-id="a0e3f-115">Especifica os dados de adição associados à tarefa, mas, caso contrário, não são usados pelo serviço de Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="a0e3f-115">Specifies addition data that is associated with the task, but is otherwise unused by the Task Scheduler service.</span></span><br/>         |
| [<span data-ttu-id="a0e3f-116">**Principals**</span><span class="sxs-lookup"><span data-stu-id="a0e3f-116">**Principals**</span></span>](taskschedulerschema-principals-tasktype-element.md)             | [<span data-ttu-id="a0e3f-117">**principalsType**</span><span class="sxs-lookup"><span data-stu-id="a0e3f-117">**principalsType**</span></span>](taskschedulerschema-principalstype-complextype.md)             | <span data-ttu-id="a0e3f-118">Especifica os contextos de segurança que podem ser usados para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="a0e3f-118">Specifies the security contexts that can be used to run the task.</span></span><br/>                                                        |
| [<span data-ttu-id="a0e3f-119">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="a0e3f-119">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="a0e3f-120">**registrationInfoType**</span><span class="sxs-lookup"><span data-stu-id="a0e3f-120">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="a0e3f-121">Especifica informações administrativas sobre a tarefa, como o autor da tarefa e a data em que a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="a0e3f-121">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |
| [<span data-ttu-id="a0e3f-122">**Configurações**</span><span class="sxs-lookup"><span data-stu-id="a0e3f-122">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md)                 | [<span data-ttu-id="a0e3f-123">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="a0e3f-123">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md)                 | <span data-ttu-id="a0e3f-124">Especifica as configurações que o Agendador de Tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="a0e3f-124">Specifies the settings that the Task Scheduler uses to perform the task.</span></span><br/>                                                 |
| [<span data-ttu-id="a0e3f-125">**Gatilhos**</span><span class="sxs-lookup"><span data-stu-id="a0e3f-125">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md)                 | [<span data-ttu-id="a0e3f-126">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="a0e3f-126">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md)                 | <span data-ttu-id="a0e3f-127">Especifica os gatilhos que iniciam a tarefa.</span><span class="sxs-lookup"><span data-stu-id="a0e3f-127">Specifies the triggers that start the task.</span></span><br/>                                                                              |



## <a name="attributes"></a><span data-ttu-id="a0e3f-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="a0e3f-128">Attributes</span></span>



| <span data-ttu-id="a0e3f-129">Nome</span><span class="sxs-lookup"><span data-stu-id="a0e3f-129">Name</span></span>    | <span data-ttu-id="a0e3f-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="a0e3f-130">Type</span></span>                                                              | <span data-ttu-id="a0e3f-131">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="a0e3f-131">Description</span></span>                                   |
|---------|-------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="a0e3f-132">version</span><span class="sxs-lookup"><span data-stu-id="a0e3f-132">version</span></span> | [<span data-ttu-id="a0e3f-133">**versãotype**</span><span class="sxs-lookup"><span data-stu-id="a0e3f-133">**versionType**</span></span>](taskschedulerschema-versiontype-simpletype.md) | <span data-ttu-id="a0e3f-134">Especifica a versão da tarefa.</span><span class="sxs-lookup"><span data-stu-id="a0e3f-134">Specifies the version of the task.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a0e3f-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0e3f-135">Requirements</span></span>



| <span data-ttu-id="a0e3f-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0e3f-136">Requirement</span></span> | <span data-ttu-id="a0e3f-137">Valor</span><span class="sxs-lookup"><span data-stu-id="a0e3f-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a0e3f-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0e3f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a0e3f-139">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a0e3f-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a0e3f-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0e3f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a0e3f-141">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a0e3f-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a0e3f-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0e3f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0e3f-143">Tipos complexos de esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="a0e3f-143">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="a0e3f-144">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="a0e3f-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





