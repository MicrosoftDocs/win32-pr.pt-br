---
title: Propriedade IdleSettings. RestartOnIdle
description: Para scripts, Obtém ou define um valor booliano que indica se a tarefa é reiniciada quando o computador entra em uma condição ociosa mais de uma vez.
ms.assetid: c77b6f5f-659c-4aa0-a5f7-39c01e5ca65e
keywords:
- Agendador de Tarefas da propriedade RestartOnIdle
- Propriedade RestartOnIdle Agendador de Tarefas, objeto IdleSettings
- Objeto IdleSettings Agendador de Tarefas, Propriedade RestartOnIdle
topic_type:
- apiref
api_name:
- IdleSettings.RestartOnIdle
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e80b2e523f2f19222292eac7752847a72291c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761812"
---
# <a name="idlesettingsrestartonidle-property"></a><span data-ttu-id="9c577-106">Propriedade IdleSettings. RestartOnIdle</span><span class="sxs-lookup"><span data-stu-id="9c577-106">IdleSettings.RestartOnIdle property</span></span>

<span data-ttu-id="9c577-107">Para scripts, Obtém ou define um valor booliano que indica se a tarefa é reiniciada quando o computador entra em uma condição ociosa mais de uma vez.</span><span class="sxs-lookup"><span data-stu-id="9c577-107">For scripting, gets or sets a Boolean value that indicates whether the task is restarted when the computer cycles into an idle condition more than once.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c577-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c577-108">Syntax</span></span>


```VB
IdleSettings.RestartOnIdle As Boolean
```



## <a name="property-value"></a><span data-ttu-id="9c577-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="9c577-109">Property value</span></span>

<span data-ttu-id="9c577-110">Um valor booliano que indica se a tarefa deve ser reiniciada quando o computador entrar em uma condição ociosa mais de uma vez.</span><span class="sxs-lookup"><span data-stu-id="9c577-110">A Boolean value that indicates whether the task must be restarted when the computer cycles into an idle condition more than once.</span></span> <span data-ttu-id="9c577-111">O padrão é False.</span><span class="sxs-lookup"><span data-stu-id="9c577-111">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c577-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c577-112">Remarks</span></span>

<span data-ttu-id="9c577-113">Essa propriedade só será usada se a propriedade [**IdleSettings. StopOnIdleEnd**](idlesettings-stoponidleend.md) for definida como true.</span><span class="sxs-lookup"><span data-stu-id="9c577-113">This property is only used if the [**IdleSettings.StopOnIdleEnd**](idlesettings-stoponidleend.md) property is set to True.</span></span>

<span data-ttu-id="9c577-114">Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="9c577-114">When reading or writing XML for a task, this setting is specified in the [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c577-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c577-115">Requirements</span></span>



| <span data-ttu-id="9c577-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c577-116">Requirement</span></span> | <span data-ttu-id="9c577-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9c577-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c577-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c577-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9c577-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9c577-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9c577-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c577-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9c577-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9c577-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9c577-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9c577-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="9c577-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9c577-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9c577-124">DLL</span><span class="sxs-lookup"><span data-stu-id="9c577-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c577-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c577-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c577-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c577-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c577-127">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="9c577-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="9c577-128">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="9c577-128">**IdleSettings**</span></span>](idlesettings.md)
</dt> </dl>

 

 





