---
title: Elemento Interval (repetiçãotype)
description: Especifica a quantidade de tempo entre cada reinicialização da tarefa.
ms.assetid: 28c6475a-88e3-44ac-92c7-6f463e8460c9
keywords:
- Elemento Interval Agendador de Tarefas
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9720bc2257d4c0b45116089bfdd4113335fc6b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918214"
---
# <a name="interval-repetitiontype-element"></a><span data-ttu-id="54baf-104">Elemento Interval (repetiçãotype)</span><span class="sxs-lookup"><span data-stu-id="54baf-104">Interval (repetitionType) Element</span></span>

<span data-ttu-id="54baf-105">Especifica a quantidade de tempo entre cada reinicialização da tarefa.</span><span class="sxs-lookup"><span data-stu-id="54baf-105">Specifies the amount of time between each restart of the task.</span></span> <span data-ttu-id="54baf-106">O formato para essa cadeia de caracteres é P <days> dt <hours> H <minutes> M <seconds> S (por exemplo, "PT5M" é de 5 minutos, "PT1H" é de 1 hora e "PT20M" é de 20 minutos).</span><span class="sxs-lookup"><span data-stu-id="54baf-106">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="54baf-107">O tempo máximo permitido é de 31 dias e o tempo mínimo permitido é de 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="54baf-107">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

``` syntax
<xs:element name="Interval">
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
            <xs:maxInclusive
                value="P31D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="54baf-108">O elemento é definido pelo tipo complexo de [**repetição**](taskschedulerschema-repetitiontype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="54baf-108">The element is defined by the [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="54baf-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="54baf-109">Parent element</span></span>



| <span data-ttu-id="54baf-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="54baf-110">Element</span></span>                                                                      | <span data-ttu-id="54baf-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="54baf-111">Derived from</span></span>                                                             | <span data-ttu-id="54baf-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="54baf-112">Description</span></span>                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="54baf-113">**Repetição**</span><span class="sxs-lookup"><span data-stu-id="54baf-113">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md) | [<span data-ttu-id="54baf-114">**repetição**</span><span class="sxs-lookup"><span data-stu-id="54baf-114">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="54baf-115">Especifica com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="54baf-115">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="54baf-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="54baf-116">Remarks</span></span>

<span data-ttu-id="54baf-117">Para o desenvolvimento de scripts, o intervalo do padrão de repetição é especificado usando a propriedade [**RepetitionPattern. Interval**](repetitionpattern-interval.md) .</span><span class="sxs-lookup"><span data-stu-id="54baf-117">For scripting development, the interval of the repetition pattern is specified using the [**RepetitionPattern.Interval**](repetitionpattern-interval.md) property.</span></span>

<span data-ttu-id="54baf-118">Para desenvolvimento em C++, o intervalo do padrão de repetição é especificado usando a propriedade [**IRepetitionPattern:: Interval**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval) .</span><span class="sxs-lookup"><span data-stu-id="54baf-118">For C++ development, the interval of the repetition pattern is specified using the [**IRepetitionPattern::Interval**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="54baf-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="54baf-119">Examples</span></span>

<span data-ttu-id="54baf-120">Para obter um exemplo completo do XML para uma tarefa que usa um intervalo de repetição, consulte [exemplo de gatilho diário (XML)](daily-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="54baf-120">For a complete example of the XML for a task that uses a repetition interval, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="54baf-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54baf-121">Requirements</span></span>



| <span data-ttu-id="54baf-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="54baf-122">Requirement</span></span> | <span data-ttu-id="54baf-123">Valor</span><span class="sxs-lookup"><span data-stu-id="54baf-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="54baf-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54baf-124">Minimum supported client</span></span><br/> | <span data-ttu-id="54baf-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="54baf-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="54baf-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54baf-126">Minimum supported server</span></span><br/> | <span data-ttu-id="54baf-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="54baf-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="54baf-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="54baf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54baf-129">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="54baf-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="54baf-130">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="54baf-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





