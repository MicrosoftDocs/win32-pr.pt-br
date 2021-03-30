---
title: Elemento data (taskType)
description: Define os dados de adição associados à tarefa, mas, caso contrário, não são usados pelo serviço de Agendador de Tarefas.
ms.assetid: 296cd33d-5f82-4de7-84a7-e791619ad0b5
keywords:
- Agendador de Tarefas de elemento de dados
topic_type:
- apiref
api_name:
- Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3afff1cbd81ede49568afdc9e516d87a57ff9e5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644481"
---
# <a name="data-tasktype-element"></a><span data-ttu-id="5cf7a-104">Elemento data (taskType)</span><span class="sxs-lookup"><span data-stu-id="5cf7a-104">Data (taskType) Element</span></span>

<span data-ttu-id="5cf7a-105">Define os dados de adição associados à tarefa, mas, caso contrário, não são usados pelo serviço de Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-105">Defines addition data that is associated with the task, but is otherwise unused by the Task Scheduler service.</span></span>

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

<span data-ttu-id="5cf7a-106">O elemento de **dados** é definido pelo tipo complexo [**TaskType**](taskschedulerschema-tasktype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5cf7a-106">The **Data** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5cf7a-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="5cf7a-107">Parent element</span></span>



| <span data-ttu-id="5cf7a-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="5cf7a-108">Element</span></span>                                          | <span data-ttu-id="5cf7a-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="5cf7a-109">Derived from</span></span>                                                 | <span data-ttu-id="5cf7a-110">Description</span><span class="sxs-lookup"><span data-stu-id="5cf7a-110">Description</span></span>                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="5cf7a-111">**Tarefa**</span><span class="sxs-lookup"><span data-stu-id="5cf7a-111">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="5cf7a-112">**taskType**</span><span class="sxs-lookup"><span data-stu-id="5cf7a-112">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="5cf7a-113">Define a tarefa que é executada pelo serviço de Agendador de Tarefas.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-113">Defines the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5cf7a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5cf7a-114">Remarks</span></span>

<span data-ttu-id="5cf7a-115">Como um exemplo desse tipo de dados, o serviço de Logs e Alertas de Desempenho usa essa propriedade como um contêiner de armazenamento para a consulta de contador de desempenho associada a uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="5cf7a-115">As an example of this type of data, the Performance Logs and Alerts service uses this property as a storage container for the perf counter query associated with a task.</span></span>

<span data-ttu-id="5cf7a-116">Para o desenvolvimento em C++, os dados de uma tarefa são especificados usando a [**propriedade data de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_data).</span><span class="sxs-lookup"><span data-stu-id="5cf7a-116">For C++ development, the data of a task is specified using the [**Data property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_data).</span></span>

<span data-ttu-id="5cf7a-117">No desenvolvimento de scripts, os dados de uma tarefa são especificados usando a propriedade [**TaskDefinition. Data**](taskdefinition-data.md) .</span><span class="sxs-lookup"><span data-stu-id="5cf7a-117">In scripting development, the data of a task is specified using the [**TaskDefinition.Data**](taskdefinition-data.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cf7a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cf7a-118">Requirements</span></span>



| <span data-ttu-id="5cf7a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cf7a-119">Requirement</span></span> | <span data-ttu-id="5cf7a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="5cf7a-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5cf7a-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5cf7a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5cf7a-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5cf7a-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5cf7a-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5cf7a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5cf7a-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5cf7a-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5cf7a-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5cf7a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cf7a-126">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="5cf7a-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="5cf7a-127">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="5cf7a-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





