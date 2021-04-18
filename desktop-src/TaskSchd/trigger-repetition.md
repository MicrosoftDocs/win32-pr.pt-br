---
title: Propriedade Trigger. Repetition
description: Para scripts, Obtém ou define um valor que indica com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.
ms.assetid: f90b935c-8b69-4c82-ac4b-6b049e7b9703
keywords:
- Agendador de Tarefas da propriedade de repetição
- Agendador de Tarefas de propriedade de repetição, objeto de gatilho
- Objeto de gatilho Agendador de Tarefas, propriedade de repetição
topic_type:
- apiref
api_name:
- Trigger.Repetition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611c7e42a14de06a8777333a6dc640781943ba06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758390"
---
# <a name="triggerrepetition-property"></a><span data-ttu-id="185c9-106">Propriedade Trigger. Repetition</span><span class="sxs-lookup"><span data-stu-id="185c9-106">Trigger.Repetition property</span></span>

<span data-ttu-id="185c9-107">Para scripts, Obtém ou define um valor que indica com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="185c9-107">For scripting, gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span>

## <a name="syntax"></a><span data-ttu-id="185c9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="185c9-108">Syntax</span></span>


```VB
Trigger.Repetition As RepetitionPattern
```



## <a name="property-value"></a><span data-ttu-id="185c9-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="185c9-109">Property value</span></span>

<span data-ttu-id="185c9-110">Um objeto [**RepetitionPattern**](repetitionpattern.md) que define a frequência em que a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.</span><span class="sxs-lookup"><span data-stu-id="185c9-110">A [**RepetitionPattern**](repetitionpattern.md) object that defines how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span>

## <a name="remarks"></a><span data-ttu-id="185c9-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="185c9-111">Remarks</span></span>

<span data-ttu-id="185c9-112">Ao ler ou gravar seu próprio XML para uma tarefa, o padrão de repetição para um gatilho é especificado no elemento de [**repetição**](taskschedulerschema-repetition-triggerbasetype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="185c9-112">When reading or writing your own XML for a task, the repetition pattern for a trigger is specified in the [**Repetition**](taskschedulerschema-repetition-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="185c9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="185c9-113">Requirements</span></span>



| <span data-ttu-id="185c9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="185c9-114">Requirement</span></span> | <span data-ttu-id="185c9-115">Valor</span><span class="sxs-lookup"><span data-stu-id="185c9-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="185c9-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="185c9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="185c9-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="185c9-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="185c9-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="185c9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="185c9-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="185c9-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="185c9-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="185c9-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="185c9-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="185c9-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="185c9-122">DLL</span><span class="sxs-lookup"><span data-stu-id="185c9-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="185c9-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="185c9-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="185c9-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="185c9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="185c9-125">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="185c9-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="185c9-126">**RepetitionPattern**</span><span class="sxs-lookup"><span data-stu-id="185c9-126">**RepetitionPattern**</span></span>](repetitionpattern.md)
</dt> </dl>

 

 





