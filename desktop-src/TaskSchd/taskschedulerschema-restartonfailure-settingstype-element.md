---
title: Elemento RestartOnFailure (settingstype)
description: Especifica que o Agendador de Tarefas tentará reiniciar a tarefa se a tarefa falhar por algum motivo.
ms.assetid: c90d8c62-dd97-4ea6-bd87-37b0915e0b38
keywords:
- Agendador de Tarefas do elemento RestartOnFailure
topic_type:
- apiref
api_name:
- RestartOnFailure
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4239d21362d589cae84252c728387b2a2b6159e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163625"
---
# <a name="restartonfailure-settingstype-element"></a><span data-ttu-id="f372b-104">Elemento RestartOnFailure (settingstype)</span><span class="sxs-lookup"><span data-stu-id="f372b-104">RestartOnFailure (settingsType) Element</span></span>

<span data-ttu-id="f372b-105">Especifica que o Agendador de Tarefas tentará reiniciar a tarefa se a tarefa falhar por algum motivo.</span><span class="sxs-lookup"><span data-stu-id="f372b-105">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span>

``` syntax
<xs:element name="RestartOnFailure"
    type="restartType"
    minOccurs="0"
 />
```

<span data-ttu-id="f372b-106">O elemento **RestartOnFailure** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f372b-106">The **RestartOnFailure** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f372b-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="f372b-107">Parent element</span></span>



| <span data-ttu-id="f372b-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="f372b-108">Element</span></span>                                                           | <span data-ttu-id="f372b-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="f372b-109">Derived from</span></span>                                                         | <span data-ttu-id="f372b-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f372b-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="f372b-111">**Configurações**</span><span class="sxs-lookup"><span data-stu-id="f372b-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="f372b-112">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="f372b-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="f372b-113">Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="f372b-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="f372b-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f372b-114">Child elements</span></span>



| <span data-ttu-id="f372b-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="f372b-115">Element</span></span>                                                              | <span data-ttu-id="f372b-116">Type</span><span class="sxs-lookup"><span data-stu-id="f372b-116">Type</span></span>         | <span data-ttu-id="f372b-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="f372b-117">Description</span></span>                                                                                        |
|----------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f372b-118">**Contar**</span><span class="sxs-lookup"><span data-stu-id="f372b-118">**Count**</span></span>](taskschedulerschema-count-restarttype-element.md)       | <span data-ttu-id="f372b-119">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="f372b-119">unsignedByte</span></span> | <span data-ttu-id="f372b-120">Especifica o número de vezes que o Agendador de Tarefas tentará reiniciar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="f372b-120">Specifies the number of times that the Task Scheduler will attempt to restart the task.</span></span><br/> |
| [<span data-ttu-id="f372b-121">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="f372b-121">**Interval**</span></span>](taskschedulerschema-interval-restarttype-element.md) | <span data-ttu-id="f372b-122">duration</span><span class="sxs-lookup"><span data-stu-id="f372b-122">duration</span></span>     | <span data-ttu-id="f372b-123">Especifica por quanto tempo o Agendador de Tarefas tentará reiniciar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="f372b-123">Specifies how long the Task Scheduler will attempt to restart the task.</span></span><br/>                 |



## <a name="remarks"></a><span data-ttu-id="f372b-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="f372b-124">Remarks</span></span>

<span data-ttu-id="f372b-125">Quando um aplicativo especifica as configurações de tarefa, essas informações são acessadas por meio das propriedades [**RestartCount**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount) e [**RestartInterval**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval) da interface [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) .</span><span class="sxs-lookup"><span data-stu-id="f372b-125">When an application specifies task settings, this information is accessed through the [**RestartCount**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount) and [**RestartInterval**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval) properties of the [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) interface.</span></span> <span data-ttu-id="f372b-126">Para scripts, essas informações são acessadas por meio das propriedades [**TaskSettings. RestartCount**](tasksettings-restartcount.md) e [**TaskSettings. RestartInterval**](tasksettings-restartinterval.md) .</span><span class="sxs-lookup"><span data-stu-id="f372b-126">For scripting, this information is accessed through the [**TaskSettings.RestartCount**](tasksettings-restartcount.md) and [**TaskSettings.RestartInterval**](tasksettings-restartinterval.md) properties.</span></span>

<span data-ttu-id="f372b-127">Ambos os elementos filho devem ser definidos para especificar como o Agendador de Tarefas reinicia a tarefa.</span><span class="sxs-lookup"><span data-stu-id="f372b-127">Both child elements must be set to specify how the Task Scheduler restarts the task.</span></span>

## <a name="requirements"></a><span data-ttu-id="f372b-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f372b-128">Requirements</span></span>



| <span data-ttu-id="f372b-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f372b-129">Requirement</span></span> | <span data-ttu-id="f372b-130">Valor</span><span class="sxs-lookup"><span data-stu-id="f372b-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f372b-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f372b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f372b-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f372b-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f372b-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f372b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f372b-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f372b-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f372b-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="f372b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f372b-136">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="f372b-136">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





