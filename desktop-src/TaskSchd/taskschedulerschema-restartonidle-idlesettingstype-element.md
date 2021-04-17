---
title: Elemento RestartOnIdle (idleSettingsType)
description: Especifica se a tarefa é reiniciada quando o computador percorre uma condição ociosa mais de uma vez.
ms.assetid: 7a7a388c-8dc9-4106-82c1-3435d9f89866
keywords:
- Agendador de Tarefas do elemento RestartOnIdle
topic_type:
- apiref
api_name:
- RestartOnIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec1d20798b7ceb6ad6ebe2c3a92896600e36eec1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760137"
---
# <a name="restartonidle-idlesettingstype-element"></a><span data-ttu-id="9c00c-104">Elemento RestartOnIdle (idleSettingsType)</span><span class="sxs-lookup"><span data-stu-id="9c00c-104">RestartOnIdle (idleSettingsType) Element</span></span>

<span data-ttu-id="9c00c-105">Especifica se a tarefa é reiniciada quando o computador percorre uma condição ociosa mais de uma vez.</span><span class="sxs-lookup"><span data-stu-id="9c00c-105">Specifies whether the task is restarted when the computer cycles into an idle condition more than once.</span></span>

``` syntax
<xs:element name="RestartOnIdle"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="9c00c-106">O elemento **RestartOnIdle** é definido pelo tipo complexo [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="9c00c-106">The **RestartOnIdle** element is defined by the [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="9c00c-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="9c00c-107">Parent element</span></span>



| <span data-ttu-id="9c00c-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="9c00c-108">Element</span></span>                                                                       | <span data-ttu-id="9c00c-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="9c00c-109">Derived from</span></span>                                                                 | <span data-ttu-id="9c00c-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="9c00c-110">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9c00c-111">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="9c00c-111">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md) | [<span data-ttu-id="9c00c-112">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="9c00c-112">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md) | <span data-ttu-id="9c00c-113">Especifica como a Agendador de Tarefas executa tarefas quando o computador está em um estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="9c00c-113">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9c00c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c00c-114">Remarks</span></span>

<span data-ttu-id="9c00c-115">Esse elemento será usado somente se o elemento [**TerminateOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) estiver definido como true.</span><span class="sxs-lookup"><span data-stu-id="9c00c-115">This element is used only if the [**TerminateOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) element is set to True.</span></span>

<span data-ttu-id="9c00c-116">Para o desenvolvimento de script, essas configurações de tarefa são especificadas usando a propriedade [**IdleSettings. RestartOnIdle**](idlesettings-restartonidle.md) .</span><span class="sxs-lookup"><span data-stu-id="9c00c-116">For script development, this task settings is specified using the [**IdleSettings.RestartOnIdle**](idlesettings-restartonidle.md) property.</span></span>

<span data-ttu-id="9c00c-117">Para desenvolvimento em C++, essas configurações de tarefa são especificadas usando a propriedade [**IIdleSettings:: RestartOnIdle**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) .</span><span class="sxs-lookup"><span data-stu-id="9c00c-117">For C++ development, this task settings is specified using the [**IIdleSettings::RestartOnIdle**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) property.</span></span>

## <a name="examples"></a><span data-ttu-id="9c00c-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9c00c-118">Examples</span></span>

<span data-ttu-id="9c00c-119">O XML a seguir define uma configuração ociosa que indica que a tarefa não deve ser reiniciada quando a condição ociosa ciclos.</span><span class="sxs-lookup"><span data-stu-id="9c00c-119">The following XML defines an idle setting that indicates that the task should not be restarted when the idle condition cycles.</span></span>


```XML
<IdleSettings>
     <TerminateOnIdleEnd>true</TerminateOnIdleEnd>
     <RestartOnIdle>true</RestartOnIdle>
</IdleSettings>
```



## <a name="requirements"></a><span data-ttu-id="9c00c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c00c-120">Requirements</span></span>



| <span data-ttu-id="9c00c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c00c-121">Requirement</span></span> | <span data-ttu-id="9c00c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9c00c-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9c00c-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c00c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9c00c-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9c00c-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9c00c-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c00c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9c00c-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9c00c-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9c00c-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c00c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c00c-128">Elementos do esquema de Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="9c00c-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="9c00c-129">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="9c00c-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





