---
title: Elemento UseUnifiedSchedulingEngine (settingstype)
description: Especifica que o mecanismo de agendamento unificado será usado para executar essa tarefa.
ms.assetid: 93436f14-1caf-4ec8-bf74-a198b7dcb27c
keywords:
- Agendador de Tarefas do elemento UseUnifiedSchedulingEngine
topic_type:
- apiref
api_name:
- UseUnifiedSchedulingEngine
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a00798a46df3dfbb351dd8705b264192c38daff6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009152"
---
# <a name="useunifiedschedulingengine-settingstype-element"></a><span data-ttu-id="69d11-104">Elemento UseUnifiedSchedulingEngine (settingstype)</span><span class="sxs-lookup"><span data-stu-id="69d11-104">UseUnifiedSchedulingEngine (settingsType) Element</span></span>

<span data-ttu-id="69d11-105">Especifica que o mecanismo de agendamento unificado será usado para executar essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="69d11-105">Specifies that the Unified Scheduling Engine will be used to run this task.</span></span>

``` syntax
<xs:element name="UseUnifiedSchedulingEngine"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="69d11-106">O elemento **UseUnifiedSchedulingEngine** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="69d11-106">The **UseUnifiedSchedulingEngine** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="69d11-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="69d11-107">Parent element</span></span>



| <span data-ttu-id="69d11-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="69d11-108">Element</span></span>                                                           | <span data-ttu-id="69d11-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="69d11-109">Derived from</span></span>                                                         | <span data-ttu-id="69d11-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="69d11-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="69d11-111">**Configurações**</span><span class="sxs-lookup"><span data-stu-id="69d11-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="69d11-112">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="69d11-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="69d11-113">Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="69d11-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="69d11-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="69d11-114">Remarks</span></span>

<span data-ttu-id="69d11-115">A configuração padrão para esse elemento é false.</span><span class="sxs-lookup"><span data-stu-id="69d11-115">The default setting for this element is False.</span></span>

<span data-ttu-id="69d11-116">Para desenvolvimento em C++, essas informações são acessadas por meio da propriedade [**ITaskSettings2:: UseUnifiedSchedulingEngine**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_useunifiedschedulingengine) .</span><span class="sxs-lookup"><span data-stu-id="69d11-116">For C++ development, this information is accessed through the [**ITaskSettings2::UseUnifiedSchedulingEngine**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_useunifiedschedulingengine) property.</span></span>

## <a name="examples"></a><span data-ttu-id="69d11-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="69d11-117">Examples</span></span>

<span data-ttu-id="69d11-118">O XML a seguir define um elemento Settings que especifica que o mecanismo de agendamento unificado será usado para executar essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="69d11-118">The following XML defines a settings element that specifies that the Unified Scheduling Engine will be used to run this task.</span></span>


```XML
<Settings>
    <UseUnifiedSchedulingEngine>true</UseUnifiedSchedulingEngine>
</Settings>
        
```



## <a name="requirements"></a><span data-ttu-id="69d11-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69d11-119">Requirements</span></span>



| <span data-ttu-id="69d11-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="69d11-120">Requirement</span></span> | <span data-ttu-id="69d11-121">Valor</span><span class="sxs-lookup"><span data-stu-id="69d11-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="69d11-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69d11-122">Minimum supported client</span></span><br/> | <span data-ttu-id="69d11-123">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="69d11-123">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="69d11-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69d11-124">Minimum supported server</span></span><br/> | <span data-ttu-id="69d11-125">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="69d11-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="69d11-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="69d11-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69d11-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="69d11-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





