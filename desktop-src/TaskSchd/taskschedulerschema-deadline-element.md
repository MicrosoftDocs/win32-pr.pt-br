---
title: Elemento prazo
description: Especifica quando o Agendador de tarefas deve iniciar a tarefa durante a manutenção automática de emergência, se ela não for concluída durante a manutenção automática regular.
ms.assetid: 34E33FAE-888E-4E82-83B8-059FB4A64B52
keywords:
- Elemento de prazo Agendador de Tarefas
topic_type:
- apiref
api_name:
- Deadline
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e12524971e8b713d4d17817a8a7c7602017bd68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644482"
---
# <a name="deadline-element"></a><span data-ttu-id="a78ae-104">Elemento prazo</span><span class="sxs-lookup"><span data-stu-id="a78ae-104">Deadline Element</span></span>

<span data-ttu-id="a78ae-105">Especifica quando o Agendador de tarefas deve iniciar a tarefa durante a manutenção automática de emergência, se ela não for concluída durante a manutenção automática regular.</span><span class="sxs-lookup"><span data-stu-id="a78ae-105">Specifies when the Task scheduler must to start the task during emergency Automatic maintenance, if it failed to complete during regular Automatic maintenance.</span></span>

<span data-ttu-id="a78ae-106">O formato dessa cadeia de caracteres é *PnYnMnDTnHnMnS*, em que *NY* é o número de anos, nm é o número de meses, *ND* é o número de dias, *T* é o separador de data/hora, *NH* é o número de horas, o *nm* é o número de minutos e o *ns* é o número de segundos (por exemplo, "PT5M" especifica 5 minutos e "P1M4DT2H5M" especifica um mês, quatro dias, duas horas e cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="a78ae-106">The format for this string is *PnYnMnDTnHnMnS*, where *nY* is the number of years, nM is the number of months, *nD* is the number of days, *T* is the date/time separator, *nH* is the number of hours, *nM* is the number of minutes, and *nS* is the number of seconds (for example, "PT5M" specifies 5 minutes and "P1M4DT2H5M" specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="a78ae-107">O valor mínimo é um minuto.</span><span class="sxs-lookup"><span data-stu-id="a78ae-107">The minimum value is one minute.</span></span> <span data-ttu-id="a78ae-108">Para obter mais informações sobre o tipo de duração, consulte [esquema XML parte 2: tipos de dados segunda edição](https://www.w3.org/TR/xmlschema-2/#duration).</span><span class="sxs-lookup"><span data-stu-id="a78ae-108">For more information about the duration type, see [XML Schema Part 2: Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration).</span></span> <span data-ttu-id="a78ae-109">Prazo mínimo que uma tarefa pode usar é 1 dia.</span><span class="sxs-lookup"><span data-stu-id="a78ae-109">Minimum Deadline a task can use is 1 day.</span></span> <span data-ttu-id="a78ae-110">O valor do elemento **prazo** deve ser maior que o valor do elemento [**period**](taskschedulerschema-period-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a78ae-110">The value of the **Deadline** element should be greater than the value of the [**Period**](taskschedulerschema-period-element.md) element.</span></span> <span data-ttu-id="a78ae-111">Se o prazo final não for especificado, a tarefa não será iniciada durante a manutenção automática de emergência.</span><span class="sxs-lookup"><span data-stu-id="a78ae-111">If the deadline is not specified the task will not be started during emergency Automatic maintenance.</span></span>

``` syntax
<xs:element name="Deadline"
    maxOccurs="1"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="P1D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="a78ae-112">O elemento **prazo** é definido pelo tipo complexo [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a78ae-112">The **Deadline** element is defined by the [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a78ae-113">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="a78ae-113">Parent element</span></span>



| <span data-ttu-id="a78ae-114">Elemento</span><span class="sxs-lookup"><span data-stu-id="a78ae-114">Element</span></span>                                                                                                                          | <span data-ttu-id="a78ae-115">Derivado de</span><span class="sxs-lookup"><span data-stu-id="a78ae-115">Derived from</span></span>                                                                               | <span data-ttu-id="a78ae-116">Description</span><span class="sxs-lookup"><span data-stu-id="a78ae-116">Description</span></span>                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a78ae-117">**MaintenanceSettings (maintenanceSettingsType)**</span><span class="sxs-lookup"><span data-stu-id="a78ae-117">**MaintenanceSettings (maintenanceSettingsType)**</span></span>](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [<span data-ttu-id="a78ae-118">**maintenanceSettingsType**</span><span class="sxs-lookup"><span data-stu-id="a78ae-118">**maintenanceSettingsType**</span></span>](taskschedulerschema-maintenancesettingstype-complextype.md) | <span data-ttu-id="a78ae-119">Especifica as configurações de tarefa que o Agendador de tarefas usará para iniciar a tarefa durante a manutenção automática.</span><span class="sxs-lookup"><span data-stu-id="a78ae-119">Specifies the task settings the Task scheduler will use to start task during Automatic maintenance.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a78ae-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="a78ae-120">Remarks</span></span>

<span data-ttu-id="a78ae-121">Para a programação C++, essa configuração ociosa é especificada usando a propriedade [**IMaintenanceSettings::D Ora**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_deadline) .</span><span class="sxs-lookup"><span data-stu-id="a78ae-121">For C++ programming, this idle setting is specified using the [**IMaintenanceSettings::Deadline**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_deadline) property.</span></span>

## <a name="examples"></a><span data-ttu-id="a78ae-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a78ae-122">Examples</span></span>

<span data-ttu-id="a78ae-123">O XML a seguir define um calendário de meses que executa a tarefa em março.</span><span class="sxs-lookup"><span data-stu-id="a78ae-123">The following XML defines a months calendar that runs the task in March.</span></span>


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
    <Deadline>P15D</Deadline>
</MaintenanceSettings>
```



## <a name="requirements"></a><span data-ttu-id="a78ae-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a78ae-124">Requirements</span></span>



| <span data-ttu-id="a78ae-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a78ae-125">Requirement</span></span> | <span data-ttu-id="a78ae-126">Valor</span><span class="sxs-lookup"><span data-stu-id="a78ae-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a78ae-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a78ae-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a78ae-128">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a78ae-128">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="a78ae-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a78ae-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a78ae-130">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a78ae-130">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a78ae-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a78ae-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a78ae-132">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="a78ae-132">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="a78ae-133">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="a78ae-133">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





