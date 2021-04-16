---
title: Elemento WakeToRun (settingstype)
description: Especifica que Agendador de Tarefas ativará o computador quando for hora de executar a tarefa.
ms.assetid: 5fb53016-5778-463d-bb32-3c1da2de6fc2
keywords:
- Agendador de Tarefas do elemento WakeToRun
topic_type:
- apiref
api_name:
- WakeToRun
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 23eeaa06073fa9259c1a48137cf3676baa402d39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757939"
---
# <a name="waketorun-settingstype-element"></a><span data-ttu-id="3937e-104">Elemento WakeToRun (settingstype)</span><span class="sxs-lookup"><span data-stu-id="3937e-104">WakeToRun (settingsType) Element</span></span>

<span data-ttu-id="3937e-105">Especifica que Agendador de Tarefas ativará o computador quando for hora de executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="3937e-105">Specifies that Task Scheduler will wake the computer when it is time to run the task.</span></span>

``` syntax
<xs:element name="WakeToRun"
    type="boolean"
 />
```

<span data-ttu-id="3937e-106">O elemento **WakeToRun** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="3937e-106">The **WakeToRun** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="3937e-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="3937e-107">Parent element</span></span>



| <span data-ttu-id="3937e-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="3937e-108">Element</span></span>                                                           | <span data-ttu-id="3937e-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="3937e-109">Derived from</span></span>                                                         | <span data-ttu-id="3937e-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="3937e-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="3937e-111">**Configurações**</span><span class="sxs-lookup"><span data-stu-id="3937e-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="3937e-112">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="3937e-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="3937e-113">Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="3937e-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3937e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3937e-114">Remarks</span></span>

<span data-ttu-id="3937e-115">Quando o serviço de Agendador de Tarefas ativa o computador para executar uma tarefa, a tela pode permanecer desativada, mesmo que o computador não esteja mais no modo de suspensão ou hibernação.</span><span class="sxs-lookup"><span data-stu-id="3937e-115">When the Task Scheduler service wakes the computer to run a task, the screen may remain off even though the computer is no longer in the sleep or hibernate mode.</span></span> <span data-ttu-id="3937e-116">A tela será ativada quando o Windows Vista detectar que um usuário voltou a usar o computador.</span><span class="sxs-lookup"><span data-stu-id="3937e-116">The screen will turn on when Windows Vista detects that a user has returned to use the computer.</span></span>

<span data-ttu-id="3937e-117">Para desenvolvimento em C++, consulte a [**Propriedade WakeToRun de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_waketorun).</span><span class="sxs-lookup"><span data-stu-id="3937e-117">For C++ development, see [**WakeToRun Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_waketorun).</span></span>

<span data-ttu-id="3937e-118">Para desenvolvimento de script, consulte [**TaskSettings. WakeToRun**](tasksettings-waketorun.md).</span><span class="sxs-lookup"><span data-stu-id="3937e-118">For script development, see [**TaskSettings.WakeToRun**](tasksettings-waketorun.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3937e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3937e-119">Requirements</span></span>



| <span data-ttu-id="3937e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3937e-120">Requirement</span></span> | <span data-ttu-id="3937e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="3937e-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3937e-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3937e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3937e-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3937e-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3937e-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3937e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3937e-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3937e-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3937e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="3937e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3937e-127">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="3937e-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="3937e-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="3937e-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





