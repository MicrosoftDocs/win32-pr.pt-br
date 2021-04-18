---
title: Elemento WaitTimeout (idleSettingsType)
description: Especifica a quantidade de tempo que o Agendador de Tarefas aguardará a ocorrência de uma condição ociosa.
ms.assetid: 6a4cc80d-adc2-47a7-946f-a9f12eeb35a4
keywords:
- Agendador de Tarefas do elemento WaitTimeout
topic_type:
- apiref
api_name:
- WaitTimeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16f71a014358a8e0520274d1ff853cf6146aa05d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499608"
---
# <a name="waittimeout-idlesettingstype-element"></a><span data-ttu-id="f3920-104">Elemento WaitTimeout (idleSettingsType)</span><span class="sxs-lookup"><span data-stu-id="f3920-104">WaitTimeout (idleSettingsType) Element</span></span>

<span data-ttu-id="f3920-105">Especifica a quantidade de tempo que o Agendador de Tarefas aguardará a ocorrência de uma condição ociosa.</span><span class="sxs-lookup"><span data-stu-id="f3920-105">Specifies the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span> <span data-ttu-id="f3920-106">Se nenhum valor for especificado para esse elemento, o serviço de Agendador de Tarefas aguardará indefinidamente se uma condição ociosa ocorrer.</span><span class="sxs-lookup"><span data-stu-id="f3920-106">If no value is specified for this element, then the Task Scheduler service will wait indefinitely for an idle condition to occur.</span></span> <span data-ttu-id="f3920-107">O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="f3920-107">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="f3920-108">Para obter mais informações sobre o tipo de duração, consulte <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="f3920-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span> <span data-ttu-id="f3920-109">O tempo mínimo permitido é de 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="f3920-109">The minimum time allowed is 1 minute.</span></span>

``` syntax
<xs:element name="WaitTimeout"
    default="PT1H"
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

<span data-ttu-id="f3920-110">O elemento é definido pelo tipo complexo [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f3920-110">The element is defined by the [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f3920-111">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="f3920-111">Parent element</span></span>



| <span data-ttu-id="f3920-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="f3920-112">Element</span></span>                                                                       | <span data-ttu-id="f3920-113">Derivado de</span><span class="sxs-lookup"><span data-stu-id="f3920-113">Derived from</span></span>                                                                 | <span data-ttu-id="f3920-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="f3920-114">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3920-115">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="f3920-115">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md) | [<span data-ttu-id="f3920-116">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="f3920-116">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md) | <span data-ttu-id="f3920-117">Especifica como a Agendador de Tarefas executa tarefas quando o computador está em um estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="f3920-117">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f3920-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3920-118">Remarks</span></span>

<span data-ttu-id="f3920-119">Para o desenvolvimento de script, essa configuração ociosa é especificada usando a propriedade [**IdleSettings. WaitTimeout**](idlesettings-waittimeout.md) .</span><span class="sxs-lookup"><span data-stu-id="f3920-119">For script development, this idle setting is specified using the [**IdleSettings.WaitTimeout**](idlesettings-waittimeout.md) property.</span></span>

<span data-ttu-id="f3920-120">Para desenvolvimento em C++, essa configuração ociosa é especificada usando a propriedade [**IIdleSettings:: WaitTimeout**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout) .</span><span class="sxs-lookup"><span data-stu-id="f3920-120">For C++ development, this idle setting is specified using the [**IIdleSettings::WaitTimeout**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout) property.</span></span>

## <a name="examples"></a><span data-ttu-id="f3920-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f3920-121">Examples</span></span>

<span data-ttu-id="f3920-122">O XML a seguir define uma configuração ociosa que aguarda 24 horas para que uma condição ociosa ocorra.</span><span class="sxs-lookup"><span data-stu-id="f3920-122">The following XML defines an idle setting that waits 24 hours for an idle condition to occur.</span></span>


```XML
<IdleSettings>
    <WaitTimeout>PT24H</WaitTimeout>
</IdleSettings>
```



## <a name="requirements"></a><span data-ttu-id="f3920-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3920-123">Requirements</span></span>



| <span data-ttu-id="f3920-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3920-124">Requirement</span></span> | <span data-ttu-id="f3920-125">Valor</span><span class="sxs-lookup"><span data-stu-id="f3920-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f3920-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3920-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f3920-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f3920-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f3920-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3920-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f3920-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f3920-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f3920-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3920-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3920-131">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="f3920-131">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f3920-132">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="f3920-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





