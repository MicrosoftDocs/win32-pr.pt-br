---
title: Elemento Day (daysOfMonthType)
description: Especifica um dia do mês durante o qual a tarefa é executada.
ms.assetid: b213df09-9301-4a51-b000-edfdafbe861e
keywords:
- Agendador de Tarefas de elemento Day
topic_type:
- apiref
api_name:
- Day
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e8e06169d2b758264f181263a5cb717977a1602
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009096"
---
# <a name="day-daysofmonthtype-element"></a><span data-ttu-id="f9db5-104">Elemento Day (daysOfMonthType)</span><span class="sxs-lookup"><span data-stu-id="f9db5-104">Day (daysOfMonthType) Element</span></span>

<span data-ttu-id="f9db5-105">Especifica um dia do mês durante o qual a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="f9db5-105">Specifies a day of the month during which the task runs.</span></span>

``` syntax
<xs:element name="Day"
    type="dayOfMonthType"
 />
```

<span data-ttu-id="f9db5-106">O elemento **Day** é definido pelo tipo complexo [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f9db5-106">The **Day** element is defined by the [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f9db5-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="f9db5-107">Parent element</span></span>



| <span data-ttu-id="f9db5-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="f9db5-108">Element</span></span>                                                                            | <span data-ttu-id="f9db5-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="f9db5-109">Derived from</span></span>                                                               | <span data-ttu-id="f9db5-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9db5-110">Description</span></span>                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="f9db5-111">**DaysOfMonth**</span><span class="sxs-lookup"><span data-stu-id="f9db5-111">**DaysOfMonth**</span></span>](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [<span data-ttu-id="f9db5-112">**daysOfMonthType**</span><span class="sxs-lookup"><span data-stu-id="f9db5-112">**daysOfMonthType**</span></span>](taskschedulerschema-daysofmonthtype-complextype.md) | <span data-ttu-id="f9db5-113">Especifica os dias do mês durante os quais a tarefa é executada.</span><span class="sxs-lookup"><span data-stu-id="f9db5-113">Specifies the days of the month during which the task runs.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="f9db5-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f9db5-114">Examples</span></span>

<span data-ttu-id="f9db5-115">O XML a seguir define a parte de dias de um calendário mensal que executa a tarefa no 1º e no 15º dia do mês.</span><span class="sxs-lookup"><span data-stu-id="f9db5-115">The following XML defines the days portion of a monthly calendar that runs the task on the 1st and 15th day of the month.</span></span>


```XML
<DaysOfMonth>
    <Day>1</Day>
    <Day>15</Day>
</DaysOfMonth>
```



## <a name="requirements"></a><span data-ttu-id="f9db5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9db5-116">Requirements</span></span>



| <span data-ttu-id="f9db5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9db5-117">Requirement</span></span> | <span data-ttu-id="f9db5-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f9db5-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f9db5-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9db5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f9db5-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f9db5-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f9db5-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9db5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f9db5-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f9db5-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9db5-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9db5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9db5-124">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="f9db5-124">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





