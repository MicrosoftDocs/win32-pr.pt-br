---
title: Elemento StopAtDurationEnd (rerepetiçãotype)
description: Especifica que uma instância em execução da tarefa é interrompida no final da duração do padrão de repetição.
ms.assetid: 4e34b5b2-ac93-4951-9de4-3e89614517d1
keywords:
- Agendador de Tarefas do elemento StopAtDurationEnd
topic_type:
- apiref
api_name:
- StopAtDurationEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a95f15f3a62d05b9bc28dc9f50b924979e2b748c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753334"
---
# <a name="stopatdurationend-repetitiontype-element"></a><span data-ttu-id="bfe92-104">Elemento StopAtDurationEnd (rerepetiçãotype)</span><span class="sxs-lookup"><span data-stu-id="bfe92-104">StopAtDurationEnd (repetitionType) Element</span></span>

<span data-ttu-id="bfe92-105">Especifica que uma instância em execução da tarefa é interrompida no final da duração do padrão de repetição.</span><span class="sxs-lookup"><span data-stu-id="bfe92-105">Specifies that a running instance of the task is stopped at the end of the repetition pattern duration.</span></span> <span data-ttu-id="bfe92-106">Isso será aplicável somente se as repetições estiverem definidas.</span><span class="sxs-lookup"><span data-stu-id="bfe92-106">This is applicable only if repetitions are set.</span></span>

``` syntax
<xs:element name="StopAtDurationEnd"
 type="boolean"
 />
```

<span data-ttu-id="bfe92-107">O elemento **StopAtDurationEnd** é definido pelo tipo complexo [**rerepetiçãotype**](taskschedulerschema-repetitiontype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="bfe92-107">The **StopAtDurationEnd** element is defined by the [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="bfe92-108">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="bfe92-108">Parent element</span></span>

| <span data-ttu-id="bfe92-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="bfe92-109">Element</span></span> | <span data-ttu-id="bfe92-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="bfe92-110">Derived from</span></span> | <span data-ttu-id="bfe92-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="bfe92-111">Description</span></span> |
|-|-|-|
| [<span data-ttu-id="bfe92-112">**Repetição**</span><span class="sxs-lookup"><span data-stu-id="bfe92-112">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md) | [<span data-ttu-id="bfe92-113">**repetição**</span><span class="sxs-lookup"><span data-stu-id="bfe92-113">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="bfe92-114">Especifica com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="bfe92-114">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |

## <a name="remarks"></a><span data-ttu-id="bfe92-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="bfe92-115">Remarks</span></span>

<span data-ttu-id="bfe92-116">Para o desenvolvimento de scripts, essa configuração é especificada usando a propriedade [**RepetitionPattern. StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) .</span><span class="sxs-lookup"><span data-stu-id="bfe92-116">For scripting development, this setting is specified using the [**RepetitionPattern.StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) property.</span></span>

<span data-ttu-id="bfe92-117">Para desenvolvimento em C++, essa configuração é especificada usando a propriedade [**IRepetitionPattern:: StopAtDurationEnd**](/windows/win32/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) .</span><span class="sxs-lookup"><span data-stu-id="bfe92-117">For C++ development, this setting is specified using the [**IRepetitionPattern::StopAtDurationEnd**](/windows/win32/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfe92-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfe92-118">Requirements</span></span>

| <span data-ttu-id="bfe92-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfe92-119">Requirement</span></span> | <span data-ttu-id="bfe92-120">Valor</span><span class="sxs-lookup"><span data-stu-id="bfe92-120">Value</span></span> |
|-|-|
| <span data-ttu-id="bfe92-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bfe92-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bfe92-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bfe92-122">Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bfe92-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bfe92-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bfe92-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bfe92-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |

## <a name="see-also"></a><span data-ttu-id="bfe92-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="bfe92-125">See also</span></span>

[<span data-ttu-id="bfe92-126">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="bfe92-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)

[<span data-ttu-id="bfe92-127">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="bfe92-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
