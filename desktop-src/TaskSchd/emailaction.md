---
title: Objeto EmailAction
description: Objeto de script que representa uma ação que envia uma mensagem de email.
ms.assetid: edc0dc4d-eda0-47e0-981f-8521ac4678eb
keywords:
- Agendador de Tarefas do objeto emailaction
- Agendador de Tarefas do objeto emailaction, descrito
topic_type:
- apiref
api_name:
- EmailAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a339a1549b76f61499b7192a48edc7c1b86a6c67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824700"
---
# <a name="emailaction-object"></a><span data-ttu-id="9a360-105">Objeto EmailAction</span><span class="sxs-lookup"><span data-stu-id="9a360-105">EmailAction object</span></span>

<span data-ttu-id="9a360-106">\[Não há mais suporte para este objeto.</span><span class="sxs-lookup"><span data-stu-id="9a360-106">\[This object is no longer supported.</span></span> <span data-ttu-id="9a360-107">Use IExecAction com o cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) do PowerShell como uma solução alternativa.\]</span><span class="sxs-lookup"><span data-stu-id="9a360-107">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="9a360-108">Objeto de script que representa uma ação que envia uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="9a360-108">Scripting object that represents an action that sends an email message.</span></span>

## <a name="members"></a><span data-ttu-id="9a360-109">Membros</span><span class="sxs-lookup"><span data-stu-id="9a360-109">Members</span></span>

<span data-ttu-id="9a360-110">O objeto **emailaction** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9a360-110">The **EmailAction** object has these types of members:</span></span>

-   [<span data-ttu-id="9a360-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9a360-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9a360-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9a360-112">Properties</span></span>

<span data-ttu-id="9a360-113">O objeto **emailaction** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9a360-113">The **EmailAction** object has these properties.</span></span>



| <span data-ttu-id="9a360-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="9a360-114">Property</span></span>                                                    | <span data-ttu-id="9a360-115">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="9a360-115">Access type</span></span>           | <span data-ttu-id="9a360-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="9a360-116">Description</span></span>                                                                                               |
|:------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a360-117">**Anexos**</span><span class="sxs-lookup"><span data-stu-id="9a360-117">**Attachments**</span></span>](emailaction-attachments.md)<br/>   | <span data-ttu-id="9a360-118">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9a360-118">Read/write</span></span><br/> | <span data-ttu-id="9a360-119">Obtém ou define uma matriz de anexos que é enviada com a mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="9a360-119">Gets or sets an array of attachments that is sent with the email message.</span></span><br/>                      |
| [<span data-ttu-id="9a360-120">**Cco**</span><span class="sxs-lookup"><span data-stu-id="9a360-120">**Bcc**</span></span>](emailaction-bcc.md)<br/>                   | <span data-ttu-id="9a360-121">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9a360-121">Read/write</span></span><br/> | <span data-ttu-id="9a360-122">Obtém ou define o endereço de email ou endereços que você deseja CCO na mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="9a360-122">Gets or sets the email address or addresses that you want to Bcc in the email message.</span></span><br/>         |
| [<span data-ttu-id="9a360-123">**Corpo**</span><span class="sxs-lookup"><span data-stu-id="9a360-123">**Body**</span></span>](emailaction-body.md)<br/>                 | <span data-ttu-id="9a360-124">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9a360-124">Read/write</span></span><br/> | <span data-ttu-id="9a360-125">Obtém ou define o corpo do email que contém a mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="9a360-125">Gets or sets the body of the email that contains the email message.</span></span><br/>                            |
| [<span data-ttu-id="9a360-126">**CC**</span><span class="sxs-lookup"><span data-stu-id="9a360-126">**Cc**</span></span>](emailaction-cc.md)<br/>                     | <span data-ttu-id="9a360-127">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9a360-127">Read/write</span></span><br/> | <span data-ttu-id="9a360-128">Obtém ou define o endereço de email ou endereços que você deseja CC na mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="9a360-128">Gets or sets the email address or addresses that you want to Cc in the email message.</span></span><br/>          |
| [<span data-ttu-id="9a360-129">**De**</span><span class="sxs-lookup"><span data-stu-id="9a360-129">**From**</span></span>](emailaction-from.md)<br/>                 | <span data-ttu-id="9a360-130">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9a360-130">Read/write</span></span><br/> | <span data-ttu-id="9a360-131">Obtém ou define o endereço de email do qual você deseja enviar o email.</span><span class="sxs-lookup"><span data-stu-id="9a360-131">Gets or sets the email address that you want to send the email from.</span></span><br/>                           |
| [<span data-ttu-id="9a360-132">**HeaderFields**</span><span class="sxs-lookup"><span data-stu-id="9a360-132">**HeaderFields**</span></span>](emailaction-headerfields.md)<br/> | <span data-ttu-id="9a360-133">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9a360-133">Read/write</span></span><br/> | <span data-ttu-id="9a360-134">Obtém ou define as informações de cabeçalho no email que você deseja enviar.</span><span class="sxs-lookup"><span data-stu-id="9a360-134">Gets or sets the header information in the email that you want to send.</span></span><br/>                        |
| [<span data-ttu-id="9a360-135">**Sessão**</span><span class="sxs-lookup"><span data-stu-id="9a360-135">**Id**</span></span>](action-id.md)<br/>                          | <span data-ttu-id="9a360-136">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9a360-136">Read/write</span></span><br/> | <span data-ttu-id="9a360-137">Herdado do objeto de [**ação**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="9a360-137">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="9a360-138">Obtém ou define o identificador da ação.</span><span class="sxs-lookup"><span data-stu-id="9a360-138">Gets or sets the identifier of the action.</span></span><br/> |
| [<span data-ttu-id="9a360-139">**ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="9a360-139">**ReplyTo**</span></span>](emailaction-replyto.md)<br/>           | <span data-ttu-id="9a360-140">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9a360-140">Read/write</span></span><br/> | <span data-ttu-id="9a360-141">Obtém ou define o endereço de email ao qual você deseja responder.</span><span class="sxs-lookup"><span data-stu-id="9a360-141">Gets or sets the email address that you want to reply to.</span></span><br/>                                      |
| [<span data-ttu-id="9a360-142">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="9a360-142">**Server**</span></span>](emailaction-server.md)<br/>             | <span data-ttu-id="9a360-143">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9a360-143">Read/write</span></span><br/> | <span data-ttu-id="9a360-144">Obtém ou define o nome do servidor que você usa para enviar email.</span><span class="sxs-lookup"><span data-stu-id="9a360-144">Gets or sets the name of the server that you use to send email from.</span></span><br/>                           |
| [<span data-ttu-id="9a360-145">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="9a360-145">**Subject**</span></span>](emailaction-subject.md)<br/>           | <span data-ttu-id="9a360-146">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9a360-146">Read/write</span></span><br/> | <span data-ttu-id="9a360-147">Obtém ou define o assunto da mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="9a360-147">Gets or sets the subject of the email message.</span></span><br/>                                                 |
| [<span data-ttu-id="9a360-148">**Para**</span><span class="sxs-lookup"><span data-stu-id="9a360-148">**To**</span></span>](emailaction-to.md)<br/>                     | <span data-ttu-id="9a360-149">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9a360-149">Read/write</span></span><br/> | <span data-ttu-id="9a360-150">Obtém ou define o endereço de email ou endereços para os quais você deseja enviar o email.</span><span class="sxs-lookup"><span data-stu-id="9a360-150">Gets or sets the email address or addresses that you want to send the email to.</span></span><br/>                |
| [<span data-ttu-id="9a360-151">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9a360-151">**Type**</span></span>](/windows/win32/api/taskschd/nf-taskschd-iaction-get_type)<br/>                     | <span data-ttu-id="9a360-152">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9a360-152">Read-only</span></span><br/>  | <span data-ttu-id="9a360-153">Herdado do objeto [**Action**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="9a360-153">Inherited from [**Action**](action.md) object.</span></span> <span data-ttu-id="9a360-154">Obtém o tipo da ação.</span><span class="sxs-lookup"><span data-stu-id="9a360-154">Gets the type of the action.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="9a360-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a360-155">Remarks</span></span>

<span data-ttu-id="9a360-156">A ação de email deve ter um valor válido para as propriedades [**servidor**](emailaction-server.md), [**de**](emailaction-from.md)e [**para**](emailaction-to.md) ou [**CC**](emailaction-cc.md) para que a tarefa seja registrada e executada corretamente.</span><span class="sxs-lookup"><span data-stu-id="9a360-156">The email action must have a valid value for the [**Server**](emailaction-server.md), [**From**](emailaction-from.md), and [**To**](emailaction-to.md) or [**Cc**](emailaction-cc.md) properties for the task to register and run correctly.</span></span>

<span data-ttu-id="9a360-157">Ao ler ou gravar seu próprio XML para uma tarefa, uma ação de email é especificada usando o elemento [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="9a360-157">When reading or writing your own XML for a task, an email action is specified using the [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="9a360-158">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9a360-158">Examples</span></span>

<span data-ttu-id="9a360-159">Para obter mais informações e código de exemplo para esse objeto de script, consulte [exemplo de gatilho de evento (script)](/previous-versions//aa446887(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9a360-159">For more information and example code for this scripting object, see [Event Trigger Example (Scripting)](/previous-versions//aa446887(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="9a360-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a360-160">Requirements</span></span>



| <span data-ttu-id="9a360-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a360-161">Requirement</span></span> | <span data-ttu-id="9a360-162">Valor</span><span class="sxs-lookup"><span data-stu-id="9a360-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a360-163">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a360-163">Minimum supported client</span></span><br/> | <span data-ttu-id="9a360-164">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9a360-164">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9a360-165">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a360-165">Minimum supported server</span></span><br/> | <span data-ttu-id="9a360-166">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9a360-166">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9a360-167">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="9a360-167">End of client support</span></span><br/>    | <span data-ttu-id="9a360-168">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9a360-168">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="9a360-169">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="9a360-169">End of server support</span></span><br/>    | <span data-ttu-id="9a360-170">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9a360-170">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="9a360-171">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9a360-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="9a360-172"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9a360-172"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9a360-173">DLL</span><span class="sxs-lookup"><span data-stu-id="9a360-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a360-174"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a360-174"><dt>Taskschd.dll</dt></span></span> </dl> |



 

