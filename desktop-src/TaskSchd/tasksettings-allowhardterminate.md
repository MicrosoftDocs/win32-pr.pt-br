---
title: Propriedade TaskSettings. AllowHardTerminate
description: Para scripts, Obtém ou define um valor booliano que indica que a tarefa pode ser encerrada pelo serviço de Agendador de Tarefas usando o TerminateProcess.
ms.assetid: 1dfd692e-efbe-41a2-8dbd-b14cf26bbcb7
keywords:
- Agendador de Tarefas da propriedade AllowHardTerminate
- Propriedade AllowHardTerminate Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade AllowHardTerminate
topic_type:
- apiref
api_name:
- TaskSettings.AllowHardTerminate
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c38e117ebc3d2175b952f01698987ccb65f7af5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644878"
---
# <a name="tasksettingsallowhardterminate-property"></a><span data-ttu-id="4ed51-106">Propriedade TaskSettings. AllowHardTerminate</span><span class="sxs-lookup"><span data-stu-id="4ed51-106">TaskSettings.AllowHardTerminate property</span></span>

<span data-ttu-id="4ed51-107">Para scripts, Obtém ou define um valor booliano que indica que a tarefa pode ser encerrada pelo serviço de Agendador de Tarefas usando o [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).</span><span class="sxs-lookup"><span data-stu-id="4ed51-107">For scripting, gets or sets a Boolean value that indicates that the task may be terminated by the Task Scheduler service using [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).</span></span> <span data-ttu-id="4ed51-108">O serviço tentará fechar a tarefa em execução enviando a notificação [**de \_ fechamento do WM**](../winmsg/wm-close.md) e, se a tarefa não responder, a tarefa será encerrada somente se essa propriedade for definida como true.</span><span class="sxs-lookup"><span data-stu-id="4ed51-108">The service will try to close the running task by sending the [**WM\_CLOSE**](../winmsg/wm-close.md) notification, and if the task does not respond, the task will be terminated only if this property is set to true.</span></span>

<span data-ttu-id="4ed51-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4ed51-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ed51-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ed51-110">Syntax</span></span>


```VB
TaskSettings.AllowHardTerminate As Boolean
```



## <a name="property-value"></a><span data-ttu-id="4ed51-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4ed51-111">Property value</span></span>

<span data-ttu-id="4ed51-112">Se for true, a tarefa poderá ser encerrada usando [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).</span><span class="sxs-lookup"><span data-stu-id="4ed51-112">If True, the task can be terminated by using [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).</span></span> <span data-ttu-id="4ed51-113">Se for false, a tarefa não poderá ser encerrada usando **TerminateProcess**.</span><span class="sxs-lookup"><span data-stu-id="4ed51-113">If False, the task cannot be terminated by using **TerminateProcess**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ed51-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ed51-114">Remarks</span></span>

<span data-ttu-id="4ed51-115">Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [AllowHardTerminate](taskschedulerschema-allowhardterminate-settingstype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="4ed51-115">When reading or writing XML for a task, this setting is specified in the [AllowHardTerminate](taskschedulerschema-allowhardterminate-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ed51-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ed51-116">Requirements</span></span>



| <span data-ttu-id="4ed51-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ed51-117">Requirement</span></span> | <span data-ttu-id="4ed51-118">Valor</span><span class="sxs-lookup"><span data-stu-id="4ed51-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ed51-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ed51-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4ed51-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4ed51-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4ed51-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ed51-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4ed51-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4ed51-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4ed51-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4ed51-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="4ed51-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4ed51-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4ed51-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4ed51-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ed51-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ed51-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ed51-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4ed51-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ed51-128">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="4ed51-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

