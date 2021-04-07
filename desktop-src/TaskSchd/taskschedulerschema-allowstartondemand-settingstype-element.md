---
title: Elemento AllowStartOnDemand (settingstype)
description: Especifica que a tarefa pode ser iniciada usando o comando executar ou o menu de contexto.
ms.assetid: 5a0f0842-9f09-4d52-bed2-45740945d9a5
keywords:
- Agendador de Tarefas do elemento AllowStartOnDemand
topic_type:
- apiref
api_name:
- AllowStartOnDemand
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec396bf10efbd11024fe39e57bdf05025db0e610
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918146"
---
# <a name="allowstartondemand-settingstype-element"></a><span data-ttu-id="1a4b3-104">Elemento AllowStartOnDemand (settingstype)</span><span class="sxs-lookup"><span data-stu-id="1a4b3-104">AllowStartOnDemand (settingsType) Element</span></span>

<span data-ttu-id="1a4b3-105">Especifica que a tarefa pode ser iniciada usando o comando executar ou o menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="1a4b3-105">Specifies that the task can be started using either the Run command or the Context menu.</span></span>

``` syntax
<xs:element name="AllowStartOnDemand"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

<span data-ttu-id="1a4b3-106">O elemento **AllowStartOnDemand** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1a4b3-106">The **AllowStartOnDemand** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1a4b3-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="1a4b3-107">Parent element</span></span>



| <span data-ttu-id="1a4b3-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="1a4b3-108">Element</span></span>                                                           | <span data-ttu-id="1a4b3-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="1a4b3-109">Derived from</span></span>                                                         | <span data-ttu-id="1a4b3-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="1a4b3-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="1a4b3-111">**Configurações**</span><span class="sxs-lookup"><span data-stu-id="1a4b3-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="1a4b3-112">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="1a4b3-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="1a4b3-113">Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="1a4b3-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1a4b3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a4b3-114">Remarks</span></span>

<span data-ttu-id="1a4b3-115">Quando esse elemento é definido como true, a tarefa pode ser iniciada independentemente de quando os gatilhos iniciam a tarefa.</span><span class="sxs-lookup"><span data-stu-id="1a4b3-115">When this element is set to True, the task can be started independently of when any triggers start the task.</span></span>

<span data-ttu-id="1a4b3-116">Para desenvolvimento em C++, consulte a [**Propriedade AllowDemandStart de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowdemandstart).</span><span class="sxs-lookup"><span data-stu-id="1a4b3-116">For C++ development, see the [**AllowDemandStart property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowdemandstart).</span></span>

<span data-ttu-id="1a4b3-117">Para desenvolvimento de script, consulte [**TaskSettings. AllowDemandStart**](tasksettings-allowdemandstart.md).</span><span class="sxs-lookup"><span data-stu-id="1a4b3-117">For script development, see [**TaskSettings.AllowDemandStart**](tasksettings-allowdemandstart.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1a4b3-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1a4b3-118">Examples</span></span>

<span data-ttu-id="1a4b3-119">Para obter um exemplo completo do XML para uma tarefa que permite iniciar a demanda, consulte [exemplo de gatilho de tempo (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="1a4b3-119">For a complete example of the XML for a task that allows demand start, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a4b3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a4b3-120">Requirements</span></span>



| <span data-ttu-id="1a4b3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a4b3-121">Requirement</span></span> | <span data-ttu-id="1a4b3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1a4b3-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1a4b3-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a4b3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1a4b3-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1a4b3-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1a4b3-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a4b3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1a4b3-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1a4b3-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1a4b3-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a4b3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a4b3-128">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="1a4b3-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





