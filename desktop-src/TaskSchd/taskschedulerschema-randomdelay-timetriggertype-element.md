---
title: Elemento RandomDelay (timetriggertype)
description: Contém o tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho. | Elemento RandomDelay (timetriggertype)
ms.assetid: 84dffd18-651d-4e81-8c02-6cee9759a9b9
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
ms.openlocfilehash: a28613cb236b6dc8a3ae77dce9452423a992a866
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105810111"
---
# <a name="randomdelay-timetriggertype-element"></a><span data-ttu-id="bb2d1-105">Elemento RandomDelay (timetriggertype)</span><span class="sxs-lookup"><span data-stu-id="bb2d1-105">RandomDelay (timeTriggerType) Element</span></span>

<span data-ttu-id="bb2d1-106">Contém o tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho.</span><span class="sxs-lookup"><span data-stu-id="bb2d1-106">Contains the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="bb2d1-107">O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="bb2d1-107">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="bb2d1-108">Para obter mais informações sobre o tipo de duração, consulte <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="bb2d1-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="RandomDelay"
    type="duration"
    default="PT0M"
    minOccurs="0"
 />
```

<span data-ttu-id="bb2d1-109">O elemento é definido pelo tipo complexo [**Timetriggertype**](taskschedulerschema-timetriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="bb2d1-109">The element is defined by the [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="bb2d1-110">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="bb2d1-110">Parent element</span></span>



| <span data-ttu-id="bb2d1-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="bb2d1-111">Element</span></span>                                                                                    | <span data-ttu-id="bb2d1-112">Derivado de</span><span class="sxs-lookup"><span data-stu-id="bb2d1-112">Derived from</span></span>                                                               | <span data-ttu-id="bb2d1-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb2d1-113">Description</span></span>                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="bb2d1-114">**Gatilho de timetrigger (The Trigger)**</span><span class="sxs-lookup"><span data-stu-id="bb2d1-114">**TimeTrigger (triggerGroup)**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md) | [<span data-ttu-id="bb2d1-115">**timetriggertype**</span><span class="sxs-lookup"><span data-stu-id="bb2d1-115">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md) | <span data-ttu-id="bb2d1-116">Especifica um gatilho que inicia uma tarefa quando o gatilho é ativado.</span><span class="sxs-lookup"><span data-stu-id="bb2d1-116">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bb2d1-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb2d1-117">Remarks</span></span>

<span data-ttu-id="bb2d1-118">Para desenvolvimento em C++, consulte a [**Propriedade RandomDelay de ITimeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-itimetrigger-get_randomdelay).</span><span class="sxs-lookup"><span data-stu-id="bb2d1-118">For C++ development, see [**RandomDelay Property of ITimeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-itimetrigger-get_randomdelay).</span></span>

<span data-ttu-id="bb2d1-119">Para desenvolvimento de script, consulte [**timetrigger. RandomDelay**](timetrigger-randomdelay.md).</span><span class="sxs-lookup"><span data-stu-id="bb2d1-119">For script development, see [**TimeTrigger.RandomDelay**](timetrigger-randomdelay.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb2d1-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb2d1-120">Requirements</span></span>



| <span data-ttu-id="bb2d1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb2d1-121">Requirement</span></span> | <span data-ttu-id="bb2d1-122">Valor</span><span class="sxs-lookup"><span data-stu-id="bb2d1-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bb2d1-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb2d1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bb2d1-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bb2d1-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bb2d1-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb2d1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bb2d1-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bb2d1-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





