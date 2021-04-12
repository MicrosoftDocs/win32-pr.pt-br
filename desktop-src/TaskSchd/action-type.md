---
title: Propriedade Action. Type
description: Para scripts, obtém o tipo da ação.
ms.assetid: 6a0bca3d-9016-4167-9f6e-2cc95bafdb95
keywords:
- Agendador de Tarefas de propriedade de tipo
- Agendador de Tarefas de propriedade de tipo, objeto de ação
- Agendador de Tarefas de objeto de ação, Propriedade Type
topic_type:
- apiref
api_name:
- Action.Type
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3db8ca46a80503136c5fbbe1240cba6c664bc1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455511"
---
# <a name="actiontype-property"></a><span data-ttu-id="4d3a8-106">Propriedade Action. Type</span><span class="sxs-lookup"><span data-stu-id="4d3a8-106">Action.Type property</span></span>

<span data-ttu-id="4d3a8-107">Para scripts, obtém o tipo da ação.</span><span class="sxs-lookup"><span data-stu-id="4d3a8-107">For scripting, gets the type of the action.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d3a8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d3a8-108">Syntax</span></span>


```VB
Action.Type As Integer
```



## <a name="property-value"></a><span data-ttu-id="4d3a8-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4d3a8-109">Property value</span></span>

<span data-ttu-id="4d3a8-110">Essa propriedade retorna uma das constantes de enumeração de [**\_ \_ tipo de ação de tarefa**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) a seguir.</span><span class="sxs-lookup"><span data-stu-id="4d3a8-110">This property returns one of the following [**TASK\_ACTION\_TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) enumeration constants.</span></span>



| <span data-ttu-id="4d3a8-111">Valor</span><span class="sxs-lookup"><span data-stu-id="4d3a8-111">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="4d3a8-112">Significado</span><span class="sxs-lookup"><span data-stu-id="4d3a8-112">Meaning</span></span>                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <span data-ttu-id="4d3a8-113"><dt>**Tarefa \_ do AÇÃO \_ exec**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4d3a8-113"><dt>**TASK\_ACTION\_EXEC**</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="4d3a8-114">Essa ação executa uma operação de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="4d3a8-114">This action performs a command-line operation.</span></span> <span data-ttu-id="4d3a8-115">Por exemplo, a ação pode executar um script, iniciar um executável ou, se o nome de um documento for fornecido, localizar seu aplicativo associado e iniciar o aplicativo com o documento.</span><span class="sxs-lookup"><span data-stu-id="4d3a8-115">For example, the action could run a script, launch an executable, or, if the name of a document is provided, find its associated application and launch the application with the document.</span></span><br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <span data-ttu-id="4d3a8-116"><dt>**Tarefa \_ do \_ \_ Manipulador com de ação**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="4d3a8-116"><dt>**TASK\_ACTION\_COM\_HANDLER**</dt> <dt>5</dt></span></span> </dl>    | <span data-ttu-id="4d3a8-117">Essa ação dispara um manipulador.</span><span class="sxs-lookup"><span data-stu-id="4d3a8-117">This action fires a handler.</span></span><br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <span data-ttu-id="4d3a8-118"><dt>**Tarefa \_ do AÇÃO \_ Enviar \_ email**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="4d3a8-118"><dt>**TASK\_ACTION\_SEND\_EMAIL**</dt> <dt>6</dt></span></span> </dl>       | <span data-ttu-id="4d3a8-119">Essa ação envia uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="4d3a8-119">This action sends an email message.</span></span><br/>                                                                                                                                                                                                       |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <span data-ttu-id="4d3a8-120"><dt>**Tarefa \_ do AÇÃO \_ Mostrar \_ mensagem**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="4d3a8-120"><dt>**TASK\_ACTION\_SHOW\_MESSAGE**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="4d3a8-121">Essa ação mostra uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="4d3a8-121">This action shows a message box.</span></span><br/>                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="4d3a8-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d3a8-122">Remarks</span></span>

<span data-ttu-id="4d3a8-123">O tipo de ação é definido quando a ação é criada e não pode ser alterada posteriormente.</span><span class="sxs-lookup"><span data-stu-id="4d3a8-123">The action type is defined when the action is created and cannot be changed later.</span></span> <span data-ttu-id="4d3a8-124">Para obter informações sobre como criar uma ação, consulte [**ActionCollection. Create**](actioncollection-create.md).</span><span class="sxs-lookup"><span data-stu-id="4d3a8-124">For information on creating an action, see [**ActionCollection.Create**](actioncollection-create.md).</span></span>

<span data-ttu-id="4d3a8-125">Para obter informações sobre como as ações e tarefas funcionam em conjunto, consulte [ações da tarefa](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="4d3a8-125">For information on how actions and tasks work together, see [Task Actions](task-actions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d3a8-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d3a8-126">Requirements</span></span>



| <span data-ttu-id="4d3a8-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d3a8-127">Requirement</span></span> | <span data-ttu-id="4d3a8-128">Valor</span><span class="sxs-lookup"><span data-stu-id="4d3a8-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d3a8-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d3a8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4d3a8-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4d3a8-130">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4d3a8-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d3a8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4d3a8-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4d3a8-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4d3a8-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4d3a8-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="4d3a8-134"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4d3a8-134"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4d3a8-135">DLL</span><span class="sxs-lookup"><span data-stu-id="4d3a8-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d3a8-136"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d3a8-136"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d3a8-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d3a8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d3a8-138">**\_tipo de ação da tarefa \_**</span><span class="sxs-lookup"><span data-stu-id="4d3a8-138">**TASK\_ACTION\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[<span data-ttu-id="4d3a8-139">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="4d3a8-139">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="4d3a8-140">**Ação**</span><span class="sxs-lookup"><span data-stu-id="4d3a8-140">**Action**</span></span>](action.md)
</dt> </dl>

 

 





