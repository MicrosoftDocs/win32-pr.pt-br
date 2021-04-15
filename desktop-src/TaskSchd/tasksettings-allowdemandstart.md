---
title: Propriedade TaskSettings. AllowDemandStart
description: Para scripts, Obtém ou define um valor booliano que indica que a tarefa pode ser iniciada usando o comando executar ou o menu de contexto.
ms.assetid: 1eae19ae-3b4d-4eb2-82d0-685ef2729f36
keywords:
- Agendador de Tarefas da propriedade AllowDemandStart
- Propriedade AllowDemandStart Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade AllowDemandStart
topic_type:
- apiref
api_name:
- TaskSettings.AllowDemandStart
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 657ba45e0809b74803e27de70fae52576fcf2a26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369332"
---
# <a name="tasksettingsallowdemandstart-property"></a><span data-ttu-id="146ae-106">Propriedade TaskSettings. AllowDemandStart</span><span class="sxs-lookup"><span data-stu-id="146ae-106">TaskSettings.AllowDemandStart property</span></span>

<span data-ttu-id="146ae-107">Para scripts, Obtém ou define um valor booliano que indica que a tarefa pode ser iniciada usando o comando executar ou o menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="146ae-107">For scripting, gets or sets a Boolean value that indicates that the task can be started by using either the Run command or the Context menu.</span></span>

<span data-ttu-id="146ae-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="146ae-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="146ae-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="146ae-109">Syntax</span></span>


```VB
TaskSettings.AllowDemandStart As Boolean
```



## <a name="property-value"></a><span data-ttu-id="146ae-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="146ae-110">Property value</span></span>

<span data-ttu-id="146ae-111">Se for true, a tarefa poderá ser executada usando o comando Run ou o menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="146ae-111">If True, the task can be run by using the Run command or the Context menu.</span></span> <span data-ttu-id="146ae-112">Se for false, a tarefa não poderá ser executada usando o comando executar ou o menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="146ae-112">If False, the task cannot be run using the Run command or the Context menu.</span></span> <span data-ttu-id="146ae-113">O padrão é True.</span><span class="sxs-lookup"><span data-stu-id="146ae-113">The default is True.</span></span>

## <a name="remarks"></a><span data-ttu-id="146ae-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="146ae-114">Remarks</span></span>

<span data-ttu-id="146ae-115">Quando essa propriedade é definida como true, a tarefa pode ser iniciada independentemente de quando os gatilhos iniciam a tarefa.</span><span class="sxs-lookup"><span data-stu-id="146ae-115">When this property is set to True, the task can be started independent of when any triggers start the task.</span></span>

<span data-ttu-id="146ae-116">Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [AllowStartOnDemand](taskschedulerschema-allowstartondemand-settingstype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="146ae-116">When reading or writing XML for a task, this setting is specified in the [AllowStartOnDemand](taskschedulerschema-allowstartondemand-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="146ae-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="146ae-117">Requirements</span></span>



| <span data-ttu-id="146ae-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="146ae-118">Requirement</span></span> | <span data-ttu-id="146ae-119">Valor</span><span class="sxs-lookup"><span data-stu-id="146ae-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="146ae-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="146ae-120">Minimum supported client</span></span><br/> | <span data-ttu-id="146ae-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="146ae-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="146ae-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="146ae-122">Minimum supported server</span></span><br/> | <span data-ttu-id="146ae-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="146ae-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="146ae-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="146ae-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="146ae-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="146ae-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="146ae-126">DLL</span><span class="sxs-lookup"><span data-stu-id="146ae-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="146ae-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="146ae-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="146ae-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="146ae-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="146ae-129">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="146ae-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





