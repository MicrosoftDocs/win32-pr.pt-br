---
title: Propriedade IdleSettings. StopOnIdleEnd
description: Para scripts, Obtém ou define um valor booliano que indica que o Agendador de Tarefas encerrará a tarefa se a condição de ociosidade terminar antes de a tarefa ser concluída.
ms.assetid: 5908bf6b-227a-4234-a741-82cf38163171
keywords:
- Agendador de Tarefas da propriedade StopOnIdleEnd
- Propriedade StopOnIdleEnd Agendador de Tarefas, objeto IdleSettings
- Objeto IdleSettings Agendador de Tarefas, Propriedade StopOnIdleEnd
topic_type:
- apiref
api_name:
- IdleSettings.StopOnIdleEnd
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f475c0a05d43cf0fbdd7097c1ee083f9040b07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824254"
---
# <a name="idlesettingsstoponidleend-property"></a><span data-ttu-id="c4369-106">Propriedade IdleSettings. StopOnIdleEnd</span><span class="sxs-lookup"><span data-stu-id="c4369-106">IdleSettings.StopOnIdleEnd property</span></span>

<span data-ttu-id="c4369-107">Para scripts, Obtém ou define um valor booliano que indica que o Agendador de Tarefas encerrará a tarefa se a condição de ociosidade terminar antes de a tarefa ser concluída.</span><span class="sxs-lookup"><span data-stu-id="c4369-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler will terminate the task if the idle condition ends before the task is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4369-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4369-108">Syntax</span></span>


```VB
IdleSettings.StopOnIdleEnd As Boolean
```



## <a name="property-value"></a><span data-ttu-id="c4369-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c4369-109">Property value</span></span>

<span data-ttu-id="c4369-110">Um valor booliano que indica que o Agendador de Tarefas encerrará a tarefa se a condição ociosa terminar antes de a tarefa ser concluída.</span><span class="sxs-lookup"><span data-stu-id="c4369-110">A Boolean value that indicates that the Task Scheduler will terminate the task if the idle condition ends before the task is completed.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4369-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4369-111">Remarks</span></span>

<span data-ttu-id="c4369-112">Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="c4369-112">When reading or writing XML for a task, this setting is specified in the [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4369-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4369-113">Requirements</span></span>



| <span data-ttu-id="c4369-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4369-114">Requirement</span></span> | <span data-ttu-id="c4369-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c4369-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4369-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4369-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c4369-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c4369-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c4369-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4369-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c4369-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c4369-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c4369-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c4369-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="c4369-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c4369-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c4369-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c4369-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4369-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4369-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4369-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4369-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4369-125">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="c4369-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="c4369-126">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="c4369-126">**IdleSettings**</span></span>](idlesettings.md)
</dt> </dl>

 

 





