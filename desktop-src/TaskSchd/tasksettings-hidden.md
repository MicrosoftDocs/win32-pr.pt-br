---
title: Propriedade TaskSettings. Hidden
description: Para scripts, Obtém ou define um valor booliano que indica que a tarefa não estará visível na interface do usuário.
ms.assetid: 84a3d0b3-30f0-4356-b6cf-9bee3091612f
keywords:
- Agendador de Tarefas de propriedade oculta
- Propriedade Hidden Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade Hidden
topic_type:
- apiref
api_name:
- TaskSettings.Hidden
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057a3d920ba70260d23ad13a5888072ab5b07767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644959"
---
# <a name="tasksettingshidden-property"></a><span data-ttu-id="3b7ee-106">Propriedade TaskSettings. Hidden</span><span class="sxs-lookup"><span data-stu-id="3b7ee-106">TaskSettings.Hidden property</span></span>

<span data-ttu-id="3b7ee-107">Para scripts, Obtém ou define um valor booliano que indica que a tarefa não estará visível na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="3b7ee-107">For scripting, gets or sets a Boolean value that indicates that the task will not be visible in the UI.</span></span> <span data-ttu-id="3b7ee-108">No entanto, os administradores podem substituir essa configuração por meio do uso de um "comutador mestre" que torna todas as tarefas visíveis na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="3b7ee-108">However, administrators can override this setting through the use of a "master switch" that makes all tasks visible in the UI.</span></span>

<span data-ttu-id="3b7ee-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3b7ee-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b7ee-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b7ee-110">Syntax</span></span>


```VB
TaskSettings.Hidden As Boolean
```



## <a name="property-value"></a><span data-ttu-id="3b7ee-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3b7ee-111">Property value</span></span>

<span data-ttu-id="3b7ee-112">Se **for true**, o valor indicará que a tarefa não estará visível na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="3b7ee-112">If **True**, the value indicates that the task will not be visible in the UI.</span></span> <span data-ttu-id="3b7ee-113">Se **for false**, a tarefa ficará visível na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="3b7ee-113">If **False**, the task will be visible in the UI.</span></span> <span data-ttu-id="3b7ee-114">O padrão é **False**.</span><span class="sxs-lookup"><span data-stu-id="3b7ee-114">The default is **False**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b7ee-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b7ee-115">Remarks</span></span>

<span data-ttu-id="3b7ee-116">Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**oculto (settingstype)**](taskschedulerschema-hidden-settingstype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="3b7ee-116">When reading or writing XML for a task, this setting is specified in the [**Hidden (settingsType)**](taskschedulerschema-hidden-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b7ee-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b7ee-117">Requirements</span></span>



| <span data-ttu-id="3b7ee-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b7ee-118">Requirement</span></span> | <span data-ttu-id="3b7ee-119">Valor</span><span class="sxs-lookup"><span data-stu-id="3b7ee-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b7ee-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b7ee-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3b7ee-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3b7ee-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3b7ee-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b7ee-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3b7ee-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3b7ee-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3b7ee-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3b7ee-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="3b7ee-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3b7ee-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3b7ee-126">DLL</span><span class="sxs-lookup"><span data-stu-id="3b7ee-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b7ee-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b7ee-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b7ee-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="3b7ee-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b7ee-129">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="3b7ee-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





