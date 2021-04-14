---
title: Propriedade EventTrigger. ValueQueries
description: Para scripts, Obtém ou define uma coleção de consultas XPath nomeadas. Cada consulta na coleção é aplicada ao último XML de evento de correspondência que é retornado da consulta de assinatura especificada na propriedade de assinatura.
ms.assetid: 9ff92b66-f63c-4736-b086-df7dd8cd2b10
keywords:
- Agendador de Tarefas da propriedade ValueQueries
- Propriedade ValueQueries Agendador de Tarefas, objeto EventTrigger
- Objeto EventTrigger Agendador de Tarefas, Propriedade ValueQueries
topic_type:
- apiref
api_name:
- EventTrigger.ValueQueries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd2061f9d910e67855cc0dcb6d64248067fcb9e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499618"
---
# <a name="eventtriggervaluequeries-property"></a><span data-ttu-id="77a83-107">Propriedade EventTrigger. ValueQueries</span><span class="sxs-lookup"><span data-stu-id="77a83-107">EventTrigger.ValueQueries property</span></span>

<span data-ttu-id="77a83-108">Para scripts, Obtém ou define uma coleção de consultas XPath nomeadas.</span><span class="sxs-lookup"><span data-stu-id="77a83-108">For scripting, gets or sets a collection of named XPath queries.</span></span> <span data-ttu-id="77a83-109">Cada consulta na coleção é aplicada ao último XML de evento de correspondência que é retornado da consulta de assinatura especificada na propriedade de [**assinatura**](eventtrigger-subscription.md) .</span><span class="sxs-lookup"><span data-stu-id="77a83-109">Each query in the collection is applied to the last matching event XML that is returned from the subscription query specified in the [**Subscription**](eventtrigger-subscription.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="77a83-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="77a83-110">Syntax</span></span>


```VB
EventTrigger.ValueQueries As String
```



## <a name="property-value"></a><span data-ttu-id="77a83-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="77a83-111">Property value</span></span>

<span data-ttu-id="77a83-112">Uma coleção de pares nome-valor.</span><span class="sxs-lookup"><span data-stu-id="77a83-112">A collection of of name-value pairs.</span></span> <span data-ttu-id="77a83-113">Cada par de nome-valor na coleção define um nome exclusivo para um valor de Propriedade do evento que dispara o gatilho de evento.</span><span class="sxs-lookup"><span data-stu-id="77a83-113">Each name-value pair in the collection defines a unique name for a property value of the event that triggers the event trigger.</span></span> <span data-ttu-id="77a83-114">O valor da Propriedade do evento é definido como uma consulta de evento XPath.</span><span class="sxs-lookup"><span data-stu-id="77a83-114">The property value of the event is defined as an XPath event query.</span></span> <span data-ttu-id="77a83-115">Para obter mais informações sobre consultas de eventos XPath, consulte [seleção de eventos](/previous-versions//aa385231(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="77a83-115">For more information about XPath event queries, see [Event Selection](/previous-versions//aa385231(v=vs.85)).</span></span>

## <a name="remarks"></a><span data-ttu-id="77a83-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="77a83-116">Remarks</span></span>

<span data-ttu-id="77a83-117">O nome da consulta pode ser usado como uma variável nas seguintes propriedades de ação:</span><span class="sxs-lookup"><span data-stu-id="77a83-117">The name of the query can be used as a variable in the following action properties:</span></span>

-   [<span data-ttu-id="77a83-118">**MessageBody.**</span><span class="sxs-lookup"><span data-stu-id="77a83-118">**ShowMessageAction.MessageBody**</span></span>](showmessageaction-messagebody.md)
-   [<span data-ttu-id="77a83-119">**Nome da mensagem. title**</span><span class="sxs-lookup"><span data-stu-id="77a83-119">**ShowMessageAction.Title**</span></span>](showmessageaction-title.md)
-   [<span data-ttu-id="77a83-120">**Argumentos execaction.**</span><span class="sxs-lookup"><span data-stu-id="77a83-120">**ExecAction.Arguments**</span></span>](execaction-arguments.md)
-   [<span data-ttu-id="77a83-121">**Execaction. WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="77a83-121">**ExecAction.WorkingDirectory**</span></span>](execaction-workingdirectory.md)
-   [<span data-ttu-id="77a83-122">**Emailaction. Server**</span><span class="sxs-lookup"><span data-stu-id="77a83-122">**EmailAction.Server**</span></span>](emailaction-server.md)
-   [<span data-ttu-id="77a83-123">**Emailaction. Subject**</span><span class="sxs-lookup"><span data-stu-id="77a83-123">**EmailAction.Subject**</span></span>](emailaction-subject.md)
-   [<span data-ttu-id="77a83-124">**EmailAction.To**</span><span class="sxs-lookup"><span data-stu-id="77a83-124">**EmailAction.To**</span></span>](emailaction-to.md)
-   [<span data-ttu-id="77a83-125">**EmailAction.Cc**</span><span class="sxs-lookup"><span data-stu-id="77a83-125">**EmailAction.Cc**</span></span>](emailaction-cc.md)
-   [<span data-ttu-id="77a83-126">**Emailaction. Bcc**</span><span class="sxs-lookup"><span data-stu-id="77a83-126">**EmailAction.Bcc**</span></span>](emailaction-bcc.md)
-   [<span data-ttu-id="77a83-127">**Emailaction. ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="77a83-127">**EmailAction.ReplyTo**</span></span>](emailaction-replyto.md)
-   [<span data-ttu-id="77a83-128">**Emailaction. from**</span><span class="sxs-lookup"><span data-stu-id="77a83-128">**EmailAction.From**</span></span>](emailaction-from.md)
-   [<span data-ttu-id="77a83-129">**Emailaction. Body**</span><span class="sxs-lookup"><span data-stu-id="77a83-129">**EmailAction.Body**</span></span>](emailaction-body.md)
-   [<span data-ttu-id="77a83-130">**Comhandleaction. Data**</span><span class="sxs-lookup"><span data-stu-id="77a83-130">**ComHandlerAction.Data**</span></span>](comhandleraction-data.md)

<span data-ttu-id="77a83-131">As cadeias de caracteres de exemplo de código a seguir mostram dois pares de valor de nome que podem ser usados em uma coleção de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="77a83-131">The following code example strings show two name value pairs that can be used in a name-value collection.</span></span> <span data-ttu-id="77a83-132">Os valores retornados pelas consultas XPath podem substituir variáveis na propriedade de uma ação.</span><span class="sxs-lookup"><span data-stu-id="77a83-132">The values returned by the XPath queries can replace variables in an action's property.</span></span> <span data-ttu-id="77a83-133">Os valores são referenciados pelo nome, com `$(user)` e `$(machine)` , na propriedade Action.</span><span class="sxs-lookup"><span data-stu-id="77a83-133">The values are referenced by name, with `$(user)` and `$(machine)`, in the action property.</span></span> <span data-ttu-id="77a83-134">Por exemplo, se as `$(user)` `$(machine)` variáveis e forem usadas na cadeia de caracteres [**. MessageBody**](showmessageaction-messagebody.md) , o valor das consultas XPath substituirá as variáveis na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="77a83-134">For example, if the `$(user)` and `$(machine)` variables are used in the [**ShowMessageAction.MessageBody**](showmessageaction-messagebody.md) string, then the value of the XPath queries will replace the variables in the string.</span></span>

``` syntax
name: user
value: Event/UserData/SubjectUserName

name: machine
value: Event/UserData/MachineName
```

<span data-ttu-id="77a83-135">Para obter mais informações sobre como gravar uma cadeia de caracteres de consulta para determinados eventos, consulte [seleção de eventos](/previous-versions//aa385231(v=vs.85)) e [assinatura de eventos](../wes/subscribing-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="77a83-135">For more information about writing a query string for certain events, see [Event Selection](/previous-versions//aa385231(v=vs.85)) and [Subscribing to Events](../wes/subscribing-to-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="77a83-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77a83-136">Requirements</span></span>



| <span data-ttu-id="77a83-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="77a83-137">Requirement</span></span> | <span data-ttu-id="77a83-138">Valor</span><span class="sxs-lookup"><span data-stu-id="77a83-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77a83-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77a83-139">Minimum supported client</span></span><br/> | <span data-ttu-id="77a83-140">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77a83-140">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="77a83-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77a83-141">Minimum supported server</span></span><br/> | <span data-ttu-id="77a83-142">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="77a83-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="77a83-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="77a83-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="77a83-144"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="77a83-144"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="77a83-145">DLL</span><span class="sxs-lookup"><span data-stu-id="77a83-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77a83-146"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77a83-146"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77a83-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="77a83-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77a83-148">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="77a83-148">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="77a83-149">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="77a83-149">**EventTrigger**</span></span>](eventtrigger.md)
</dt> </dl>

 

