---
title: Propriedade TaskSettings. DisallowStartIfOnBatteries
description: Para scripts, Obtém ou define um valor booliano que indica que a tarefa não será iniciada se o computador estiver sendo executado em baterias.
ms.assetid: 5e13f168-a396-495f-a486-e64e8524c8cd
keywords:
- Agendador de Tarefas da propriedade DisallowStartIfOnBatteries
- Propriedade DisallowStartIfOnBatteries Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade DisallowStartIfOnBatteries
topic_type:
- apiref
api_name:
- TaskSettings.DisallowStartIfOnBatteries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35a7fde3012b25dfeab65e6e6088bb1d950892d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086111"
---
# <a name="tasksettingsdisallowstartifonbatteries-property"></a><span data-ttu-id="86e25-106">Propriedade TaskSettings. DisallowStartIfOnBatteries</span><span class="sxs-lookup"><span data-stu-id="86e25-106">TaskSettings.DisallowStartIfOnBatteries property</span></span>

<span data-ttu-id="86e25-107">Para scripts, Obtém ou define um valor booliano que indica que a tarefa não será iniciada se o computador estiver sendo executado em baterias.</span><span class="sxs-lookup"><span data-stu-id="86e25-107">For scripting, gets or sets a Boolean value that indicates that the task will not be started if the computer is running on batteries.</span></span>

<span data-ttu-id="86e25-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="86e25-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="86e25-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="86e25-109">Syntax</span></span>


```VB
TaskSettings.DisallowStartIfOnBatteries As Boolean
```



## <a name="property-value"></a><span data-ttu-id="86e25-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="86e25-110">Property value</span></span>

<span data-ttu-id="86e25-111">Um valor booliano que indica que a tarefa não será iniciada se o computador estiver sendo executado em baterias.</span><span class="sxs-lookup"><span data-stu-id="86e25-111">A Boolean value that indicates that the task will not be started if the computer is running on batteries.</span></span> <span data-ttu-id="86e25-112">Se for true, a tarefa não será iniciada se o computador estiver sendo executado em baterias.</span><span class="sxs-lookup"><span data-stu-id="86e25-112">If True, the task will not be started if the computer is running on batteries.</span></span> <span data-ttu-id="86e25-113">Se for false, a tarefa será iniciada se o computador estiver sendo executado em baterias.</span><span class="sxs-lookup"><span data-stu-id="86e25-113">If False, the task will be started if the computer is running on batteries.</span></span> <span data-ttu-id="86e25-114">O padrão é True.</span><span class="sxs-lookup"><span data-stu-id="86e25-114">The default is True.</span></span>

## <a name="remarks"></a><span data-ttu-id="86e25-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="86e25-115">Remarks</span></span>

<span data-ttu-id="86e25-116">Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="86e25-116">When reading or writing XML for a task, this setting is specified in the [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="86e25-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86e25-117">Requirements</span></span>



| <span data-ttu-id="86e25-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="86e25-118">Requirement</span></span> | <span data-ttu-id="86e25-119">Valor</span><span class="sxs-lookup"><span data-stu-id="86e25-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86e25-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86e25-120">Minimum supported client</span></span><br/> | <span data-ttu-id="86e25-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="86e25-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="86e25-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86e25-122">Minimum supported server</span></span><br/> | <span data-ttu-id="86e25-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="86e25-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="86e25-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="86e25-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="86e25-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="86e25-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="86e25-126">DLL</span><span class="sxs-lookup"><span data-stu-id="86e25-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86e25-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86e25-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86e25-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="86e25-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86e25-129">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="86e25-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





