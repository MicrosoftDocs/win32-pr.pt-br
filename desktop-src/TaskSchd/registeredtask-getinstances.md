---
title: Método RegisteredTask. GetInstances
description: Para scripts, retorna todas as instâncias atualmente em execução da tarefa registrada.
ms.assetid: 01fea94e-fdec-4edf-886a-f6d9b566f201
keywords:
- Método GetInstances Agendador de Tarefas
- Método GetInstances Agendador de Tarefas, objeto RegisteredTask
- Objeto RegisteredTask Agendador de Tarefas, método GetInstances
topic_type:
- apiref
api_name:
- RegisteredTask.GetInstances
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78b1579df1124fcd6d26ea658730190b5eb0f5de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086077"
---
# <a name="registeredtaskgetinstances-method"></a><span data-ttu-id="27e14-106">Método RegisteredTask. GetInstances</span><span class="sxs-lookup"><span data-stu-id="27e14-106">RegisteredTask.GetInstances method</span></span>

<span data-ttu-id="27e14-107">Para scripts, retorna todas as instâncias atualmente em execução da tarefa registrada.</span><span class="sxs-lookup"><span data-stu-id="27e14-107">For scripting, returns all currently running instances of the registered task.</span></span>

> [!Note]  
> <span data-ttu-id="27e14-108">**RegisteredTask. GetInstances** retornará apenas instâncias da tarefa registrada em execução no momento que estão em execução no contexto de segurança de um usuário ou abaixo dele.</span><span class="sxs-lookup"><span data-stu-id="27e14-108">**RegisteredTask.GetInstances** will only return instances of the currently running registered task that are running at or below a user's security context.</span></span> <span data-ttu-id="27e14-109">Por exemplo, para membros do grupo Administradores, as **GetInstances** retornarão todas as instâncias da tarefa registrada atualmente em execução, mas, para os membros do grupo usuários, **GetInstances** retornará apenas as instâncias da tarefa registrada atualmente em execução no contexto de segurança do grupo de usuários.</span><span class="sxs-lookup"><span data-stu-id="27e14-109">For example, for members of the Administrators group, **GetInstances** will return all instances of the currently running registered task, but for members of the Users group, **GetInstances** will only return instances of the currently running registered task that are running under the Users group security context.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="27e14-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27e14-110">Syntax</span></span>


```VB
RegisteredTask.GetInstances( _
  ByVal flags, _
  ByRef runningTasks _
)
```



## <a name="parameters"></a><span data-ttu-id="27e14-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27e14-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27e14-112">*sinalizadores*</span><span class="sxs-lookup"><span data-stu-id="27e14-112">*flags*</span></span> 
</dt> <dd>

<span data-ttu-id="27e14-113">Esse parâmetro é reservado para uso futuro e deve ser definido como 0.</span><span class="sxs-lookup"><span data-stu-id="27e14-113">This parameter is reserved for future use and must be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="27e14-114">*runningTasks* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="27e14-114">*runningTasks* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27e14-115">Um objeto [**RunningTaskCollection**](runningtaskcollection.md) que contém todas as instâncias atualmente em execução da tarefa.</span><span class="sxs-lookup"><span data-stu-id="27e14-115">A [**RunningTaskCollection**](runningtaskcollection.md) object that contains all currently running instances of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27e14-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="27e14-116">Return value</span></span>

<span data-ttu-id="27e14-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="27e14-117">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="27e14-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27e14-118">Requirements</span></span>



| <span data-ttu-id="27e14-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="27e14-119">Requirement</span></span> | <span data-ttu-id="27e14-120">Valor</span><span class="sxs-lookup"><span data-stu-id="27e14-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27e14-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27e14-121">Minimum supported client</span></span><br/> | <span data-ttu-id="27e14-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="27e14-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="27e14-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27e14-123">Minimum supported server</span></span><br/> | <span data-ttu-id="27e14-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="27e14-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="27e14-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="27e14-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="27e14-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="27e14-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="27e14-127">DLL</span><span class="sxs-lookup"><span data-stu-id="27e14-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27e14-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27e14-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27e14-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="27e14-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27e14-130">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="27e14-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="27e14-131">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="27e14-131">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





