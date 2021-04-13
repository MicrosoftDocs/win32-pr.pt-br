---
title: Elemento period
description: Especifica com que frequência a tarefa precisa ser iniciada durante a manutenção automática.
ms.assetid: E4BE2466-3119-41F8-8238-4627C28B26E5
keywords:
- Agendador de Tarefas de elemento de período
topic_type:
- apiref
api_name:
- Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a507a9b0a8f97d1ae4e6c8df654a45d67b77767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455984"
---
# <a name="period-element"></a><span data-ttu-id="dcc65-104">Elemento period</span><span class="sxs-lookup"><span data-stu-id="dcc65-104">Period Element</span></span>

<span data-ttu-id="dcc65-105">Especifica com que frequência a tarefa precisa ser iniciada durante a manutenção automática.</span><span class="sxs-lookup"><span data-stu-id="dcc65-105">Specifies how often the task needs to be started during Automatic maintenance.</span></span>

<span data-ttu-id="dcc65-106">O formato dessa cadeia de caracteres é *PnYnMnDTnHnMnS*, em que *NY* é o número de anos, nm é o número de meses, *ND* é o número de dias, *T* é o separador de data/hora, *NH* é o número de horas, o *nm* é o número de minutos e o *ns* é o número de segundos (por exemplo, "PT5M" especifica 5 minutos e "P1M4DT2H5M" especifica um mês, quatro dias, duas horas e cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="dcc65-106">The format for this string is *PnYnMnDTnHnMnS*, where *nY* is the number of years, nM is the number of months, *nD* is the number of days, *T* is the date/time separator, *nH* is the number of hours, *nM* is the number of minutes, and *nS* is the number of seconds (for example, "PT5M" specifies 5 minutes and "P1M4DT2H5M" specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="dcc65-107">O valor mínimo é um minuto.</span><span class="sxs-lookup"><span data-stu-id="dcc65-107">The minimum value is one minute.</span></span> <span data-ttu-id="dcc65-108">Para obter mais informações sobre o tipo de duração, consulte [esquema XML parte 2: tipos de dados segunda edição](https://www.w3.org/TR/xmlschema-2/#duration).</span><span class="sxs-lookup"><span data-stu-id="dcc65-108">For more information about the duration type, see [XML Schema Part 2: Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration).</span></span>

``` syntax
<xs:element name="Period"
    maxOccurs="1"
    minOccurs="1"
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

<span data-ttu-id="dcc65-109">O elemento **period** é definido pelo tipo complexo [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="dcc65-109">The **Period** element is defined by the [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="dcc65-110">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="dcc65-110">Parent element</span></span>



| <span data-ttu-id="dcc65-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="dcc65-111">Element</span></span>                                                                                                                          | <span data-ttu-id="dcc65-112">Derivado de</span><span class="sxs-lookup"><span data-stu-id="dcc65-112">Derived from</span></span>                                                                               | <span data-ttu-id="dcc65-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="dcc65-113">Description</span></span>                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dcc65-114">**MaintenanceSettings (maintenanceSettingsType)**</span><span class="sxs-lookup"><span data-stu-id="dcc65-114">**MaintenanceSettings (maintenanceSettingsType)**</span></span>](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [<span data-ttu-id="dcc65-115">**maintenanceSettingsType**</span><span class="sxs-lookup"><span data-stu-id="dcc65-115">**maintenanceSettingsType**</span></span>](taskschedulerschema-maintenancesettingstype-complextype.md) | <span data-ttu-id="dcc65-116">Especifica as configurações de tarefa que o Agendador de tarefas usará para iniciar a tarefa durante a manutenção automática.</span><span class="sxs-lookup"><span data-stu-id="dcc65-116">Specifies the task settings the Task scheduler will use to start task during Automatic maintenance.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="dcc65-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="dcc65-117">Remarks</span></span>

<span data-ttu-id="dcc65-118">Para a programação C++, essa configuração ociosa é especificada usando a propriedade [**IMaintenanceSettings::P eriod**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_period) .</span><span class="sxs-lookup"><span data-stu-id="dcc65-118">For C++ programming, this idle setting is specified using the [**IMaintenanceSettings::Period**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_period) property.</span></span>

## <a name="examples"></a><span data-ttu-id="dcc65-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dcc65-119">Examples</span></span>

<span data-ttu-id="dcc65-120">O XML a seguir define a tarefa de manutenção com o requisito de periodicidade definido como 5 dias.</span><span class="sxs-lookup"><span data-stu-id="dcc65-120">The following XML defines maintenance task with periodicity requirement set to 5 days.</span></span>


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
</MaintenanceSettings>
```



## <a name="requirements"></a><span data-ttu-id="dcc65-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcc65-121">Requirements</span></span>



| <span data-ttu-id="dcc65-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcc65-122">Requirement</span></span> | <span data-ttu-id="dcc65-123">Valor</span><span class="sxs-lookup"><span data-stu-id="dcc65-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dcc65-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dcc65-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dcc65-125">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dcc65-125">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="dcc65-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dcc65-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dcc65-127">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dcc65-127">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dcc65-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="dcc65-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcc65-129">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="dcc65-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="dcc65-130">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="dcc65-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





