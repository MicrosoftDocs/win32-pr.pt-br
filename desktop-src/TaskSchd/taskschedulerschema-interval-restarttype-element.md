---
title: Elemento Interval (restartype)
description: Especifica por quanto tempo o Agendador de Tarefas tentará reiniciar a tarefa.
ms.assetid: 00b8fcbb-5be8-4bf1-92a0-2afd2a50f8e1
keywords:
- Elemento Interval Agendador de Tarefas
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e731582364df23bdef800ab5d2cf15dd5c882ae
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734181"
---
# <a name="interval-restarttype-element"></a><span data-ttu-id="54a95-104">Elemento Interval (restartype)</span><span class="sxs-lookup"><span data-stu-id="54a95-104">Interval (restartType) Element</span></span>

<span data-ttu-id="54a95-105">Especifica por quanto tempo o Agendador de Tarefas tentará reiniciar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="54a95-105">Specifies how long the Task Scheduler will attempt to restart the task.</span></span> <span data-ttu-id="54a95-106">O formato dessa cadeia de caracteres é `P<days>DT<hours>H<minutes>M<seconds>S` (por exemplo, "PT5M" é de 5 minutos, "PT1H" é de 1 hora e "PT20M" é de 20 minutos).</span><span class="sxs-lookup"><span data-stu-id="54a95-106">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="54a95-107">O tempo máximo permitido é de 31 dias e o tempo mínimo permitido é de 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="54a95-107">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

``` syntax
<xs:element name="Interval">
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
            <xs:maxInclusive
                value="P31D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="54a95-108">O elemento é definido pelo tipo complexo [**Restart**](taskschedulerschema-restarttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="54a95-108">The element is defined by the [**restartType**](taskschedulerschema-restarttype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="54a95-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="54a95-109">Parent element</span></span>



| <span data-ttu-id="54a95-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="54a95-110">Element</span></span>                                                                               | <span data-ttu-id="54a95-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="54a95-111">Derived from</span></span>                                                       | <span data-ttu-id="54a95-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="54a95-112">Description</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="54a95-113">**RestartOnFailure**</span><span class="sxs-lookup"><span data-stu-id="54a95-113">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md) | [<span data-ttu-id="54a95-114">**Restart**</span><span class="sxs-lookup"><span data-stu-id="54a95-114">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md) | <span data-ttu-id="54a95-115">Especifica que o Agendador de Tarefas tentará reiniciar a tarefa se a tarefa falhar por algum motivo.</span><span class="sxs-lookup"><span data-stu-id="54a95-115">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="54a95-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="54a95-116">Remarks</span></span>

<span data-ttu-id="54a95-117">Se esse elemento for especificado, o elemento [**Count**](taskschedulerschema-count-restarttype-element.md) também deverá ser especificado para informar ao agendador de tarefas quantas vezes ele deve tentar reiniciar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="54a95-117">If this element is specified, the [**Count**](taskschedulerschema-count-restarttype-element.md) element must also be specified to tell the Task Scheduler how many times it should try to restart the task.</span></span>

<span data-ttu-id="54a95-118">Para desenvolvimento em C++, consulte a [**Propriedade RestartInterval de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval).</span><span class="sxs-lookup"><span data-stu-id="54a95-118">For C++ development, see [**RestartInterval Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval).</span></span>

<span data-ttu-id="54a95-119">Para desenvolvimento de script, consulte [**TaskSettings. RestartInterval**](tasksettings-restartinterval.md).</span><span class="sxs-lookup"><span data-stu-id="54a95-119">For script development, see [**TaskSettings.RestartInterval**](tasksettings-restartinterval.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="54a95-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54a95-120">Requirements</span></span>



| <span data-ttu-id="54a95-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="54a95-121">Requirement</span></span> | <span data-ttu-id="54a95-122">Valor</span><span class="sxs-lookup"><span data-stu-id="54a95-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="54a95-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54a95-123">Minimum supported client</span></span><br/> | <span data-ttu-id="54a95-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="54a95-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="54a95-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54a95-125">Minimum supported server</span></span><br/> | <span data-ttu-id="54a95-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="54a95-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="54a95-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="54a95-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54a95-128">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="54a95-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





