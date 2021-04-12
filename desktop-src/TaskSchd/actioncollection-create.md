---
title: Método ActionCollection. Create
description: Para scripts, o cria e adiciona uma nova ação à coleção.
ms.assetid: f33542e1-ee49-4696-b2ab-c48a9b5440d4
keywords:
- Criar Agendador de Tarefas do método
- Criar método Agendador de Tarefas, objeto ActionCollection
- Objeto ActionCollection Agendador de Tarefas, método Create
topic_type:
- apiref
api_name:
- ActionCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50ec2ede228a27e753316860ac44e604d39e2e4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499526"
---
# <a name="actioncollectioncreate-method"></a><span data-ttu-id="cd390-106">Método ActionCollection. Create</span><span class="sxs-lookup"><span data-stu-id="cd390-106">ActionCollection.Create method</span></span>

<span data-ttu-id="cd390-107">Para scripts, o cria e adiciona uma nova ação à coleção.</span><span class="sxs-lookup"><span data-stu-id="cd390-107">For scripting, creates and adds a new action to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd390-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd390-108">Syntax</span></span>


```VB
ActionCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a><span data-ttu-id="cd390-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd390-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd390-110">*tipo* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="cd390-110">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd390-111">Esse parâmetro é definido como uma das constantes de enumeração de [**\_ \_ tipo de ação de tarefa**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) a seguir.</span><span class="sxs-lookup"><span data-stu-id="cd390-111">This parameter is set to one of the following [**TASK\_ACTION\_TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) enumeration constants.</span></span>



| <span data-ttu-id="cd390-112">Valor</span><span class="sxs-lookup"><span data-stu-id="cd390-112">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="cd390-113">Significado</span><span class="sxs-lookup"><span data-stu-id="cd390-113">Meaning</span></span>                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <span data-ttu-id="cd390-114"><dt>**Tarefa \_ do AÇÃO \_ exec**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cd390-114"><dt>**TASK\_ACTION\_EXEC**</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="cd390-115">A ação executa uma operação de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="cd390-115">The action performs a command-line operation.</span></span> <span data-ttu-id="cd390-116">Por exemplo, a ação pode executar um script, iniciar um executável ou, se o nome de um documento for fornecido, localizar seu aplicativo associado e iniciar o aplicativo com o documento.</span><span class="sxs-lookup"><span data-stu-id="cd390-116">For example, the action could run a script, launch an executable, or, if the name of a document is provided, find its associated application and launch the application with the document.</span></span><br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <span data-ttu-id="cd390-117"><dt>**Tarefa \_ do \_ \_ Manipulador com de ação**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="cd390-117"><dt>**TASK\_ACTION\_COM\_HANDLER**</dt> <dt>5</dt></span></span> </dl>    | <span data-ttu-id="cd390-118">A ação dispara um manipulador.</span><span class="sxs-lookup"><span data-stu-id="cd390-118">The action fires a handler.</span></span><br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <span data-ttu-id="cd390-119"><dt>**Tarefa \_ do AÇÃO \_ Enviar \_ email**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="cd390-119"><dt>**TASK\_ACTION\_SEND\_EMAIL**</dt> <dt>6</dt></span></span> </dl>       | <span data-ttu-id="cd390-120">Essa ação envia mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="cd390-120">This action sends email message.</span></span><br/>                                                                                                                                                                                                         |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <span data-ttu-id="cd390-121"><dt>**Tarefa \_ do AÇÃO \_ Mostrar \_ mensagem**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="cd390-121"><dt>**TASK\_ACTION\_SHOW\_MESSAGE**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="cd390-122">Essa ação mostra uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="cd390-122">This action shows a message box.</span></span><br/>                                                                                                                                                                                                         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd390-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cd390-123">Return value</span></span>

<span data-ttu-id="cd390-124">Um objeto de [**ação**](action.md) que representa a nova ação.</span><span class="sxs-lookup"><span data-stu-id="cd390-124">An [**Action**](action.md) object that represents the new action.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd390-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd390-125">Remarks</span></span>

<span data-ttu-id="cd390-126">Você não pode adicionar mais de 32 ações à coleção.</span><span class="sxs-lookup"><span data-stu-id="cd390-126">You cannot add more than 32 actions to the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd390-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd390-127">Requirements</span></span>



| <span data-ttu-id="cd390-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd390-128">Requirement</span></span> | <span data-ttu-id="cd390-129">Valor</span><span class="sxs-lookup"><span data-stu-id="cd390-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd390-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd390-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cd390-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cd390-131">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cd390-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd390-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cd390-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cd390-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cd390-134">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="cd390-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="cd390-135"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cd390-135"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cd390-136">DLL</span><span class="sxs-lookup"><span data-stu-id="cd390-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd390-137"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd390-137"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd390-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd390-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd390-139">**\_tipo de ação da tarefa \_**</span><span class="sxs-lookup"><span data-stu-id="cd390-139">**TASK\_ACTION\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[<span data-ttu-id="cd390-140">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="cd390-140">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="cd390-141">**Açãocollection**</span><span class="sxs-lookup"><span data-stu-id="cd390-141">**ActionCollection**</span></span>](actioncollection.md)
</dt> <dt>

[<span data-ttu-id="cd390-142">**Action**</span><span class="sxs-lookup"><span data-stu-id="cd390-142">**Action**</span></span>](action.md)
</dt> <dt>

[<span data-ttu-id="cd390-143">**Execaction**</span><span class="sxs-lookup"><span data-stu-id="cd390-143">**ExecAction**</span></span>](execaction.md)
</dt> <dt>

[<span data-ttu-id="cd390-144">**Emailaction**</span><span class="sxs-lookup"><span data-stu-id="cd390-144">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="cd390-145">**Permessageaction**</span><span class="sxs-lookup"><span data-stu-id="cd390-145">**ShowMessageAction**</span></span>](showmessageaction.md)
</dt> <dt>

[<span data-ttu-id="cd390-146">**Comhandleaction**</span><span class="sxs-lookup"><span data-stu-id="cd390-146">**ComHandlerAction**</span></span>](comhandleraction.md)
</dt> </dl>

 

 





