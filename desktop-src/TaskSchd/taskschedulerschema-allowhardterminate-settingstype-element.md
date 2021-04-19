---
title: Elemento AllowHardTerminate (settingstype)
description: Especifica que a tarefa pode ser encerrada usando TerminateProcess.
ms.assetid: 093a3cc6-d3e1-48e3-bc9e-0b15df2a54de
keywords:
- Elemento AllowHardTerminate (settingstype) Agendador de Tarefas
- Agendador de Tarefas do elemento AllowHardTerminate
topic_type:
- apiref
api_name:
- AllowHardTerminate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eba987b42206121b91b3c096f298eac32cf52b38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105800011"
---
# <a name="allowhardterminate-settingstype-element"></a><span data-ttu-id="1bc09-105">Elemento AllowHardTerminate (settingstype)</span><span class="sxs-lookup"><span data-stu-id="1bc09-105">AllowHardTerminate (settingsType) Element</span></span>

<span data-ttu-id="1bc09-106">Especifica que a tarefa pode ser encerrada usando TerminateProcess.</span><span class="sxs-lookup"><span data-stu-id="1bc09-106">Specifies that the task may be terminated using TerminateProcess.</span></span>

``` syntax
<xs:element name="AllowHardTerminate"
    type="boolean"
    default="true"
    minOccurs="0"
 />
```

<span data-ttu-id="1bc09-107">O elemento **AllowHardTerminate** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1bc09-107">The **AllowHardTerminate** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1bc09-108">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="1bc09-108">Parent element</span></span>



| <span data-ttu-id="1bc09-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="1bc09-109">Element</span></span>                                                           | <span data-ttu-id="1bc09-110">Derivado de</span><span class="sxs-lookup"><span data-stu-id="1bc09-110">Derived from</span></span>                                                 | <span data-ttu-id="1bc09-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="1bc09-111">Description</span></span>                                                                        |
|-------------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="1bc09-112">**Configurações**</span><span class="sxs-lookup"><span data-stu-id="1bc09-112">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="1bc09-113">**taskType**</span><span class="sxs-lookup"><span data-stu-id="1bc09-113">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="1bc09-114">Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="1bc09-114">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1bc09-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="1bc09-115">Remarks</span></span>

<span data-ttu-id="1bc09-116">Para desenvolvimento em C++, consulte a [**Propriedade AllowHardTerminate de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowhardterminate).</span><span class="sxs-lookup"><span data-stu-id="1bc09-116">For C++ development, see the [**AllowHardTerminate property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowhardterminate).</span></span>

<span data-ttu-id="1bc09-117">Para desenvolvimento de script, consulte [**TaskSettings. AllowHardTerminate**](tasksettings-allowhardterminate.md).</span><span class="sxs-lookup"><span data-stu-id="1bc09-117">For script development, see [**TaskSettings.AllowHardTerminate**](tasksettings-allowhardterminate.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1bc09-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1bc09-118">Examples</span></span>

<span data-ttu-id="1bc09-119">Para obter um exemplo completo do XML para uma tarefa que permite um encerramento rígido, consulte [exemplo de gatilho de tempo (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="1bc09-119">For a complete example of the XML for a task that allows hard termination, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1bc09-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bc09-120">Requirements</span></span>



| <span data-ttu-id="1bc09-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bc09-121">Requirement</span></span> | <span data-ttu-id="1bc09-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1bc09-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1bc09-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bc09-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1bc09-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1bc09-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1bc09-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bc09-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1bc09-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1bc09-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1bc09-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="1bc09-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bc09-128">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="1bc09-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





