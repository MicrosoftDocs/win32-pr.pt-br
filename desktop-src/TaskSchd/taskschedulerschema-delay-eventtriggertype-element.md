---
title: Elemento Delay (eventTriggertype)
description: Especifica a quantidade de tempo entre o momento em que o evento ocorre e quando a tarefa é iniciada.
ms.assetid: b38bebc7-9818-41f0-a277-cb0e63c28d86
keywords:
- Elemento Delay Agendador de Tarefas
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: de1117ff4f7e0f823b1b213721521e1b526125bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105783346"
---
# <a name="delay-eventtriggertype-element"></a><span data-ttu-id="98d78-104">Elemento Delay (eventTriggertype)</span><span class="sxs-lookup"><span data-stu-id="98d78-104">Delay (eventTriggerType) Element</span></span>

<span data-ttu-id="98d78-105">Especifica a quantidade de tempo entre o momento em que o evento ocorre e quando a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="98d78-105">Specifies the amount of time between when the event occurs and when the task is started.</span></span> <span data-ttu-id="98d78-106">O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="98d78-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="98d78-107">Para obter mais informações sobre o tipo de duração, consulte <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="98d78-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="98d78-108">O elemento **Delay** é definido pelo tipo complexo [**eventtriggertype**](taskschedulerschema-eventtriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="98d78-108">The **Delay** element is defined by the [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="98d78-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="98d78-109">Parent element</span></span>



| <span data-ttu-id="98d78-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="98d78-110">Element</span></span>                                                                       | <span data-ttu-id="98d78-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="98d78-111">Derived from</span></span>                                                                 | <span data-ttu-id="98d78-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="98d78-112">Description</span></span>                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="98d78-113">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="98d78-113">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md) | [<span data-ttu-id="98d78-114">**eventTriggertype**</span><span class="sxs-lookup"><span data-stu-id="98d78-114">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md) | <span data-ttu-id="98d78-115">Especifica um gatilho que inicia uma tarefa quando ocorre um evento do sistema.</span><span class="sxs-lookup"><span data-stu-id="98d78-115">Specifies a trigger that starts a task when a system event occurs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="98d78-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="98d78-116">Remarks</span></span>

<span data-ttu-id="98d78-117">Para o desenvolvimento de script, o atraso do gatilho de evento é especificado pela propriedade [**EventTrigger. Delay**](eventtrigger-delay.md) .</span><span class="sxs-lookup"><span data-stu-id="98d78-117">For script development, the event trigger delay is specified by the [**EventTrigger.Delay**](eventtrigger-delay.md) property.</span></span>

<span data-ttu-id="98d78-118">Para desenvolvimento em C++, o atraso do gatilho de evento é especificado pela propriedade [**IEventTrigger::D epetição**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_delay) .</span><span class="sxs-lookup"><span data-stu-id="98d78-118">For C++ development, the event trigger delay is specified by the [**IEventTrigger::Delay**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_delay) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="98d78-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98d78-119">Requirements</span></span>



| <span data-ttu-id="98d78-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="98d78-120">Requirement</span></span> | <span data-ttu-id="98d78-121">Valor</span><span class="sxs-lookup"><span data-stu-id="98d78-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="98d78-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98d78-122">Minimum supported client</span></span><br/> | <span data-ttu-id="98d78-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="98d78-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="98d78-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98d78-124">Minimum supported server</span></span><br/> | <span data-ttu-id="98d78-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="98d78-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="98d78-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="98d78-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98d78-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="98d78-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="98d78-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="98d78-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





