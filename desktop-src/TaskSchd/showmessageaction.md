---
title: Objeto exmessageaction
description: Para scripts, representa uma ação que mostra uma caixa de mensagem quando uma tarefa é ativada.
ms.assetid: fdd22eef-965c-4a81-954c-66011c435ab9
keywords:
- Agendador de Tarefas de objeto do exmessageaction
- Agendador de Tarefas do objeto exmessageaction, descrito
topic_type:
- apiref
api_name:
- ShowMessageAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1e500f0492ad010e88719a467fda38f85e184c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369402"
---
# <a name="showmessageaction-object"></a><span data-ttu-id="b57cf-105">Objeto exmessageaction</span><span class="sxs-lookup"><span data-stu-id="b57cf-105">ShowMessageAction object</span></span>

<span data-ttu-id="b57cf-106">\[Não há mais suporte para este objeto.</span><span class="sxs-lookup"><span data-stu-id="b57cf-106">\[This object is no longer supported.</span></span> <span data-ttu-id="b57cf-107">Você pode usar o IExecAction com a função script do Windows [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) para mostrar uma mensagem na sessão do usuário.\]</span><span class="sxs-lookup"><span data-stu-id="b57cf-107">You can use IExecAction with the Windows scripting [**MsgBox function**](/previous-versions/sfw6660x(v=vs.80)) to show a message in the user session.\]</span></span>

<span data-ttu-id="b57cf-108">Para scripts, representa uma ação que mostra uma caixa de mensagem quando uma tarefa é ativada.</span><span class="sxs-lookup"><span data-stu-id="b57cf-108">For scripting, represents an action that shows a message box when a task is activated.</span></span>

## <a name="members"></a><span data-ttu-id="b57cf-109">Membros</span><span class="sxs-lookup"><span data-stu-id="b57cf-109">Members</span></span>

<span data-ttu-id="b57cf-110">O objeto **Exmessageaction** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b57cf-110">The **ShowMessageAction** object has these types of members:</span></span>

-   [<span data-ttu-id="b57cf-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b57cf-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b57cf-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b57cf-112">Properties</span></span>

<span data-ttu-id="b57cf-113">O objeto **Exmessageaction** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b57cf-113">The **ShowMessageAction** object has these properties.</span></span>



| <span data-ttu-id="b57cf-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="b57cf-114">Property</span></span>                                                        | <span data-ttu-id="b57cf-115">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="b57cf-115">Access type</span></span>           | <span data-ttu-id="b57cf-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="b57cf-116">Description</span></span>                                                                                               |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b57cf-117">**Sessão**</span><span class="sxs-lookup"><span data-stu-id="b57cf-117">**Id**</span></span>](action-id.md)<br/>                              | <span data-ttu-id="b57cf-118">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b57cf-118">Read/write</span></span><br/> | <span data-ttu-id="b57cf-119">Herdado do objeto de [**ação**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="b57cf-119">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="b57cf-120">Obtém ou define o identificador da ação.</span><span class="sxs-lookup"><span data-stu-id="b57cf-120">Gets or sets the identifier of the action.</span></span><br/> |
| [<span data-ttu-id="b57cf-121">**MessageBody**</span><span class="sxs-lookup"><span data-stu-id="b57cf-121">**MessageBody**</span></span>](showmessageaction-messagebody.md)<br/> | <span data-ttu-id="b57cf-122">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b57cf-122">Read/write</span></span><br/> | <span data-ttu-id="b57cf-123">Obtém ou define o texto da mensagem que é exibido no corpo da caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="b57cf-123">Gets or sets the message text that is displayed in the body of the message box.</span></span><br/>                |
| [<span data-ttu-id="b57cf-124">**Título**</span><span class="sxs-lookup"><span data-stu-id="b57cf-124">**Title**</span></span>](showmessageaction-title.md)<br/>             | <span data-ttu-id="b57cf-125">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b57cf-125">Read/write</span></span><br/> | <span data-ttu-id="b57cf-126">Obtém ou define o título da caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="b57cf-126">Gets or sets the title of the message box.</span></span><br/>                                                     |
| [<span data-ttu-id="b57cf-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b57cf-127">**Type**</span></span>](action-type.md)<br/>                          | <span data-ttu-id="b57cf-128">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b57cf-128">Read-only</span></span><br/>  | <span data-ttu-id="b57cf-129">Herdado do objeto de [**ação**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="b57cf-129">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="b57cf-130">Obtém o tipo da ação.</span><span class="sxs-lookup"><span data-stu-id="b57cf-130">Gets the type of the action.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="b57cf-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="b57cf-131">Remarks</span></span>

<span data-ttu-id="b57cf-132">Para uma tarefa que contém uma ação de caixa de mensagem, a caixa de mensagem será exibida se a tarefa for ativada e a tarefa tiver um tipo de logon interativo.</span><span class="sxs-lookup"><span data-stu-id="b57cf-132">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="b57cf-133">Para definir o tipo de logon da tarefa como interativo, especifique 3 (**\_ \_ \_ token interativo de logon da tarefa**) ou 4 (**\_ \_ grupo de logon de tarefa**) na propriedade [**Logontype**](principal-logontype.md) da entidade de segurança da tarefa ou no parâmetro *Logontype* de [**TaskFolder. RegisterTask**](taskfolder-registertask.md) ou [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="b57cf-133">To set the task logon type to interactive, specify 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) or 4 (**TASK\_LOGON\_GROUP**) in the [**LogonType**](principal-logontype.md) property of the task principal, or in the *logonType* parameter of [**TaskFolder.RegisterTask**](taskfolder-registertask.md) or [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span></span>

<span data-ttu-id="b57cf-134">Ao ler ou gravar seu próprio XML para uma tarefa, uma ação da caixa de mensagem é especificada usando o elemento [**exmessage**](taskschedulerschema-showmessage-actiongroup-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="b57cf-134">When reading or writing your own XML for a task, a message box action is specified using the [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="b57cf-135">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b57cf-135">Examples</span></span>

<span data-ttu-id="b57cf-136">Para obter mais informações e código de exemplo para esse objeto de script, consulte o [exemplo de caixa de mensagem (script)](/previous-versions//aa381916(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b57cf-136">For more information and example code for this scripting object, see [Message Box Example (Scripting)](/previous-versions//aa381916(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="b57cf-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b57cf-137">Requirements</span></span>



| <span data-ttu-id="b57cf-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="b57cf-138">Requirement</span></span> | <span data-ttu-id="b57cf-139">Valor</span><span class="sxs-lookup"><span data-stu-id="b57cf-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b57cf-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b57cf-140">Minimum supported client</span></span><br/> | <span data-ttu-id="b57cf-141">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b57cf-141">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b57cf-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b57cf-142">Minimum supported server</span></span><br/> | <span data-ttu-id="b57cf-143">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b57cf-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b57cf-144">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b57cf-144">End of client support</span></span><br/>    | <span data-ttu-id="b57cf-145">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b57cf-145">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="b57cf-146">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="b57cf-146">End of server support</span></span><br/>    | <span data-ttu-id="b57cf-147">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b57cf-147">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="b57cf-148">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b57cf-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="b57cf-149"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b57cf-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b57cf-150">DLL</span><span class="sxs-lookup"><span data-stu-id="b57cf-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b57cf-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b57cf-151"><dt>Taskschd.dll</dt></span></span> </dl> |



 

