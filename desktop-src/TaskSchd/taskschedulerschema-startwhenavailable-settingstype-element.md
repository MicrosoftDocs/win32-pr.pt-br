---
title: Elemento StartWhenAvailable (settingstype)
description: Especifica que o Agendador de Tarefas pode iniciar a tarefa a qualquer momento após o horário agendado ter passado.
ms.assetid: 1d65fd51-3a94-4083-8e38-2a652383656a
keywords:
- Agendador de Tarefas do elemento StartWhenAvailable
topic_type:
- apiref
api_name:
- StartWhenAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d86f6f6e75457d08e10ef40d728eaf3e3b00aa7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918143"
---
# <a name="startwhenavailable-settingstype-element"></a><span data-ttu-id="e612a-104">Elemento StartWhenAvailable (settingstype)</span><span class="sxs-lookup"><span data-stu-id="e612a-104">StartWhenAvailable (settingsType) Element</span></span>

<span data-ttu-id="e612a-105">Especifica que o Agendador de Tarefas pode iniciar a tarefa a qualquer momento após o horário agendado ter passado.</span><span class="sxs-lookup"><span data-stu-id="e612a-105">Specifies that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span>

``` syntax
<xs:element name="StartWhenAvailable"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="e612a-106">O elemento **StartWhenAvailable** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e612a-106">The **StartWhenAvailable** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e612a-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="e612a-107">Parent element</span></span>



| <span data-ttu-id="e612a-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="e612a-108">Element</span></span>                                                           | <span data-ttu-id="e612a-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="e612a-109">Derived from</span></span>                                                         | <span data-ttu-id="e612a-110">Description</span><span class="sxs-lookup"><span data-stu-id="e612a-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="e612a-111">**Configurações**</span><span class="sxs-lookup"><span data-stu-id="e612a-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="e612a-112">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="e612a-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="e612a-113">Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="e612a-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e612a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e612a-114">Remarks</span></span>

<span data-ttu-id="e612a-115">Essa propriedade só se aplica a tarefas com tempo.</span><span class="sxs-lookup"><span data-stu-id="e612a-115">This property applies only to timed tasks.</span></span>

<span data-ttu-id="e612a-116">Para desenvolvimento em C++, consulte a [**Propriedade StartWhenAvailable de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable).</span><span class="sxs-lookup"><span data-stu-id="e612a-116">For C++ development, see [**StartWhenAvailable Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable).</span></span>

<span data-ttu-id="e612a-117">Para desenvolvimento de script, consulte [**TaskSettings. StartWhenAvailable**](tasksettings-startwhenavailable.md).</span><span class="sxs-lookup"><span data-stu-id="e612a-117">For script development, see [**TaskSettings.StartWhenAvailable**](tasksettings-startwhenavailable.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e612a-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e612a-118">Examples</span></span>

<span data-ttu-id="e612a-119">O XML a seguir define um elemento Settings que permite que o Agendador de Tarefas inicie a tarefa quando ela estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="e612a-119">The following XML defines a settings element that allows the Task Scheduler to start the task when it is available.</span></span>


```XML
<Settings>
    <StartWhenAvailable>true</StartWhenAvailable>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="e612a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e612a-120">Requirements</span></span>



| <span data-ttu-id="e612a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e612a-121">Requirement</span></span> | <span data-ttu-id="e612a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e612a-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e612a-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e612a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e612a-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e612a-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e612a-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e612a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e612a-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e612a-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e612a-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e612a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e612a-128">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="e612a-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





