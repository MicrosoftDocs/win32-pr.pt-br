---
title: Propriedade EventTrigger. Subscription
description: Para scripts, Obtém ou define uma cadeia de caracteres de consulta que identifica o evento que dispara o gatilho.
ms.assetid: 31d32426-3dd7-41f9-89cc-b13767871b74
keywords:
- Agendador de Tarefas de propriedade de assinatura
- Propriedade de assinatura Agendador de Tarefas, objeto EventTrigger
- Agendador de Tarefas de objeto EventTrigger, propriedade de assinatura
topic_type:
- apiref
api_name:
- EventTrigger.Subscription
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68ad05576e248d3ad6c2551a8654a9198ca3c0f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810450"
---
# <a name="eventtriggersubscription-property"></a><span data-ttu-id="7b5de-106">Propriedade EventTrigger. Subscription</span><span class="sxs-lookup"><span data-stu-id="7b5de-106">EventTrigger.Subscription property</span></span>

<span data-ttu-id="7b5de-107">Para scripts, Obtém ou define uma cadeia de caracteres de consulta que identifica o evento que dispara o gatilho.</span><span class="sxs-lookup"><span data-stu-id="7b5de-107">For scripting, gets or sets a query string that identifies the event that fires the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b5de-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b5de-108">Syntax</span></span>


```VB
EventTrigger.Subscription As String
```



## <a name="property-value"></a><span data-ttu-id="7b5de-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7b5de-109">Property value</span></span>

<span data-ttu-id="7b5de-110">Uma cadeia de caracteres de consulta que identifica o evento que dispara o gatilho.</span><span class="sxs-lookup"><span data-stu-id="7b5de-110">A query string that identifies the event that fires the trigger.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b5de-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b5de-111">Remarks</span></span>

<span data-ttu-id="7b5de-112">Ao ler ou gravar seu próprio XML para uma tarefa, a assinatura de evento é especificada usando o elemento [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="7b5de-112">When reading or writing your own XML for a task, the event subscription is specified using the [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="7b5de-113">Para obter mais informações sobre como gravar uma cadeia de caracteres de consulta para determinados eventos, consulte [seleção de eventos](/previous-versions//aa385231(v=vs.85)) e [assinatura de eventos](../wes/subscribing-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="7b5de-113">For more information about writing a query string for certain events, see [Event Selection](/previous-versions//aa385231(v=vs.85)) and [Subscribing to Events](../wes/subscribing-to-events.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7b5de-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7b5de-114">Examples</span></span>

<span data-ttu-id="7b5de-115">A cadeia de caracteres de consulta a seguir define uma assinatura para todos os eventos de nível 2 no canal do sistema:</span><span class="sxs-lookup"><span data-stu-id="7b5de-115">The following query string defines a subscription to all level 2 events in the System channel:</span></span>


```XML
"<QueryList>
    <Query Id='1'>
        <Select Path='System'>*[System/Level=2]</Select>
    </Query>
</QueryList>" 
```



## <a name="requirements"></a><span data-ttu-id="7b5de-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b5de-116">Requirements</span></span>



| <span data-ttu-id="7b5de-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b5de-117">Requirement</span></span> | <span data-ttu-id="7b5de-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7b5de-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b5de-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b5de-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7b5de-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7b5de-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7b5de-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b5de-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7b5de-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7b5de-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7b5de-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7b5de-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="7b5de-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7b5de-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7b5de-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7b5de-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b5de-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b5de-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b5de-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b5de-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b5de-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="7b5de-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="7b5de-129">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="7b5de-129">**EventTrigger**</span></span>](eventtrigger.md)
</dt> </dl>

 

