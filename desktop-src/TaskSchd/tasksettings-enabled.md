---
title: Propriedade TaskSettings. Enabled
description: Para scripts, Obtém ou define um valor booliano que indica que a tarefa está habilitada. A tarefa pode ser executada somente quando essa configuração for verdadeira.
ms.assetid: af8aa237-3402-4a82-b6ef-b713e1757d3a
keywords:
- Propriedade habilitada Agendador de Tarefas
- Propriedade Enabled Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade Enabled
topic_type:
- apiref
api_name:
- TaskSettings.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6805d7b754ac2c3553d5fde91826ffa192b91d97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369740"
---
# <a name="tasksettingsenabled-property"></a><span data-ttu-id="7df98-107">Propriedade TaskSettings. Enabled</span><span class="sxs-lookup"><span data-stu-id="7df98-107">TaskSettings.Enabled property</span></span>

<span data-ttu-id="7df98-108">Para scripts, Obtém ou define um valor booliano que indica que a tarefa está habilitada.</span><span class="sxs-lookup"><span data-stu-id="7df98-108">For scripting, gets or sets a Boolean value that indicates that the task is enabled.</span></span> <span data-ttu-id="7df98-109">A tarefa pode ser executada somente quando essa configuração for verdadeira.</span><span class="sxs-lookup"><span data-stu-id="7df98-109">The task can be performed only when this setting is True.</span></span>

<span data-ttu-id="7df98-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="7df98-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7df98-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="7df98-111">Syntax</span></span>


```VB
TaskSettings.Enabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="7df98-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7df98-112">Property value</span></span>

<span data-ttu-id="7df98-113">Se for true, a tarefa será habilitada.</span><span class="sxs-lookup"><span data-stu-id="7df98-113">If True, the task is enabled.</span></span> <span data-ttu-id="7df98-114">Se for false, a tarefa não estará habilitada.</span><span class="sxs-lookup"><span data-stu-id="7df98-114">If False, the task is not enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="7df98-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="7df98-115">Remarks</span></span>

<span data-ttu-id="7df98-116">Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**habilitado (settingstype)**](taskschedulerschema-enabled-settingstype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="7df98-116">When reading or writing XML for a task, this setting is specified in the [**Enabled (settingsType)**](taskschedulerschema-enabled-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="7df98-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7df98-117">Requirements</span></span>



| <span data-ttu-id="7df98-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7df98-118">Requirement</span></span> | <span data-ttu-id="7df98-119">Valor</span><span class="sxs-lookup"><span data-stu-id="7df98-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7df98-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7df98-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7df98-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7df98-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7df98-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7df98-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7df98-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7df98-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7df98-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7df98-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="7df98-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7df98-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7df98-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7df98-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7df98-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7df98-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7df98-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="7df98-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7df98-129">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="7df98-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





