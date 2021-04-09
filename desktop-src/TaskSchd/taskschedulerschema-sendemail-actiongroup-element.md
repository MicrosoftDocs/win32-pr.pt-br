---
title: Elemento SendEmail (actionGroup)
description: Representa uma ação que envia uma mensagem de email.
ms.assetid: 83416b02-8327-47b3-9dfc-1bf5b9365728
keywords:
- Agendador de Tarefas do elemento SendEmail
topic_type:
- apiref
api_name:
- SendEmail
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81f6f3437521dea2c5cf6e157ad7997718632081
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918901"
---
# <a name="sendemail-actiongroup-element"></a><span data-ttu-id="78dd1-104">Elemento SendEmail (actionGroup)</span><span class="sxs-lookup"><span data-stu-id="78dd1-104">SendEmail (actionGroup) Element</span></span>

<span data-ttu-id="78dd1-105">Representa uma ação que envia uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="78dd1-105">Represents an action that sends an email message.</span></span>

``` syntax
<xs:element name="SendEmail"
    type="sendEmailType"
 />
```

<span data-ttu-id="78dd1-106">O elemento **SendEmail** é definido pelo The [**Action**](taskschedulerschema-actiongroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="78dd1-106">The **SendEmail** element is defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="78dd1-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="78dd1-107">Parent element</span></span>



| <span data-ttu-id="78dd1-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="78dd1-108">Element</span></span>                                                         | <span data-ttu-id="78dd1-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="78dd1-109">Derived from</span></span>                                                       | <span data-ttu-id="78dd1-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="78dd1-110">Description</span></span>                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="78dd1-111">**Ações**</span><span class="sxs-lookup"><span data-stu-id="78dd1-111">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md) | [<span data-ttu-id="78dd1-112">**ActionType**</span><span class="sxs-lookup"><span data-stu-id="78dd1-112">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md) | <span data-ttu-id="78dd1-113">Contém as ações executadas pela tarefa.</span><span class="sxs-lookup"><span data-stu-id="78dd1-113">Contains the actions performed by the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="78dd1-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="78dd1-114">Child elements</span></span>



| <span data-ttu-id="78dd1-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="78dd1-115">Element</span></span>                                                                        | <span data-ttu-id="78dd1-116">Type</span><span class="sxs-lookup"><span data-stu-id="78dd1-116">Type</span></span>                                                                         | <span data-ttu-id="78dd1-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="78dd1-117">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78dd1-118">**Anexos**</span><span class="sxs-lookup"><span data-stu-id="78dd1-118">**Attachments**</span></span>](taskschedulerschema-attachments-sendemailtype-element.md)   | [<span data-ttu-id="78dd1-119">**AttachmentType**</span><span class="sxs-lookup"><span data-stu-id="78dd1-119">**attachmentsType**</span></span>](taskschedulerschema-attachmentstype-complextype.md)   | <span data-ttu-id="78dd1-120">Especifica uma lista de anexos na mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="78dd1-120">Specifies a list of attachments in the email message.</span></span><br/>                                 |
| [<span data-ttu-id="78dd1-121">**Cco**</span><span class="sxs-lookup"><span data-stu-id="78dd1-121">**Bcc**</span></span>](taskschedulerschema-bcc-sendemailtype-element.md)                   | <span data-ttu-id="78dd1-122">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78dd1-122">**string**</span></span>                                                                   | <span data-ttu-id="78dd1-123">Especifica os endereços de email usados na linha Cco de uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="78dd1-123">Specifies the email addresses used on the Bcc line of an email message.</span></span><br/>               |
| [<span data-ttu-id="78dd1-124">**Corpo**</span><span class="sxs-lookup"><span data-stu-id="78dd1-124">**Body**</span></span>](taskschedulerschema-body-sendemailtype-element.md)                 | <span data-ttu-id="78dd1-125">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78dd1-125">**string**</span></span>                                                                   | <span data-ttu-id="78dd1-126">Especifica o texto no corpo da mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="78dd1-126">Specifies the text in the body of the email message.</span></span><br/>                                  |
| [<span data-ttu-id="78dd1-127">**CC**</span><span class="sxs-lookup"><span data-stu-id="78dd1-127">**Cc**</span></span>](taskschedulerschema-cc-sendemailtype-element.md)                     | <span data-ttu-id="78dd1-128">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78dd1-128">**string**</span></span>                                                                   | <span data-ttu-id="78dd1-129">Especifica os endereços de email usados na linha CC de uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="78dd1-129">Specifies the email addresses used on the Cc line of an email message.</span></span><br/>                |
| [<span data-ttu-id="78dd1-130">**De**</span><span class="sxs-lookup"><span data-stu-id="78dd1-130">**From**</span></span>](taskschedulerschema-from-sendemailtype-element.md)                 | <span data-ttu-id="78dd1-131">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78dd1-131">**string**</span></span>                                                                   | <span data-ttu-id="78dd1-132">Especifica o endereço de email do remetente.</span><span class="sxs-lookup"><span data-stu-id="78dd1-132">Specifies the email address of the sender.</span></span><br/>                                            |
| [<span data-ttu-id="78dd1-133">**HeaderFields**</span><span class="sxs-lookup"><span data-stu-id="78dd1-133">**HeaderFields**</span></span>](taskschedulerschema-headerfields-sendemailtype-element.md) | [<span data-ttu-id="78dd1-134">**headerFieldsType**</span><span class="sxs-lookup"><span data-stu-id="78dd1-134">**headerFieldsType**</span></span>](taskschedulerschema-headerfieldstype-complextype.md) | <span data-ttu-id="78dd1-135">Especifica os campos de cabeçalho e seus valores usados no cabeçalho da mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="78dd1-135">Specifies the header fields and their values used in the header of the email message.</span></span><br/> |
| [<span data-ttu-id="78dd1-136">**ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="78dd1-136">**ReplyTo**</span></span>](taskschedulerschema-replyto-sendemailtype-element.md)           | <span data-ttu-id="78dd1-137">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78dd1-137">**string**</span></span>                                                                   | <span data-ttu-id="78dd1-138">Especifica os endereços de email que são respondidos na mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="78dd1-138">Specifies the email addresses that are replied to in the email message.</span></span><br/>               |
| [<span data-ttu-id="78dd1-139">**Servidor**</span><span class="sxs-lookup"><span data-stu-id="78dd1-139">**Server**</span></span>](taskschedulerschema-server-sendemailtype-element.md)             | [<span data-ttu-id="78dd1-140">**não vazio**</span><span class="sxs-lookup"><span data-stu-id="78dd1-140">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)      | <span data-ttu-id="78dd1-141">Especifica o servidor de email usado para enviar a mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="78dd1-141">Specifies the email server used to send the email message.</span></span> <br/>                           |
| [<span data-ttu-id="78dd1-142">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="78dd1-142">**Subject**</span></span>](taskschedulerschema-subject-sendemailtype-element.md)           | <span data-ttu-id="78dd1-143">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78dd1-143">**string**</span></span>                                                                   | <span data-ttu-id="78dd1-144">Especifica o assunto da mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="78dd1-144">Specifies the subject of the email message.</span></span><br/>                                           |
| [<span data-ttu-id="78dd1-145">**Para**</span><span class="sxs-lookup"><span data-stu-id="78dd1-145">**To**</span></span>](taskschedulerschema-to-sendemailtype-element.md)                     | <span data-ttu-id="78dd1-146">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="78dd1-146">**string**</span></span>                                                                   | <span data-ttu-id="78dd1-147">Especifica os endereços de email para os quais o email será enviado.</span><span class="sxs-lookup"><span data-stu-id="78dd1-147">Specifies the email addresses to which the email will be sent.</span></span><br/>                        |



## <a name="remarks"></a><span data-ttu-id="78dd1-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="78dd1-148">Remarks</span></span>

<span data-ttu-id="78dd1-149">Para desenvolvimento em C++, consulte a interface [**IEmailAction**](/windows/win32/api/taskschd/nn-taskschd-iemailaction) .</span><span class="sxs-lookup"><span data-stu-id="78dd1-149">For C++ development, see the [**IEmailAction**](/windows/win32/api/taskschd/nn-taskschd-iemailaction) interface.</span></span>

<span data-ttu-id="78dd1-150">Para o desenvolvimento de script, consulte o objeto [**emailaction**](emailaction.md) .</span><span class="sxs-lookup"><span data-stu-id="78dd1-150">For script development, see the [**EmailAction**](emailaction.md) object.</span></span>

<span data-ttu-id="78dd1-151">**Windows 8 e Windows Server 2012:** Este elemento foi removido.</span><span class="sxs-lookup"><span data-stu-id="78dd1-151">**Windows 8 and Windows Server 2012:** This element has been removed.</span></span> <span data-ttu-id="78dd1-152">Use IExecAction com o cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) do PowerShell como uma solução alternativa.</span><span class="sxs-lookup"><span data-stu-id="78dd1-152">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.</span></span>

## <a name="examples"></a><span data-ttu-id="78dd1-153">Exemplos</span><span class="sxs-lookup"><span data-stu-id="78dd1-153">Examples</span></span>

<span data-ttu-id="78dd1-154">Para obter um exemplo completo do XML para uma tarefa que especifica uma ação de email, consulte [exemplo de gatilho de evento (XML)](/previous-versions//aa446889(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="78dd1-154">For a complete example of the XML for a task that specifies an email action, see [Event Trigger Example (XML)](/previous-versions//aa446889(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="78dd1-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78dd1-155">Requirements</span></span>



| <span data-ttu-id="78dd1-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="78dd1-156">Requirement</span></span> | <span data-ttu-id="78dd1-157">Valor</span><span class="sxs-lookup"><span data-stu-id="78dd1-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="78dd1-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78dd1-158">Minimum supported client</span></span><br/> | <span data-ttu-id="78dd1-159">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="78dd1-159">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="78dd1-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78dd1-160">Minimum supported server</span></span><br/> | <span data-ttu-id="78dd1-161">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="78dd1-161">Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="78dd1-162">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="78dd1-162">End of client support</span></span><br/>    | <span data-ttu-id="78dd1-163">Windows 7</span><span class="sxs-lookup"><span data-stu-id="78dd1-163">Windows 7</span></span><br/>                                 |
| <span data-ttu-id="78dd1-164">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="78dd1-164">End of server support</span></span><br/>    | <span data-ttu-id="78dd1-165">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="78dd1-165">Windows Server 2008 R2</span></span><br/>                    |



 

