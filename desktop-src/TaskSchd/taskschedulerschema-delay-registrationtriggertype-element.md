---
title: Elemento Delay (registrationTriggerType)
description: Especifica a quantidade de tempo entre quando a tarefa é registrada e quando a tarefa é iniciada.
ms.assetid: 8955d86c-8306-45e7-93cf-eacf50e10075
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
ms.openlocfilehash: 4fe1a580a0e69c8e4816022971b2d0bc143544cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645219"
---
# <a name="delay-registrationtriggertype-element"></a><span data-ttu-id="37c21-104">Elemento Delay (registrationTriggerType)</span><span class="sxs-lookup"><span data-stu-id="37c21-104">Delay (registrationTriggerType) Element</span></span>

<span data-ttu-id="37c21-105">Especifica a quantidade de tempo entre quando a tarefa é registrada e quando a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="37c21-105">Specifies the amount of time between when the task is registered and when the task is started.</span></span> <span data-ttu-id="37c21-106">O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="37c21-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="37c21-107">Para obter mais informações sobre o tipo de duração, consulte <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="37c21-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="37c21-108">O elemento **Delay** é definido pelo tipo complexo [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="37c21-108">The **Delay** element is defined by the [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="37c21-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="37c21-109">Parent element</span></span>



| <span data-ttu-id="37c21-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="37c21-110">Element</span></span>                                                                                     | <span data-ttu-id="37c21-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="37c21-111">Derived from</span></span>                                                                               | <span data-ttu-id="37c21-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="37c21-112">Description</span></span>                                                                    |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="37c21-113">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="37c21-113">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="37c21-114">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="37c21-114">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="37c21-115">Especifica um gatilho que inicia uma tarefa quando a tarefa é registrada.</span><span class="sxs-lookup"><span data-stu-id="37c21-115">Specifies a trigger that starts a task when the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="37c21-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="37c21-116">Remarks</span></span>

<span data-ttu-id="37c21-117">Para o desenvolvimento de scripts, o atraso do gatilho de registro é especificado usando a propriedade [**RegistrationTrigger. Delay**](registrationtrigger-delay.md) .</span><span class="sxs-lookup"><span data-stu-id="37c21-117">For scripting development, the registration trigger delay is specified using the [**RegistrationTrigger.Delay**](registrationtrigger-delay.md) property.</span></span>

<span data-ttu-id="37c21-118">Para desenvolvimento em C++, o atraso do gatilho de registro é especificado usando a propriedade [**IRegistrationTrigger::D epetição**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) .</span><span class="sxs-lookup"><span data-stu-id="37c21-118">For C++ development, the registration trigger delay is specified using the [**IRegistrationTrigger::Delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) property.</span></span>

## <a name="examples"></a><span data-ttu-id="37c21-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="37c21-119">Examples</span></span>

<span data-ttu-id="37c21-120">O XML a seguir define um atraso de gatilho de registro que permite um atraso de 5 minutos entre o momento em que a tarefa é registrada e quando a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="37c21-120">The following XML defines a registration trigger delay that allows a 5 minute delay between when the task is registered and when the task is started.</span></span>


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled></Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay>PT5M<Delay>
 </BootTrigger>
```



## <a name="requirements"></a><span data-ttu-id="37c21-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37c21-121">Requirements</span></span>



| <span data-ttu-id="37c21-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="37c21-122">Requirement</span></span> | <span data-ttu-id="37c21-123">Valor</span><span class="sxs-lookup"><span data-stu-id="37c21-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="37c21-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37c21-124">Minimum supported client</span></span><br/> | <span data-ttu-id="37c21-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="37c21-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="37c21-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37c21-126">Minimum supported server</span></span><br/> | <span data-ttu-id="37c21-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="37c21-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="37c21-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="37c21-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37c21-129">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="37c21-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="37c21-130">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="37c21-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





