---
title: Propriedade RunningTask. State
description: Para scripts, obtém um identificador para o estado da tarefa em execução.
ms.assetid: 048863f4-b80b-42ab-bd74-ec761a8f03aa
keywords:
- Agendador de Tarefas de propriedade de estado
- Agendador de Tarefas de propriedade de estado, objeto RunningTask
- Agendador de Tarefas de objeto RunningTask, propriedade State
topic_type:
- apiref
api_name:
- RunningTask.State
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b962de116eef1301be209828181147dfe03273e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644488"
---
# <a name="runningtaskstate-property"></a><span data-ttu-id="7177b-106">Propriedade RunningTask. State</span><span class="sxs-lookup"><span data-stu-id="7177b-106">RunningTask.State property</span></span>

<span data-ttu-id="7177b-107">Para scripts, obtém um identificador para o estado da tarefa em execução.</span><span class="sxs-lookup"><span data-stu-id="7177b-107">For scripting, gets an identifier for the state of the running task.</span></span>

<span data-ttu-id="7177b-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="7177b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7177b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7177b-109">Syntax</span></span>


```VB
RunningTask.State As String
```



## <a name="property-value"></a><span data-ttu-id="7177b-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7177b-110">Property value</span></span>

<span data-ttu-id="7177b-111">Um identificador para o estado da tarefa em execução.</span><span class="sxs-lookup"><span data-stu-id="7177b-111">An identifier for the state of the running task.</span></span>



| <span data-ttu-id="7177b-112">Valor</span><span class="sxs-lookup"><span data-stu-id="7177b-112">Value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="7177b-113">Significado</span><span class="sxs-lookup"><span data-stu-id="7177b-113">Meaning</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_STATE_UNKNOWN"></span><span id="task_state_unknown"></span><dl> <span data-ttu-id="7177b-114"><dt>**Tarefa \_ do ESTADO \_ desconhecido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7177b-114"><dt>**TASK\_STATE\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="7177b-115">O estado da tarefa é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="7177b-115">The state of the task is unknown.</span></span><br/>                                                                                                      |
| <span id="TASK_STATE_DISABLED"></span><span id="task_state_disabled"></span><dl> <span data-ttu-id="7177b-116"><dt>**Tarefa \_ do ESTADO \_ desabilitado**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7177b-116"><dt>**TASK\_STATE\_DISABLED**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="7177b-117">A tarefa está registrada, mas está desabilitada e nenhuma instância da tarefa está em fila ou em execução.</span><span class="sxs-lookup"><span data-stu-id="7177b-117">The task is registered but is disabled and no instances of the task are queued or running.</span></span> <span data-ttu-id="7177b-118">A tarefa não pode ser executada até que esteja habilitada.</span><span class="sxs-lookup"><span data-stu-id="7177b-118">The task cannot be run until it is enabled.</span></span><br/> |
| <span id="TASK_STATE_QUEUED"></span><span id="task_state_queued"></span><dl> <span data-ttu-id="7177b-119"><dt>**Tarefa \_ do ESTADO \_ na fila**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7177b-119"><dt>**TASK\_STATE\_QUEUED**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="7177b-120">As instâncias da tarefa são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="7177b-120">Instances of the task are queued.</span></span><br/>                                                                                                      |
| <span id="TASK_STATE_READY"></span><span id="task_state_ready"></span><dl> <span data-ttu-id="7177b-121"><dt>**Tarefa \_ do ESTADO \_ pronto**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7177b-121"><dt>**TASK\_STATE\_READY**</dt> <dt>3</dt></span></span> </dl>          | <span data-ttu-id="7177b-122">A tarefa está pronta para ser executada, mas nenhuma instância está enfileirada ou em execução.</span><span class="sxs-lookup"><span data-stu-id="7177b-122">The task is ready to be executed, but no instances are queued or running.</span></span><br/>                                                              |
| <span id="TASK_STATE_RUNNING"></span><span id="task_state_running"></span><dl> <span data-ttu-id="7177b-123"><dt>**Tarefa \_ do ESTADO \_ em execução**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="7177b-123"><dt>**TASK\_STATE\_RUNNING**</dt> <dt>4</dt></span></span> </dl>    | <span data-ttu-id="7177b-124">Uma ou mais instâncias da tarefa estão em execução.</span><span class="sxs-lookup"><span data-stu-id="7177b-124">One or more instances of the task are running.</span></span><br/>                                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="7177b-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="7177b-125">Remarks</span></span>

<span data-ttu-id="7177b-126">O método [**RunningTask. Refresh**](runningtask-refresh.md) é chamado antes que o valor da propriedade seja retornado.</span><span class="sxs-lookup"><span data-stu-id="7177b-126">The [**RunningTask.Refresh**](runningtask-refresh.md) method is called before the property value is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="7177b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7177b-127">Requirements</span></span>



| <span data-ttu-id="7177b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7177b-128">Requirement</span></span> | <span data-ttu-id="7177b-129">Valor</span><span class="sxs-lookup"><span data-stu-id="7177b-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7177b-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7177b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7177b-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7177b-131">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7177b-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7177b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7177b-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7177b-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7177b-134">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7177b-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="7177b-135"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7177b-135"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7177b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7177b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7177b-137"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7177b-137"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





