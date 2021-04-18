---
title: Elemento exclusivo
description: Indica se o Agendador de tarefas deve iniciar a tarefa durante a manutenção automática no modo exclusivo.
ms.assetid: F690FD8F-BCCB-456D-92E3-25A262D6DCF1
keywords:
- Elemento exclusivo Agendador de Tarefas
topic_type:
- apiref
api_name:
- Exclusive
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e0cd7cf5b2a5ce3aa68f92834aa45563000945d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760139"
---
# <a name="exclusive-element"></a><span data-ttu-id="48eb7-104">Elemento exclusivo</span><span class="sxs-lookup"><span data-stu-id="48eb7-104">Exclusive Element</span></span>

<span data-ttu-id="48eb7-105">Indica se o Agendador de tarefas deve iniciar a tarefa durante a manutenção automática no modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="48eb7-105">Indicates whether the Task scheduler must start the task during the Automatic maintenance in exclusive mode.</span></span>

<span data-ttu-id="48eb7-106">O exclusividade é garantido apenas entre outras tarefas de manutenção e não concede nenhuma prioridade de ordenação da tarefa.</span><span class="sxs-lookup"><span data-stu-id="48eb7-106">The exclusivity is guaranteed only between other maintenance tasks and doesn't grant any ordering priority of the task.</span></span> <span data-ttu-id="48eb7-107">Se exclusividade não for especificado, a tarefa será iniciada em paralelo com outras tarefas de manutenção.</span><span class="sxs-lookup"><span data-stu-id="48eb7-107">If exclusivity is not specified, the task is started in parallel with other maintenance tasks.</span></span>

``` syntax
<xs:element name="Exclusive"
    type="xsd:boolean"
    maxOccurs="1"
    minOccurs="0"
 />
```

<span data-ttu-id="48eb7-108">O elemento **exclusivo** é definido pelo tipo complexo [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="48eb7-108">The **Exclusive** element is defined by the [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="48eb7-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="48eb7-109">Parent element</span></span>



| <span data-ttu-id="48eb7-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="48eb7-110">Element</span></span>                                                                                                                          | <span data-ttu-id="48eb7-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="48eb7-111">Derived from</span></span>                                                                               | <span data-ttu-id="48eb7-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="48eb7-112">Description</span></span>                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48eb7-113">**MaintenanceSettings (maintenanceSettingsType)**</span><span class="sxs-lookup"><span data-stu-id="48eb7-113">**MaintenanceSettings (maintenanceSettingsType)**</span></span>](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [<span data-ttu-id="48eb7-114">**maintenanceSettingsType**</span><span class="sxs-lookup"><span data-stu-id="48eb7-114">**maintenanceSettingsType**</span></span>](taskschedulerschema-maintenancesettingstype-complextype.md) | <span data-ttu-id="48eb7-115">Especifica as configurações de tarefa que o Agendador de tarefas usará para iniciar a tarefa durante a manutenção automática.</span><span class="sxs-lookup"><span data-stu-id="48eb7-115">Specifies the task settings the Task scheduler will use to start task during Automatic maintenance.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="48eb7-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="48eb7-116">Remarks</span></span>

<span data-ttu-id="48eb7-117">Para a programação C++, essa configuração ociosa é especificada usando a propriedade [**IMaintenanceSettings:: Exclusive**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_exclusive) .</span><span class="sxs-lookup"><span data-stu-id="48eb7-117">For C++ programming, this idle setting is specified using the [**IMaintenanceSettings::Exclusive**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_exclusive) property.</span></span>

## <a name="examples"></a><span data-ttu-id="48eb7-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="48eb7-118">Examples</span></span>

<span data-ttu-id="48eb7-119">O XML a seguir define a tarefa de manutenção com o requisito de prazo definido como 15 dias.</span><span class="sxs-lookup"><span data-stu-id="48eb7-119">The following XML defines maintenance task with deadline requirement set to 15 days.</span></span>


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
    <Deadline>P15D</Deadline>
    <Exclusive>true</Exclusive>
</MaintenanceSettings>
```



## <a name="requirements"></a><span data-ttu-id="48eb7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48eb7-120">Requirements</span></span>



| <span data-ttu-id="48eb7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="48eb7-121">Requirement</span></span> | <span data-ttu-id="48eb7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="48eb7-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="48eb7-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48eb7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="48eb7-124">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="48eb7-124">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="48eb7-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48eb7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="48eb7-126">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="48eb7-126">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="48eb7-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="48eb7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48eb7-128">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="48eb7-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="48eb7-129">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="48eb7-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





