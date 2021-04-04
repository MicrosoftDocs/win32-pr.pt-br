---
title: Propriedade RegisteredTask. NextRunTime
description: Para scripts, obtém a hora em que a tarefa registrada está agendada para ser executada.
ms.assetid: f63298a8-c9fa-4fea-ad0b-2c8739aced19
keywords:
- Agendador de Tarefas da propriedade NextRunTime
- Propriedade NextRunTime Agendador de Tarefas, objeto RegisteredTask
- Objeto RegisteredTask Agendador de Tarefas, Propriedade NextRunTime
topic_type:
- apiref
api_name:
- RegisteredTask.NextRunTime
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94db26c023ddd2c146586fbc433548517a84f234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644969"
---
# <a name="registeredtasknextruntime-property"></a><span data-ttu-id="68e42-106">Propriedade RegisteredTask. NextRunTime</span><span class="sxs-lookup"><span data-stu-id="68e42-106">RegisteredTask.NextRunTime property</span></span>

<span data-ttu-id="68e42-107">Para scripts, obtém a hora em que a tarefa registrada está agendada para ser executada.</span><span class="sxs-lookup"><span data-stu-id="68e42-107">For scripting, gets the time when the registered task is next scheduled to run.</span></span>

## <a name="syntax"></a><span data-ttu-id="68e42-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="68e42-108">Syntax</span></span>


```VB
RegisteredTask.NextRunTime As String
```



## <a name="property-value"></a><span data-ttu-id="68e42-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="68e42-109">Property value</span></span>

<span data-ttu-id="68e42-110">A hora em que a tarefa registrada está próxima agendada para ser executada.</span><span class="sxs-lookup"><span data-stu-id="68e42-110">The time when the registered task is next scheduled to run.</span></span>

## <a name="remarks"></a><span data-ttu-id="68e42-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="68e42-111">Remarks</span></span>

<span data-ttu-id="68e42-112">Se a tarefa registrada contiver gatilhos que são desabilitados individualmente, esses gatilhos ainda afetarão o próximo tempo de execução agendado que é retornado, embora estejam desabilitados.</span><span class="sxs-lookup"><span data-stu-id="68e42-112">If the registered task contains triggers that are individually disabled, these triggers will still affect the next scheduled run time that is returned even though they are disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="68e42-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68e42-113">Requirements</span></span>



| <span data-ttu-id="68e42-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="68e42-114">Requirement</span></span> | <span data-ttu-id="68e42-115">Valor</span><span class="sxs-lookup"><span data-stu-id="68e42-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68e42-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68e42-116">Minimum supported client</span></span><br/> | <span data-ttu-id="68e42-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="68e42-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="68e42-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68e42-118">Minimum supported server</span></span><br/> | <span data-ttu-id="68e42-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="68e42-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="68e42-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="68e42-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="68e42-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="68e42-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="68e42-122">DLL</span><span class="sxs-lookup"><span data-stu-id="68e42-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68e42-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68e42-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68e42-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="68e42-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68e42-125">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="68e42-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="68e42-126">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="68e42-126">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





