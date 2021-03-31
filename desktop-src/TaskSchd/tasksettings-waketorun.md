---
title: Propriedade TaskSettings. WakeToRun
description: Para scripts, Obtém ou define um valor booliano que indica que o Agendador de Tarefas ativará o computador quando for hora de executar a tarefa.
ms.assetid: 51f83637-5bae-48c6-b750-b4467e651cec
keywords:
- Agendador de Tarefas da propriedade WakeToRun
- Propriedade WakeToRun Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade WakeToRun
topic_type:
- apiref
api_name:
- TaskSettings.WakeToRun
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b563fd1ecd27914e84043b85c44f0cf5262e9fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644475"
---
# <a name="tasksettingswaketorun-property"></a><span data-ttu-id="d9dcb-106">Propriedade TaskSettings. WakeToRun</span><span class="sxs-lookup"><span data-stu-id="d9dcb-106">TaskSettings.WakeToRun property</span></span>

<span data-ttu-id="d9dcb-107">Para scripts, Obtém ou define um valor booliano que indica que o Agendador de Tarefas ativará o computador quando for hora de executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="d9dcb-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler will wake the computer when it is time to run the task.</span></span>

<span data-ttu-id="d9dcb-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d9dcb-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9dcb-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d9dcb-109">Syntax</span></span>


```VB
TaskSettings.WakeToRun As Boolean
```



## <a name="property-value"></a><span data-ttu-id="d9dcb-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d9dcb-110">Property value</span></span>

<span data-ttu-id="d9dcb-111">Se for true, a propriedade indicará que o Agendador de Tarefas ativará o computador quando for hora de executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="d9dcb-111">If True, the property indicates that the Task Scheduler will wake the computer when it is time to run the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9dcb-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9dcb-112">Remarks</span></span>

<span data-ttu-id="d9dcb-113">Quando o serviço de Agendador de Tarefas ativa o computador para executar uma tarefa, a tela pode permanecer desativada, mesmo que o computador não esteja mais no modo de suspensão ou hibernação.</span><span class="sxs-lookup"><span data-stu-id="d9dcb-113">When the Task Scheduler service wakes the computer to run a task, the screen may remain off even though the computer is no longer in the sleep or hibernate mode.</span></span> <span data-ttu-id="d9dcb-114">A tela será ativada quando o Windows Vista detectar que um usuário voltou a usar o computador.</span><span class="sxs-lookup"><span data-stu-id="d9dcb-114">The screen will turn on when Windows Vista detects that a user has returned to use the computer.</span></span>

<span data-ttu-id="d9dcb-115">Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**WakeToRun**](taskschedulerschema-waketorun-settingstype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="d9dcb-115">When reading or writing XML for a task, this setting is specified in the [**WakeToRun**](taskschedulerschema-waketorun-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9dcb-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9dcb-116">Requirements</span></span>



| <span data-ttu-id="d9dcb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9dcb-117">Requirement</span></span> | <span data-ttu-id="d9dcb-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d9dcb-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9dcb-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9dcb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d9dcb-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d9dcb-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d9dcb-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9dcb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d9dcb-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d9dcb-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d9dcb-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d9dcb-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="d9dcb-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d9dcb-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d9dcb-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d9dcb-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9dcb-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9dcb-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9dcb-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d9dcb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9dcb-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="d9dcb-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





