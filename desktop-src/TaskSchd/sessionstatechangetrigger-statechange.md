---
title: Propriedade SessionStateChangeTrigger. StateChange
description: Para scripts, Obtém ou define o tipo de Terminal Server alteração de sessão que dispararia um lançamento de tarefa.
ms.assetid: ae1460c7-2939-4fcb-b7fc-edc859596bc4
keywords:
- Agendador de Tarefas da propriedade StateChange
- Propriedade StateChange Agendador de Tarefas, objeto SessionStateChangeTrigger
- Objeto SessionStateChangeTrigger Agendador de Tarefas, Propriedade StateChange
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger.StateChange
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac4be561482917788f6afb9b8eb7394cdcce7985
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644428"
---
# <a name="sessionstatechangetriggerstatechange-property"></a><span data-ttu-id="b13a0-106">Propriedade SessionStateChangeTrigger. StateChange</span><span class="sxs-lookup"><span data-stu-id="b13a0-106">SessionStateChangeTrigger.StateChange property</span></span>

<span data-ttu-id="b13a0-107">Para scripts, Obtém ou define o tipo de Terminal Server alteração de sessão que dispararia um lançamento de tarefa.</span><span class="sxs-lookup"><span data-stu-id="b13a0-107">For scripting, gets or sets the kind of Terminal Server session change that would trigger a task launch.</span></span>

## <a name="syntax"></a><span data-ttu-id="b13a0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b13a0-108">Syntax</span></span>


```VB
SessionStateChangeTrigger.StateChange As Integer
```



## <a name="property-value"></a><span data-ttu-id="b13a0-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b13a0-109">Property value</span></span>

<span data-ttu-id="b13a0-110">O tipo de Terminal Server alteração de sessão que dispara uma tarefa a ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="b13a0-110">The kind of Terminal Server session change that triggers a task to launch.</span></span>

<span data-ttu-id="b13a0-111">Os valores possíveis são da enumeração [**de \_ \_ tipo de \_ alteração \_ de estado de sessão de tarefa**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) .</span><span class="sxs-lookup"><span data-stu-id="b13a0-111">The possible values are from the [**TASK\_SESSION\_STATE\_CHANGE\_TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) enumeration.</span></span>



| <span data-ttu-id="b13a0-112">Valor</span><span class="sxs-lookup"><span data-stu-id="b13a0-112">Value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="b13a0-113">Significado</span><span class="sxs-lookup"><span data-stu-id="b13a0-113">Meaning</span></span>                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_CONSOLE_CONNECT"></span><span id="task_console_connect"></span><dl> <span data-ttu-id="b13a0-114"><dt>**Tarefa \_ do CONSOLE \_ Connect**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b13a0-114"><dt>**TASK\_CONSOLE\_CONNECT**</dt> <dt>1</dt></span></span> </dl>          | <span data-ttu-id="b13a0-115">Terminal Server alteração de estado da conexão do console.</span><span class="sxs-lookup"><span data-stu-id="b13a0-115">Terminal Server console connection state change.</span></span> <span data-ttu-id="b13a0-116">Por exemplo, quando você se conecta a uma sessão de usuário no computador local, alternando os usuários no computador.</span><span class="sxs-lookup"><span data-stu-id="b13a0-116">For example, when you connect to a user session on the local computer by switching users on the computer.</span></span> <br/>                           |
| <span id="TASK_CONSOLE_DISCONNECT"></span><span id="task_console_disconnect"></span><dl> <span data-ttu-id="b13a0-117"><dt>**Tarefa \_ do \_Desconexão do console**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b13a0-117"><dt>**TASK\_CONSOLE\_DISCONNECT**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="b13a0-118">Alteração do estado de desconexão do Console Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="b13a0-118">Terminal Server console disconnection state change.</span></span> <span data-ttu-id="b13a0-119">Por exemplo, quando você se desconecta a uma sessão de usuário no computador local, alternando os usuários no computador.</span><span class="sxs-lookup"><span data-stu-id="b13a0-119">For example, when you disconnect to a user session on the local computer by switching users on the computer.</span></span><br/>                      |
| <span id="TASK_REMOTE_CONNECT"></span><span id="task_remote_connect"></span><dl> <span data-ttu-id="b13a0-120"><dt>**Tarefa \_ do \_Conexão remota**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b13a0-120"><dt>**TASK\_REMOTE\_CONNECT**</dt> <dt>3</dt></span></span> </dl>             | <span data-ttu-id="b13a0-121">Terminal Server alteração de estado da conexão remota.</span><span class="sxs-lookup"><span data-stu-id="b13a0-121">Terminal Server remote connection state change.</span></span> <span data-ttu-id="b13a0-122">Por exemplo, quando um usuário se conecta a uma sessão de usuário usando o programa Conexão de Área de Trabalho Remota de um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="b13a0-122">For example, when a user connects to a user session by using the Remote Desktop Connection program from a remote computer.</span></span><br/>            |
| <span id="TASK_REMOTE_DISCONNECT"></span><span id="task_remote_disconnect"></span><dl> <span data-ttu-id="b13a0-123"><dt>**Tarefa \_ do \_Desconexão remota**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b13a0-123"><dt>**TASK\_REMOTE\_DISCONNECT**</dt> <dt>4</dt></span></span> </dl>    | <span data-ttu-id="b13a0-124">Terminal Server alteração de estado de desconexão remota.</span><span class="sxs-lookup"><span data-stu-id="b13a0-124">Terminal Server remote disconnection state change.</span></span> <span data-ttu-id="b13a0-125">Por exemplo, quando um usuário se desconecta de uma sessão de usuário enquanto usa o programa de Conexão de Área de Trabalho Remota de um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="b13a0-125">For example, when a user disconnects from a user session while using the Remote Desktop Connection program from a remote computer.</span></span><br/> |
| <span id="TASK_SESSION_LOCK"></span><span id="task_session_lock"></span><dl> <span data-ttu-id="b13a0-126"><dt>**Tarefa \_ do \_Bloqueio de sessão**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="b13a0-126"><dt>**TASK\_SESSION\_LOCK**</dt> <dt>7</dt></span></span> </dl>                   | <span data-ttu-id="b13a0-127">Alteração de estado bloqueado da sessão de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="b13a0-127">Terminal Server session locked state change.</span></span> <span data-ttu-id="b13a0-128">Por exemplo, essa alteração de estado faz com que a tarefa seja executada quando o computador é bloqueado.</span><span class="sxs-lookup"><span data-stu-id="b13a0-128">For example, this state change causes the task to run when the computer is locked.</span></span> <br/>                                                      |
| <span id="TASK_SESSION_UNLOCK"></span><span id="task_session_unlock"></span><dl> <span data-ttu-id="b13a0-129"><dt>**Tarefa \_ do \_Desbloqueio de sessão**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="b13a0-129"><dt>**TASK\_SESSION\_UNLOCK**</dt> <dt>8</dt></span></span> </dl>             | <span data-ttu-id="b13a0-130">Alteração de estado desbloqueado da sessão de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="b13a0-130">Terminal Server session unlocked state change.</span></span> <span data-ttu-id="b13a0-131">Por exemplo, essa alteração de estado faz com que a tarefa seja executada quando o computador é desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="b13a0-131">For example, this state change causes the task to run when the computer is unlocked.</span></span><br/>                                                   |



 

## <a name="requirements"></a><span data-ttu-id="b13a0-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b13a0-132">Requirements</span></span>



| <span data-ttu-id="b13a0-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b13a0-133">Requirement</span></span> | <span data-ttu-id="b13a0-134">Valor</span><span class="sxs-lookup"><span data-stu-id="b13a0-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b13a0-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b13a0-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b13a0-136">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b13a0-136">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b13a0-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b13a0-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b13a0-138">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b13a0-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b13a0-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b13a0-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="b13a0-140"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b13a0-140"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b13a0-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b13a0-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b13a0-142"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b13a0-142"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





