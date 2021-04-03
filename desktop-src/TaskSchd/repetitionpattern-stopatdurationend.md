---
title: Propriedade RepetitionPattern. StopAtDurationEnd
description: Para scripts, Obtém ou define um valor booliano que indica se uma instância em execução da tarefa é interrompida no final da duração do padrão de repetição.
ms.assetid: 421f2d6f-7c35-44b4-97f2-45f46ca5e40e
keywords:
- Agendador de Tarefas da propriedade StopAtDurationEnd
- Propriedade StopAtDurationEnd Agendador de Tarefas, objeto RepetitionPattern
- Objeto RepetitionPattern Agendador de Tarefas, Propriedade StopAtDurationEnd
topic_type:
- apiref
api_name:
- RepetitionPattern.StopAtDurationEnd
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b95d7e8941a4249991692dffbd3cac9ad1ca7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644884"
---
# <a name="repetitionpatternstopatdurationend-property"></a><span data-ttu-id="591a7-106">Propriedade RepetitionPattern. StopAtDurationEnd</span><span class="sxs-lookup"><span data-stu-id="591a7-106">RepetitionPattern.StopAtDurationEnd property</span></span>

<span data-ttu-id="591a7-107">Para scripts, Obtém ou define um valor booliano que indica se uma instância em execução da tarefa é interrompida no final da duração do padrão de repetição.</span><span class="sxs-lookup"><span data-stu-id="591a7-107">For scripting, gets or sets a Boolean value that indicates if a running instance of the task is stopped at the end of the repetition pattern duration.</span></span>

## <a name="syntax"></a><span data-ttu-id="591a7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="591a7-108">Syntax</span></span>


```VB
RepetitionPattern.StopAtDurationEnd As Boolean
```



## <a name="property-value"></a><span data-ttu-id="591a7-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="591a7-109">Property value</span></span>

<span data-ttu-id="591a7-110">Um valor booliano que indica se uma instância em execução da tarefa é interrompida no final da duração do padrão de repetição.</span><span class="sxs-lookup"><span data-stu-id="591a7-110">A Boolean value that indicates if a running instance of the task is stopped at the end of the repetition pattern duration.</span></span>

## <a name="remarks"></a><span data-ttu-id="591a7-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="591a7-111">Remarks</span></span>

<span data-ttu-id="591a7-112">Ao ler ou gravar XML para uma tarefa, essas informações são especificadas no elemento [**StopAtDurationEnd**](taskschedulerschema-stopatdurationend-repetitiontype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="591a7-112">When reading or writing XML for a task, this information is specified in the [**StopAtDurationEnd**](taskschedulerschema-stopatdurationend-repetitiontype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="591a7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="591a7-113">Requirements</span></span>



| <span data-ttu-id="591a7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="591a7-114">Requirement</span></span> | <span data-ttu-id="591a7-115">Valor</span><span class="sxs-lookup"><span data-stu-id="591a7-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="591a7-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="591a7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="591a7-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="591a7-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="591a7-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="591a7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="591a7-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="591a7-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="591a7-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="591a7-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="591a7-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="591a7-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="591a7-122">DLL</span><span class="sxs-lookup"><span data-stu-id="591a7-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="591a7-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="591a7-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="591a7-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="591a7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="591a7-125">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="591a7-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





