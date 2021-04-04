---
title: Elemento SessionStateChangeTrigger (Trigger)
description: Especifica um gatilho que inicia uma tarefa quando uma sessão de Terminal Server muda de estado.
ms.assetid: 38b0da3c-205f-48c5-83e6-ff7c432c02b9
keywords:
- Agendador de Tarefas do elemento SessionStateChangeTrigger
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d21847a929e79e2da53b1e66a23aec0c2f1c630f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644963"
---
# <a name="sessionstatechangetrigger-triggergroup-element"></a><span data-ttu-id="efb92-104">Elemento SessionStateChangeTrigger (Trigger)</span><span class="sxs-lookup"><span data-stu-id="efb92-104">SessionStateChangeTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="efb92-105">Especifica um gatilho que inicia uma tarefa quando uma sessão de Terminal Server muda de estado.</span><span class="sxs-lookup"><span data-stu-id="efb92-105">Specifies a trigger that starts a task when a Terminal Server session changes state.</span></span>

``` syntax
<xs:element name="SessionStateChangeTrigger"
    type="sessionStateChangeTriggerType"
 />
```

<span data-ttu-id="efb92-106">O elemento **SessionStateChangeTrigger** é definido pelo [**disparador**](taskschedulerschema-triggergroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="efb92-106">The **SessionStateChangeTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="efb92-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="efb92-107">Parent element</span></span>



| <span data-ttu-id="efb92-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="efb92-108">Element</span></span>                                                           | <span data-ttu-id="efb92-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="efb92-109">Derived from</span></span>                                                         | <span data-ttu-id="efb92-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="efb92-110">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="efb92-111">**Gatilhos**</span><span class="sxs-lookup"><span data-stu-id="efb92-111">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="efb92-112">**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="efb92-112">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="efb92-113">Especifica os gatilhos que iniciam a tarefa.</span><span class="sxs-lookup"><span data-stu-id="efb92-113">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="efb92-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="efb92-114">Child elements</span></span>



| <span data-ttu-id="efb92-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="efb92-115">Element</span></span>                                                                                      | <span data-ttu-id="efb92-116">Type</span><span class="sxs-lookup"><span data-stu-id="efb92-116">Type</span></span>                                                                                    | <span data-ttu-id="efb92-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="efb92-117">Description</span></span>                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="efb92-118">**Retardo**</span><span class="sxs-lookup"><span data-stu-id="efb92-118">**Delay**</span></span>](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | <span data-ttu-id="efb92-119">duration</span><span class="sxs-lookup"><span data-stu-id="efb92-119">duration</span></span>                                                                                | <span data-ttu-id="efb92-120">Especifica um valor que indica o comprimento do atraso antes que uma tarefa seja iniciada quando uma alteração de estado de sessão de Terminal Server for detectada.</span><span class="sxs-lookup"><span data-stu-id="efb92-120">Specifies a value that indicates the length of the delay before a task is started when a Terminal Server session state change is detected.</span></span><br/> |
| [<span data-ttu-id="efb92-121">**StateChange**</span><span class="sxs-lookup"><span data-stu-id="efb92-121">**StateChange**</span></span>](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [<span data-ttu-id="efb92-122">**sessionStateChangeType**</span><span class="sxs-lookup"><span data-stu-id="efb92-122">**sessionStateChangeType**</span></span>](taskschedulerschema-sessionstatechangetype-simpletype.md) | <span data-ttu-id="efb92-123">Especifica o tipo de Terminal Server alteração de sessão que dispararia uma inicialização de tarefa.</span><span class="sxs-lookup"><span data-stu-id="efb92-123">Specifies the kind of Terminal Server session change that would trigger a task launch.</span></span><br/>                                                     |
| [<span data-ttu-id="efb92-124">**ID**</span><span class="sxs-lookup"><span data-stu-id="efb92-124">**UserId**</span></span>](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [<span data-ttu-id="efb92-125">**não vazio**</span><span class="sxs-lookup"><span data-stu-id="efb92-125">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)                 | <span data-ttu-id="efb92-126">Especifica o usuário para a sessão de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="efb92-126">Specifies the user for the Terminal Server session.</span></span> <span data-ttu-id="efb92-127">Quando uma alteração de estado de sessão é detectada para esse usuário, uma tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="efb92-127">When a session state change is detected for this user, a task is started.</span></span><br/>              |



## <a name="remarks"></a><span data-ttu-id="efb92-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="efb92-128">Remarks</span></span>

<span data-ttu-id="efb92-129">Para o desenvolvimento de scripts, um gatilho de alteração de estado de sessão é especificado usando o objeto [**SessionStateChangeTrigger**](sessionstatechangetrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="efb92-129">For scripting development, a session state change trigger is specified using the [**SessionStateChangeTrigger**](sessionstatechangetrigger.md) object.</span></span>

<span data-ttu-id="efb92-130">Para desenvolvimento em C++, um gatilho de alteração de estado de sessão é especificado usando a interface [**ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger) .</span><span class="sxs-lookup"><span data-stu-id="efb92-130">For C++ development, a session state change trigger is specified using the [**ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="efb92-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efb92-131">Requirements</span></span>



| <span data-ttu-id="efb92-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="efb92-132">Requirement</span></span> | <span data-ttu-id="efb92-133">Valor</span><span class="sxs-lookup"><span data-stu-id="efb92-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="efb92-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="efb92-134">Minimum supported client</span></span><br/> | <span data-ttu-id="efb92-135">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="efb92-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="efb92-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="efb92-136">Minimum supported server</span></span><br/> | <span data-ttu-id="efb92-137">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="efb92-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





