---
title: Método RegisteredTask. Stop
description: Para scripts, o interrompe a tarefa registrada imediatamente.
ms.assetid: e4a533d8-5cf0-46ba-a603-f7a9c59ab0fd
keywords:
- Agendador de Tarefas do método Stop
- Método Stop Agendador de Tarefas, objeto RegisteredTask
- Agendador de Tarefas de objeto RegisteredTask, método Stop
topic_type:
- apiref
api_name:
- RegisteredTask.Stop
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d51cf748bb65a9db38c56fded102ddeb5b40fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369880"
---
# <a name="registeredtaskstop-method"></a><span data-ttu-id="9ff84-106">Método RegisteredTask. Stop</span><span class="sxs-lookup"><span data-stu-id="9ff84-106">RegisteredTask.Stop method</span></span>

<span data-ttu-id="9ff84-107">Para scripts, o interrompe a tarefa registrada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="9ff84-107">For scripting, stops the registered task immediately.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ff84-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9ff84-108">Syntax</span></span>


```VB
RegisteredTask.Stop( _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="9ff84-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ff84-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ff84-110">*sinalizadores* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="9ff84-110">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ff84-111">Reservado.</span><span class="sxs-lookup"><span data-stu-id="9ff84-111">Reserved.</span></span> <span data-ttu-id="9ff84-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="9ff84-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ff84-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9ff84-113">Return value</span></span>

<span data-ttu-id="9ff84-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9ff84-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ff84-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ff84-115">Remarks</span></span>

<span data-ttu-id="9ff84-116">A função **RegisteredTask. Stop** interrompe todas as instâncias da tarefa.</span><span class="sxs-lookup"><span data-stu-id="9ff84-116">The **RegisteredTask.Stop** function stops all instances of the task.</span></span>

<span data-ttu-id="9ff84-117">Os usuários da conta do sistema podem interromper uma tarefa, os usuários com privilégios de grupo de administradores podem interromper uma tarefa e, se um usuário tiver direitos para executar e ler uma tarefa, o usuário poderá interromper a tarefa.</span><span class="sxs-lookup"><span data-stu-id="9ff84-117">System account users can stop a task, users with Administrator group privileges can stop a task, and if a user has rights to execute and read a task, then the user can stop the task.</span></span> <span data-ttu-id="9ff84-118">Um usuário pode interromper as instâncias de tarefa que estão sendo executadas com as mesmas credenciais que a conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="9ff84-118">A user can stop the task instances that are running under the same credentials as the user account.</span></span> <span data-ttu-id="9ff84-119">Em todos os outros casos, o acesso ao usuário é negado para interromper a tarefa.</span><span class="sxs-lookup"><span data-stu-id="9ff84-119">In all other cases, the user is denied access to stop the task.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ff84-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ff84-120">Requirements</span></span>



| <span data-ttu-id="9ff84-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ff84-121">Requirement</span></span> | <span data-ttu-id="9ff84-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9ff84-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ff84-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ff84-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9ff84-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9ff84-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9ff84-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ff84-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9ff84-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9ff84-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9ff84-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9ff84-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="9ff84-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9ff84-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9ff84-129">DLL</span><span class="sxs-lookup"><span data-stu-id="9ff84-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ff84-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ff84-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ff84-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ff84-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ff84-132">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="9ff84-132">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





