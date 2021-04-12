---
title: Elemento RandomDelay (calendarTriggerType)
description: Contém o tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho. | Elemento RandomDelay (calendarTriggerType)
ms.assetid: 497fab4e-ad63-43e6-a086-2d77b43662d9
keywords:
- Agendador de Tarefas do elemento RandomDelay
topic_type:
- apiref
api_name:
- RandomDelay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d71149bfeceeb6c17cafa27f56bb15bb184ead06
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298325"
---
# <a name="randomdelay-calendartriggertype-element"></a><span data-ttu-id="1b56d-105">Elemento RandomDelay (calendarTriggerType)</span><span class="sxs-lookup"><span data-stu-id="1b56d-105">RandomDelay (calendarTriggerType) Element</span></span>

<span data-ttu-id="1b56d-106">Contém o tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho.</span><span class="sxs-lookup"><span data-stu-id="1b56d-106">Contains the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="1b56d-107">O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="1b56d-107">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="1b56d-108">Para obter mais informações sobre o tipo de duração, consulte <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="1b56d-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="RandomDelay"
    type="duration"
    default="PT0M"
    minOccurs="0"
 />
```

<span data-ttu-id="1b56d-109">O elemento **RandomDelay** é definido pelo tipo complexo [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1b56d-109">The **RandomDelay** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1b56d-110">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="1b56d-110">Parent element</span></span>



| <span data-ttu-id="1b56d-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="1b56d-111">Element</span></span>                                                                                            | <span data-ttu-id="1b56d-112">Derivado de</span><span class="sxs-lookup"><span data-stu-id="1b56d-112">Derived from</span></span>                                                                       | <span data-ttu-id="1b56d-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="1b56d-113">Description</span></span>                                                                                 |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1b56d-114">**CalendarTrigger (The Trigger)**</span><span class="sxs-lookup"><span data-stu-id="1b56d-114">**CalendarTrigger (triggerGroup)**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="1b56d-115">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="1b56d-115">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="1b56d-116">Especifica um gatilho diário, semanal, mensal ou um dia da semana (DOW) mensal.</span><span class="sxs-lookup"><span data-stu-id="1b56d-116">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="1b56d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b56d-117">Requirements</span></span>



| <span data-ttu-id="1b56d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b56d-118">Requirement</span></span> | <span data-ttu-id="1b56d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="1b56d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1b56d-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b56d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1b56d-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1b56d-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1b56d-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b56d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1b56d-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1b56d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





