---
title: Elemento volátil
description: Indica se a tarefa é automaticamente desabilitada toda vez que o Windows é iniciado.
ms.assetid: E0298876-2A96-401D-B857-69758AF980E5
keywords:
- Elemento volátil Agendador de Tarefas
topic_type:
- apiref
api_name:
- Volatile
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca697bd0dff3a1fffd0b92a29d2fc88f1d4ed433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645103"
---
# <a name="volatile-element"></a><span data-ttu-id="b1e3f-104">Elemento volátil</span><span class="sxs-lookup"><span data-stu-id="b1e3f-104">Volatile Element</span></span>

<span data-ttu-id="b1e3f-105">Indica se a tarefa é automaticamente desabilitada toda vez que o Windows é iniciado.</span><span class="sxs-lookup"><span data-stu-id="b1e3f-105">Indicates whether the task is automatically disabled every time Windows starts.</span></span>

``` syntax
<xs:element name="Volatile"
    type="xsd:boolean"
    maxOccurs="1"
    minOccurs="0"
    default="false"
 />
```

<span data-ttu-id="b1e3f-106">O elemento **volátil** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="b1e3f-106">The **Volatile** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b1e3f-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="b1e3f-107">Parent element</span></span>



| <span data-ttu-id="b1e3f-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="b1e3f-108">Element</span></span>                                                           | <span data-ttu-id="b1e3f-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="b1e3f-109">Derived from</span></span> | <span data-ttu-id="b1e3f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1e3f-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1e3f-111">**Configurações**</span><span class="sxs-lookup"><span data-stu-id="b1e3f-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) |              | <span data-ttu-id="b1e3f-112">Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="b1e3f-112">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b1e3f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1e3f-113">Remarks</span></span>

<span data-ttu-id="b1e3f-114">Para a programação C++, essa configuração ociosa é especificada usando a propriedade [**ITaskSettings3:: volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile) .</span><span class="sxs-lookup"><span data-stu-id="b1e3f-114">For C++ programming, this idle setting is specified using the [**ITaskSettings3::Volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1e3f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1e3f-115">Requirements</span></span>



| <span data-ttu-id="b1e3f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1e3f-116">Requirement</span></span> | <span data-ttu-id="b1e3f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b1e3f-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b1e3f-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1e3f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b1e3f-119">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b1e3f-119">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="b1e3f-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1e3f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b1e3f-121">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b1e3f-121">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b1e3f-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1e3f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1e3f-123">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="b1e3f-123">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="b1e3f-124">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="b1e3f-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





