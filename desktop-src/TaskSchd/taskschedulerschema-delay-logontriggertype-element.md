---
title: Elemento Delay (logonTriggerType)
description: Quantidade de tempo entre quando o usuário faz logon e quando a tarefa é iniciada.
ms.assetid: daab29f7-5d05-4e6d-a0c0-7b83b4d0b941
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
ms.openlocfilehash: a820bad3d68cfb0a697f795a9fd7326c9e52abe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455875"
---
# <a name="delay-logontriggertype-element"></a><span data-ttu-id="3296f-104">Elemento Delay (logonTriggerType)</span><span class="sxs-lookup"><span data-stu-id="3296f-104">Delay (logonTriggerType) Element</span></span>

<span data-ttu-id="3296f-105">Quantidade de tempo entre quando o usuário faz logon e quando a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="3296f-105">Amount of time between when the user logs on and when the task is started.</span></span> <span data-ttu-id="3296f-106">O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="3296f-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="3296f-107">Para obter mais informações sobre o tipo de duração, consulte <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="3296f-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="3296f-108">O elemento **Delay** é definido pelo tipo complexo [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="3296f-108">The **Delay** element is defined by the [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="3296f-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="3296f-109">Parent element</span></span>



| <span data-ttu-id="3296f-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="3296f-110">Element</span></span>                                                                       | <span data-ttu-id="3296f-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="3296f-111">Derived from</span></span>                                                                 | <span data-ttu-id="3296f-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="3296f-112">Description</span></span>                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="3296f-113">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="3296f-113">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md) | [<span data-ttu-id="3296f-114">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="3296f-114">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md) | <span data-ttu-id="3296f-115">Especifica um gatilho que inicia uma tarefa quando um usuário faz logon.</span><span class="sxs-lookup"><span data-stu-id="3296f-115">Specifies a trigger that starts a task when a user logs on.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3296f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3296f-116">Remarks</span></span>

<span data-ttu-id="3296f-117">Para o desenvolvimento de scripts, o atraso do gatilho de logon é especificado usando a propriedade [**LogonTrigger. Delay**](logontrigger-delay.md) .</span><span class="sxs-lookup"><span data-stu-id="3296f-117">For scripting development, the logon trigger delay is specified using the [**LogonTrigger.Delay**](logontrigger-delay.md) property.</span></span>

<span data-ttu-id="3296f-118">Para desenvolvimento em C++, o identificador de usuário para o gatilho de logon é especificado usando a propriedade [**ILogonTrigger::D epetição**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_delay) .</span><span class="sxs-lookup"><span data-stu-id="3296f-118">For C++ development, the user identifier for the logon trigger is specified using the [**ILogonTrigger::Delay**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_delay) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="3296f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3296f-119">Requirements</span></span>



| <span data-ttu-id="3296f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3296f-120">Requirement</span></span> | <span data-ttu-id="3296f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="3296f-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3296f-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3296f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3296f-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3296f-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3296f-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3296f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3296f-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3296f-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3296f-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="3296f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3296f-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="3296f-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="3296f-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="3296f-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





