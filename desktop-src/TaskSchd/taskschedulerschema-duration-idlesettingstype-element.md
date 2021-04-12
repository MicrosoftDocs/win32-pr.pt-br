---
title: Elemento Duration (idleSettingsType)
description: Especifica por quanto tempo o computador deve estar em um estado ocioso antes que a tarefa seja executada.
ms.assetid: 89584694-0685-44e2-b8b7-69e47ee28d5d
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
ms.openlocfilehash: 31ad092693c72dcc33357f4b7e21436e2cba8af8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499303"
---
# <a name="duration-idlesettingstype-element"></a><span data-ttu-id="011bf-104">Elemento Duration (idleSettingsType)</span><span class="sxs-lookup"><span data-stu-id="011bf-104">Duration (idleSettingsType) Element</span></span>

<span data-ttu-id="011bf-105">Especifica por quanto tempo o computador deve estar em um estado ocioso antes que a tarefa seja executada.</span><span class="sxs-lookup"><span data-stu-id="011bf-105">Specifies how long the computer must be in an idle state before the task is run.</span></span> <span data-ttu-id="011bf-106">O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="011bf-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="011bf-107">O valor mínimo é um minuto.</span><span class="sxs-lookup"><span data-stu-id="011bf-107">The minimum value is one minute.</span></span> <span data-ttu-id="011bf-108">Para obter mais informações sobre o tipo de duração, consulte <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="011bf-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Duration"
    default="PT10M"
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

<span data-ttu-id="011bf-109">O elemento é definido pelo tipo complexo [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="011bf-109">The element is defined by the [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="011bf-110">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="011bf-110">Parent element</span></span>



| <span data-ttu-id="011bf-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="011bf-111">Element</span></span>                                                                       | <span data-ttu-id="011bf-112">Derivado de</span><span class="sxs-lookup"><span data-stu-id="011bf-112">Derived from</span></span>                                                                 | <span data-ttu-id="011bf-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="011bf-113">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="011bf-114">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="011bf-114">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md) | [<span data-ttu-id="011bf-115">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="011bf-115">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md) | <span data-ttu-id="011bf-116">Especifica como a Agendador de Tarefas executa tarefas quando o computador está em um estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="011bf-116">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="011bf-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="011bf-117">Remarks</span></span>

<span data-ttu-id="011bf-118">Para a programação de script, essa configuração ociosa é especificada usando a propriedade [**IdleSettings. IdleDuration**](idlesettings-idleduration.md) .</span><span class="sxs-lookup"><span data-stu-id="011bf-118">For script programming, this idle setting is specified using the [**IdleSettings.IdleDuration**](idlesettings-idleduration.md) property.</span></span>

<span data-ttu-id="011bf-119">Para a programação C++, essa configuração ociosa é especificada usando a propriedade [**IIdleSettings:: IdleDuration**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_idleduration) .</span><span class="sxs-lookup"><span data-stu-id="011bf-119">For C++ programming, this idle setting is specified using the [**IIdleSettings::IdleDuration**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_idleduration) property.</span></span>

## <a name="examples"></a><span data-ttu-id="011bf-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="011bf-120">Examples</span></span>

<span data-ttu-id="011bf-121">O XML a seguir define uma configuração ociosa que permite 5 minutos para a tarefa ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="011bf-121">The following XML defines an idle setting that allows 5 minutes for the task to start.</span></span>


```XML
<IdleSettings>
    <Duration>PT5M</Duration>
</IdleSettings>
```



## <a name="requirements"></a><span data-ttu-id="011bf-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="011bf-122">Requirements</span></span>



| <span data-ttu-id="011bf-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="011bf-123">Requirement</span></span> | <span data-ttu-id="011bf-124">Valor</span><span class="sxs-lookup"><span data-stu-id="011bf-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="011bf-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="011bf-125">Minimum supported client</span></span><br/> | <span data-ttu-id="011bf-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="011bf-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="011bf-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="011bf-127">Minimum supported server</span></span><br/> | <span data-ttu-id="011bf-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="011bf-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="011bf-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="011bf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="011bf-130">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="011bf-130">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="011bf-131">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="011bf-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





