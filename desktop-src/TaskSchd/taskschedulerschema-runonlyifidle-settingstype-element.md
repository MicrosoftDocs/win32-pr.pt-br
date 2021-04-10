---
title: Elemento RunOnlyIfIdle (settingstype)
description: Especifica que a tarefa é executada somente quando o computador está em um estado ocioso.
ms.assetid: 2ef3dd19-4d5c-4399-89b8-d737be4ef85e
keywords:
- Agendador de Tarefas do elemento RunOnlyIfIdle
topic_type:
- apiref
api_name:
- RunOnlyIfIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c57663d763926d68e5a552ebaf66edff2172e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009629"
---
# <a name="runonlyifidle-settingstype-element"></a><span data-ttu-id="f5ec2-104">Elemento RunOnlyIfIdle (settingstype)</span><span class="sxs-lookup"><span data-stu-id="f5ec2-104">RunOnlyIfIdle (settingsType) Element</span></span>

<span data-ttu-id="f5ec2-105">Especifica que a tarefa é executada somente quando o computador está em um estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="f5ec2-105">Specifies that the task is run only when the computer is in an idle state.</span></span>

``` syntax
<xs:element name="RunOnlyIfIdle"
    type="boolean"
 />
```

<span data-ttu-id="f5ec2-106">O elemento **RunOnlyIfIdle** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f5ec2-106">The **RunOnlyIfIdle** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f5ec2-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="f5ec2-107">Parent element</span></span>



| <span data-ttu-id="f5ec2-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="f5ec2-108">Element</span></span>                                                           | <span data-ttu-id="f5ec2-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="f5ec2-109">Derived from</span></span>                                                         | <span data-ttu-id="f5ec2-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5ec2-110">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="f5ec2-111">**Configurações**</span><span class="sxs-lookup"><span data-stu-id="f5ec2-111">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="f5ec2-112">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="f5ec2-112">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="f5ec2-113">Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="f5ec2-113">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f5ec2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5ec2-114">Remarks</span></span>

<span data-ttu-id="f5ec2-115">Para desenvolvimento em C++, consulte a [**Propriedade RunOnlyIfIdle de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifidle).</span><span class="sxs-lookup"><span data-stu-id="f5ec2-115">For C++ development, see [**RunOnlyIfIdle Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifidle).</span></span>

<span data-ttu-id="f5ec2-116">Para desenvolvimento de script, consulte [**TaskSettings. RunOnlyIfIdle**](tasksettings-runonlyifidle.md).</span><span class="sxs-lookup"><span data-stu-id="f5ec2-116">For script development, see [**TaskSettings.RunOnlyIfIdle**](tasksettings-runonlyifidle.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5ec2-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5ec2-117">Requirements</span></span>



| <span data-ttu-id="f5ec2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5ec2-118">Requirement</span></span> | <span data-ttu-id="f5ec2-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f5ec2-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f5ec2-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5ec2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f5ec2-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f5ec2-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f5ec2-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5ec2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f5ec2-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f5ec2-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f5ec2-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5ec2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5ec2-125">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="f5ec2-125">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f5ec2-126">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="f5ec2-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





