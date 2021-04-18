---
title: Elemento MultipleInstancesPolicy (settingstype)
description: Especifica a política que define como o Agendador de Tarefas lida com várias instâncias da tarefa.
ms.assetid: ec82d396-f83c-4684-98ab-f70e15ada075
keywords:
- Agendador de Tarefas do elemento MultipleInstancesPolicy
topic_type:
- apiref
api_name:
- MultipleInstancesPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5bcbbd26880f1ccced3e71b44dc93993d20f4a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105766959"
---
# <a name="multipleinstancespolicy-settingstype-element"></a><span data-ttu-id="3490d-104">Elemento MultipleInstancesPolicy (settingstype)</span><span class="sxs-lookup"><span data-stu-id="3490d-104">MultipleInstancesPolicy (settingsType) Element</span></span>

<span data-ttu-id="3490d-105">Especifica a política que define como o Agendador de Tarefas lida com várias instâncias da tarefa.</span><span class="sxs-lookup"><span data-stu-id="3490d-105">Specifies the policy that defines how the Task Scheduler deals with multiple instances of the task.</span></span>

``` syntax
<xs:element name="MultipleInstancesPolicy"
    type="multipleInstancesPolicyType"
 />
```

<span data-ttu-id="3490d-106">O elemento **MultipleInstancesPolicy** é definido pelo tipo simples [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) .</span><span class="sxs-lookup"><span data-stu-id="3490d-106">The **MultipleInstancesPolicy** element is defined by the [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) simple type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="3490d-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="3490d-107">Parent element</span></span>



| <span data-ttu-id="3490d-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="3490d-108">Element</span></span>                                                           | <span data-ttu-id="3490d-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="3490d-109">Derived from</span></span>                                                         | <span data-ttu-id="3490d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="3490d-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="3490d-111">**Configurações**</span><span class="sxs-lookup"><span data-stu-id="3490d-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="3490d-112">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="3490d-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="3490d-113">Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="3490d-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3490d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3490d-114">Remarks</span></span>

<span data-ttu-id="3490d-115">Para desenvolvimento em C++, consulte a [**Propriedade MultipleInstances de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_multipleinstances).</span><span class="sxs-lookup"><span data-stu-id="3490d-115">For C++ development, see [**MultipleInstances Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_multipleinstances).</span></span>

<span data-ttu-id="3490d-116">Para desenvolvimento de script, consulte [**TaskSettings. MultipleInstances**](tasksettings-multipleinstances.md).</span><span class="sxs-lookup"><span data-stu-id="3490d-116">For script development, see [**TaskSettings.MultipleInstances**](tasksettings-multipleinstances.md).</span></span>

### <a name="restricted-values"></a><span data-ttu-id="3490d-117">Valores restritos</span><span class="sxs-lookup"><span data-stu-id="3490d-117">Restricted Values</span></span>

<span data-ttu-id="3490d-118">Este elemento é restrito aos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="3490d-118">This element is restricted to the following values.</span></span>

-   <span data-ttu-id="3490d-119">Parallel: inicia uma nova instância enquanto uma instância existente está em execução.</span><span class="sxs-lookup"><span data-stu-id="3490d-119">Parallel: Starts a new instance while an existing instance is running.</span></span>
-   <span data-ttu-id="3490d-120">Fila: inicia uma nova instância da tarefa depois que todas as outras instâncias da tarefa são concluídas.</span><span class="sxs-lookup"><span data-stu-id="3490d-120">Queue: Starts a new instance of task after all other instances of the task are complete.</span></span>
-   <span data-ttu-id="3490d-121">IgnoreNew: padrão.</span><span class="sxs-lookup"><span data-stu-id="3490d-121">IgnoreNew: Default.</span></span> <span data-ttu-id="3490d-122">Não iniciará uma nova instância se uma instância existente da tarefa estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="3490d-122">Does not start a new instance if an existing instance of the task is running.</span></span>
-   <span data-ttu-id="3490d-123">StopExisting: para uma instância existente da tarefa antes de iniciar uma nova instância.</span><span class="sxs-lookup"><span data-stu-id="3490d-123">StopExisting: Stops an existing instance of the task before it starts a new instance.</span></span>

## <a name="examples"></a><span data-ttu-id="3490d-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3490d-124">Examples</span></span>

<span data-ttu-id="3490d-125">O XML a seguir define um elemento Settings que permite que várias instâncias da tarefa sejam executadas em paralelo.</span><span class="sxs-lookup"><span data-stu-id="3490d-125">The following XML defines a settings element that allows multiple instances of the task to run in parallel.</span></span>


```XML
<Settings>
    <MultipleInstancesPolicy>Parallel</MultipleInstancesPolicy>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="3490d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3490d-126">Requirements</span></span>



| <span data-ttu-id="3490d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3490d-127">Requirement</span></span> | <span data-ttu-id="3490d-128">Valor</span><span class="sxs-lookup"><span data-stu-id="3490d-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3490d-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3490d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3490d-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3490d-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3490d-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3490d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3490d-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3490d-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3490d-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="3490d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3490d-134">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="3490d-134">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





