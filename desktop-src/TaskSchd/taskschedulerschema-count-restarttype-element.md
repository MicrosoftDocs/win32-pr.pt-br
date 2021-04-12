---
title: Elemento Count (restartype)
description: Especifica o número de vezes que o Agendador de Tarefas tentará reiniciar a tarefa.
ms.assetid: 67466c14-c9dd-49c8-a6ed-df7531fc63b8
keywords:
- Agendador de Tarefas de elemento de contagem
topic_type:
- apiref
api_name:
- Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 655f636b725e48749540d67710afa57b3c45c89c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454897"
---
# <a name="count-restarttype-element"></a><span data-ttu-id="91e05-104">Elemento Count (restartype)</span><span class="sxs-lookup"><span data-stu-id="91e05-104">Count (restartType) Element</span></span>

<span data-ttu-id="91e05-105">Especifica o número de vezes que o Agendador de Tarefas tentará reiniciar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="91e05-105">Specifies the number of times that the Task Scheduler will attempt to restart the task.</span></span>

``` syntax
<xs:element name="Count">
    <xs:simpleType>
        <xs:restriction
            base="unsignedByte"
        >
            <xs:minInclusive
                value="1"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="91e05-106">O elemento é definido pelo tipo complexo [**Restart**](taskschedulerschema-restarttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="91e05-106">The element is defined by the [**restartType**](taskschedulerschema-restarttype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="91e05-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="91e05-107">Parent element</span></span>



| <span data-ttu-id="91e05-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="91e05-108">Element</span></span>                                                                               | <span data-ttu-id="91e05-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="91e05-109">Derived from</span></span>                                                       | <span data-ttu-id="91e05-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="91e05-110">Description</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="91e05-111">**RestartOnFailure**</span><span class="sxs-lookup"><span data-stu-id="91e05-111">**RestartOnFailure**</span></span>](taskschedulerschema-restartonfailure-settingstype-element.md) | [<span data-ttu-id="91e05-112">**Restart**</span><span class="sxs-lookup"><span data-stu-id="91e05-112">**restartType**</span></span>](taskschedulerschema-restarttype-complextype.md) | <span data-ttu-id="91e05-113">Especifica que o Agendador de Tarefas tentará reiniciar a tarefa se a tarefa falhar por algum motivo.</span><span class="sxs-lookup"><span data-stu-id="91e05-113">Specifies that the Task Scheduler will attempt to restart the task if the task fails for any reason.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="91e05-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="91e05-114">Remarks</span></span>

<span data-ttu-id="91e05-115">Se esse elemento for especificado, o elemento [**Interval**](taskschedulerschema-interval-restarttype-element.md) também deverá ser especificado para informar ao agendador de tarefas por quanto tempo tentar reiniciar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="91e05-115">If this element is specified, the [**Interval**](taskschedulerschema-interval-restarttype-element.md) element must also be specified to tell the Task Scheduler how long to attempt to restart the task.</span></span>

<span data-ttu-id="91e05-116">Para desenvolvimento em C++, consulte a [**Propriedade RestartCount de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount).</span><span class="sxs-lookup"><span data-stu-id="91e05-116">For C++ development, see [**RestartCount Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount).</span></span>

<span data-ttu-id="91e05-117">Para desenvolvimento de script, consulte [**TaskSettings. RestartCount**](tasksettings-restartcount.md).</span><span class="sxs-lookup"><span data-stu-id="91e05-117">For script development, see [**TaskSettings.RestartCount**](tasksettings-restartcount.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="91e05-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91e05-118">Requirements</span></span>



| <span data-ttu-id="91e05-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="91e05-119">Requirement</span></span> | <span data-ttu-id="91e05-120">Valor</span><span class="sxs-lookup"><span data-stu-id="91e05-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="91e05-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91e05-121">Minimum supported client</span></span><br/> | <span data-ttu-id="91e05-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="91e05-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="91e05-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91e05-123">Minimum supported server</span></span><br/> | <span data-ttu-id="91e05-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="91e05-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="91e05-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="91e05-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91e05-126">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="91e05-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





