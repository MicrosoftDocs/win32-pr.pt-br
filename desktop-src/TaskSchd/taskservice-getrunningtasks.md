---
title: Método TaskService. GetRunningTasks
description: Para scripts, obtém uma coleção de tarefas em execução.
ms.assetid: bae3c035-a6b2-4ca5-970b-d4bc808068ad
keywords:
- Agendador de Tarefas do método GetRunningTasks
- Método GetRunningTasks Agendador de Tarefas, objeto TaskService
- Objeto TaskService Agendador de Tarefas, método GetRunningTasks
topic_type:
- apiref
api_name:
- TaskService.GetRunningTasks
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec585b9ed46af9a283e337c8f200687c512cd36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645209"
---
# <a name="taskservicegetrunningtasks-method"></a><span data-ttu-id="e22f6-106">Método TaskService. GetRunningTasks</span><span class="sxs-lookup"><span data-stu-id="e22f6-106">TaskService.GetRunningTasks method</span></span>

<span data-ttu-id="e22f6-107">Para scripts, obtém uma coleção de tarefas em execução.</span><span class="sxs-lookup"><span data-stu-id="e22f6-107">For scripting, gets a collection of running tasks.</span></span>

> [!Note]  
> <span data-ttu-id="e22f6-108">**TaskService. GetRunningTasks** retornará apenas uma coleção de tarefas em execução em execução no contexto de segurança de um usuário ou abaixo dele.</span><span class="sxs-lookup"><span data-stu-id="e22f6-108">**TaskService.GetRunningTasks** will only return a collection of running tasks that are running at or below a user's security context.</span></span> <span data-ttu-id="e22f6-109">Por exemplo, para membros do grupo Administradores, **GetRunningTasks** retornará uma coleção de todas as tarefas em execução, mas para os membros do grupo usuários, o **GetRunningTasks** retornará apenas uma coleção de tarefas que estão sendo executadas no contexto de segurança do grupo usuários.</span><span class="sxs-lookup"><span data-stu-id="e22f6-109">For example, for members of the Administrators group, **GetRunningTasks** will return a collection of all running tasks, but for members of the Users group, **GetRunningTasks** will only return a collection of tasks that are running under the Users group security context.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e22f6-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e22f6-110">Syntax</span></span>


```VB
TaskService.GetRunningTasks( _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="e22f6-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e22f6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e22f6-112">*sinalizadores* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="e22f6-112">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e22f6-113">Passe 1 para retornar todas as tarefas em execução, incluindo tarefas ocultas.</span><span class="sxs-lookup"><span data-stu-id="e22f6-113">Pass in 1 to return all running tasks, including hidden tasks.</span></span> <span data-ttu-id="e22f6-114">Passe 0 para retornar uma coleção de tarefas em execução que não são tarefas ocultas.</span><span class="sxs-lookup"><span data-stu-id="e22f6-114">Pass in 0 to return a collection of running tasks that are not hidden tasks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e22f6-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e22f6-115">Return value</span></span>

<span data-ttu-id="e22f6-116">Um objeto [**RunningTaskCollection**](runningtaskcollection.md) que contém as tarefas em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="e22f6-116">A [**RunningTaskCollection**](runningtaskcollection.md) object that contains the currently running tasks.</span></span>

## <a name="requirements"></a><span data-ttu-id="e22f6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e22f6-117">Requirements</span></span>



| <span data-ttu-id="e22f6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e22f6-118">Requirement</span></span> | <span data-ttu-id="e22f6-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e22f6-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e22f6-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e22f6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e22f6-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e22f6-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e22f6-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e22f6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e22f6-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e22f6-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e22f6-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e22f6-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="e22f6-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e22f6-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e22f6-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e22f6-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e22f6-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e22f6-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e22f6-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="e22f6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e22f6-129">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="e22f6-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





