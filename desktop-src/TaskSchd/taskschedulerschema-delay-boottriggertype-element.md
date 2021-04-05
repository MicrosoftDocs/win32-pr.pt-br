---
title: Elemento Delay (bootTriggerType)
description: Especifica a quantidade de tempo entre quando o sistema é inicializado e quando a tarefa é iniciada.
ms.assetid: 2a583069-ad38-43b4-bcf2-f7c9101f1927
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
ms.openlocfilehash: 1ab28da8e9c739d3deff52572fe6a5d37f862119
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919186"
---
# <a name="delay-boottriggertype-element"></a><span data-ttu-id="f7365-104">Elemento Delay (bootTriggerType)</span><span class="sxs-lookup"><span data-stu-id="f7365-104">Delay (bootTriggerType) Element</span></span>

<span data-ttu-id="f7365-105">Especifica a quantidade de tempo entre quando o sistema é inicializado e quando a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="f7365-105">Specifies the amount of time between when the system is booted and when the task is started.</span></span> <span data-ttu-id="f7365-106">O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="f7365-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="f7365-107">Para obter mais informações sobre o tipo de duração, consulte <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="f7365-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="f7365-108">O elemento **Delay** é definido pelo tipo complexo [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f7365-108">The **Delay** element is defined by the [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f7365-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="f7365-109">Parent element</span></span>



| <span data-ttu-id="f7365-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="f7365-110">Element</span></span>                                                                     | <span data-ttu-id="f7365-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="f7365-111">Derived from</span></span>                                                               | <span data-ttu-id="f7365-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="f7365-112">Description</span></span>                                                                  |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="f7365-113">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="f7365-113">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md) | [<span data-ttu-id="f7365-114">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="f7365-114">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md) | <span data-ttu-id="f7365-115">Especifica um gatilho que inicia uma tarefa quando o sistema é inicializado.</span><span class="sxs-lookup"><span data-stu-id="f7365-115">Specifies a trigger that starts a task when the system is booted.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f7365-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7365-116">Remarks</span></span>

<span data-ttu-id="f7365-117">Para o desenvolvimento de script, o atraso do gatilho de evento é especificado pela propriedade [**BootTrigger. Delay**](boottrigger-delay.md) .</span><span class="sxs-lookup"><span data-stu-id="f7365-117">For script development, the event trigger delay is specified by the [**BootTrigger.Delay**](boottrigger-delay.md) property.</span></span>

<span data-ttu-id="f7365-118">Para desenvolvimento em C++, o atraso do gatilho de evento é especificado pela propriedade [**IBootTrigger::D epetição**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) .</span><span class="sxs-lookup"><span data-stu-id="f7365-118">For C++ development, the event trigger delay is specified by the [**IBootTrigger::Delay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7365-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7365-119">Requirements</span></span>



| <span data-ttu-id="f7365-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7365-120">Requirement</span></span> | <span data-ttu-id="f7365-121">Valor</span><span class="sxs-lookup"><span data-stu-id="f7365-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f7365-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7365-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f7365-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f7365-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f7365-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7365-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f7365-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f7365-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f7365-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7365-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7365-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="f7365-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f7365-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="f7365-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





