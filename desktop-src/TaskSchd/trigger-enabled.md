---
title: Propriedade Trigger. Enabled
description: Para scripts, Obtém ou define um valor booliano que indica se o gatilho está habilitado.
ms.assetid: 8fb5a0cc-ddd4-430d-9593-95a4cb311f18
keywords:
- Propriedade habilitada Agendador de Tarefas
- Propriedade habilitada Agendador de Tarefas, objeto de gatilho
- Objeto disparador Agendador de Tarefas, Propriedade Enabled
topic_type:
- apiref
api_name:
- Trigger.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411bc36dcf03933e2b4cee2f575aaec3b8133846
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918209"
---
# <a name="triggerenabled-property"></a><span data-ttu-id="c3f05-106">Propriedade Trigger. Enabled</span><span class="sxs-lookup"><span data-stu-id="c3f05-106">Trigger.Enabled property</span></span>

<span data-ttu-id="c3f05-107">Para scripts, Obtém ou define um valor booliano que indica se o gatilho está habilitado.</span><span class="sxs-lookup"><span data-stu-id="c3f05-107">For scripting, gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3f05-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3f05-108">Syntax</span></span>


```VB
Trigger.Enabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="c3f05-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c3f05-109">Property value</span></span>

<span data-ttu-id="c3f05-110">True se o gatilho estiver habilitado; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="c3f05-110">True if the trigger is enabled; otherwise, false.</span></span> <span data-ttu-id="c3f05-111">O padrão é true.</span><span class="sxs-lookup"><span data-stu-id="c3f05-111">The default is true.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3f05-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3f05-112">Remarks</span></span>

<span data-ttu-id="c3f05-113">Ao ler ou gravar XML para uma tarefa, a propriedade Enabled é especificada usando o elemento [**Enabled**](taskschedulerschema-enabled-triggerbasetype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="c3f05-113">When reading or writing XML for a task, the enabled property is specified using the [**Enabled**](taskschedulerschema-enabled-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3f05-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3f05-114">Requirements</span></span>



| <span data-ttu-id="c3f05-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3f05-115">Requirement</span></span> | <span data-ttu-id="c3f05-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c3f05-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3f05-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3f05-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c3f05-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c3f05-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c3f05-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3f05-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c3f05-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c3f05-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c3f05-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c3f05-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="c3f05-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c3f05-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c3f05-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c3f05-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3f05-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3f05-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3f05-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3f05-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3f05-126">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="c3f05-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





