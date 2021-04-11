---
title: Elemento Duration (repetiçãotype)
description: Especifica por quanto tempo o padrão é repetido.
ms.assetid: a24f3827-18b2-465e-b132-77dce139e0d4
keywords:
- Elemento Duration Agendador de Tarefas
topic_type:
- apiref
api_name:
- Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3772abb0224b03db4985de126e1d9cc0058ab5de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295913"
---
# <a name="duration-repetitiontype-element"></a><span data-ttu-id="526c1-104">Elemento Duration (repetiçãotype)</span><span class="sxs-lookup"><span data-stu-id="526c1-104">Duration (repetitionType) Element</span></span>

<span data-ttu-id="526c1-105">Especifica por quanto tempo o padrão é repetido.</span><span class="sxs-lookup"><span data-stu-id="526c1-105">Specifies how long the pattern is repeated.</span></span> <span data-ttu-id="526c1-106">O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="526c1-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="526c1-107">Para obter mais informações sobre o tipo de duração, consulte <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="526c1-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span> <span data-ttu-id="526c1-108">Se nenhum valor for especificado para a duração, o padrão será repetido indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="526c1-108">If no value is specified for the duration, then the pattern is repeated indefinitely.</span></span> <span data-ttu-id="526c1-109">O valor mínimo é um minuto.</span><span class="sxs-lookup"><span data-stu-id="526c1-109">The minimum value is one minute.</span></span>

``` syntax
<xs:element name="Duration"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="526c1-110">O elemento é definido pelo tipo complexo de [**repetição**](taskschedulerschema-repetitiontype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="526c1-110">The element is defined by the [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="526c1-111">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="526c1-111">Parent element</span></span>



| <span data-ttu-id="526c1-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="526c1-112">Element</span></span>                                                                      | <span data-ttu-id="526c1-113">Derivado de</span><span class="sxs-lookup"><span data-stu-id="526c1-113">Derived from</span></span>                                                             | <span data-ttu-id="526c1-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="526c1-114">Description</span></span>                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="526c1-115">**Repetição**</span><span class="sxs-lookup"><span data-stu-id="526c1-115">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md) | [<span data-ttu-id="526c1-116">**repetição**</span><span class="sxs-lookup"><span data-stu-id="526c1-116">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="526c1-117">Especifica com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="526c1-117">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="526c1-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="526c1-118">Remarks</span></span>

<span data-ttu-id="526c1-119">Para aplicativos de script, a duração do padrão é especificada usando a propriedade [**RepetitionPattern. Duration**](repetitionpattern-duration.md) .</span><span class="sxs-lookup"><span data-stu-id="526c1-119">For scripting applications, the duration of the pattern is specified using the [**RepetitionPattern.Duration**](repetitionpattern-duration.md) property.</span></span>

<span data-ttu-id="526c1-120">Para aplicativos C++, a duração do padrão é especificada usando a propriedade [**IRepetitionPattern::D uração**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_duration) .</span><span class="sxs-lookup"><span data-stu-id="526c1-120">For C++ applications, the duration of the pattern is specified using the [**IRepetitionPattern::Duration**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_duration) property.</span></span>

## <a name="examples"></a><span data-ttu-id="526c1-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="526c1-121">Examples</span></span>

<span data-ttu-id="526c1-122">O XML a seguir define um padrão de repetição para um gatilho.</span><span class="sxs-lookup"><span data-stu-id="526c1-122">The following XML defines a repetition pattern for a trigger.</span></span>


```XML
<Repetition>
    <Interval></Interval>
    <Duration></Duration>
    <StopAtDurationEnd>true</StopAtDirationEnd>
</Repetition>
```



## <a name="requirements"></a><span data-ttu-id="526c1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="526c1-123">Requirements</span></span>



| <span data-ttu-id="526c1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="526c1-124">Requirement</span></span> | <span data-ttu-id="526c1-125">Valor</span><span class="sxs-lookup"><span data-stu-id="526c1-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="526c1-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="526c1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="526c1-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="526c1-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="526c1-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="526c1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="526c1-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="526c1-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="526c1-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="526c1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="526c1-131">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="526c1-131">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="526c1-132">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="526c1-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





