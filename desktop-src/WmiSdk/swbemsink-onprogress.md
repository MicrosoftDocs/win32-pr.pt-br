---
description: O evento OnProgress de SWbemSink é disparado quando uma chamada assíncrona retorna o status de uma chamada em andamento.
ms.assetid: abb43916-f952-41fe-a5ba-0428864c0685
ms.tgt_platform: multiple
title: 'Evento ISWbemSinkEvents:: OnProgress (Wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnProgress
- ISWbemSinkEvents.OnProgress
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0d322309adcfad33b1c303d7efd6af28db1cac80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787656"
---
# <a name="iswbemsinkeventsonprogress-event"></a><span data-ttu-id="66de0-103">Evento ISWbemSinkEvents:: OnProgress</span><span class="sxs-lookup"><span data-stu-id="66de0-103">ISWbemSinkEvents::OnProgress event</span></span>

<span data-ttu-id="66de0-104">O evento **OnProgress** de [**SWbemSink**](swbemsink.md) é disparado quando uma chamada assíncrona retorna o status de uma chamada em andamento.</span><span class="sxs-lookup"><span data-stu-id="66de0-104">The **OnProgress** event of [**SWbemSink**](swbemsink.md) is triggered when an asynchronous call returns the status of a call that is in progress.</span></span> <span data-ttu-id="66de0-105">Se os eventos, instâncias ou classes forem produzidos de um provedor que dá suporte a atualizações de status, você poderá posicionar o código nesse evento para fornecer aos usuários comentários sobre o status de uma operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="66de0-105">If the events, instances, or classes are produced from a provider that supports status updates, you can place code in this event to provide users with feedback about the status of an asynchronous operation.</span></span> <span data-ttu-id="66de0-106">Você deve definir o parâmetro *iFlags* da chamada assíncrona para **wbemFlagSendStatus** (128/0x80) se quiser receber atualizações de status, caso contrário, esse evento não será disparado.</span><span class="sxs-lookup"><span data-stu-id="66de0-106">You must set the *iFlags* parameter of the asynchronous call to **wbemFlagSendStatus** (128/0x80) if you want to receive status updates, otherwise this event is not triggered.</span></span>

<span data-ttu-id="66de0-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="66de0-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="66de0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66de0-108">Syntax</span></span>


```VB
SWbemSink.OnProgress( _
  ByVal iUpperBound, _
  ByVal iCurrent, _
  ByVal strMessage, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a><span data-ttu-id="66de0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66de0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66de0-110">*iUpperBound*</span><span class="sxs-lookup"><span data-stu-id="66de0-110">*iUpperBound*</span></span> 
</dt> <dd>

<span data-ttu-id="66de0-111">Inteiro que descreve o número total de tarefas a serem concluídas.</span><span class="sxs-lookup"><span data-stu-id="66de0-111">Integer that describes the total number of tasks to complete.</span></span>

</dd> <dt>

<span data-ttu-id="66de0-112">*iCurrent*</span><span class="sxs-lookup"><span data-stu-id="66de0-112">*iCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="66de0-113">Item atual que está sendo processado.</span><span class="sxs-lookup"><span data-stu-id="66de0-113">Current item that is being processed.</span></span>

</dd> <dt>

<span data-ttu-id="66de0-114">*strMessage*</span><span class="sxs-lookup"><span data-stu-id="66de0-114">*strMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="66de0-115">Mensagem que descreve o status da tarefa atual.</span><span class="sxs-lookup"><span data-stu-id="66de0-115">Message that describes the status of the current task.</span></span>

</dd> <dt>

<span data-ttu-id="66de0-116">*objWbemAsyncContext*</span><span class="sxs-lookup"><span data-stu-id="66de0-116">*objWbemAsyncContext*</span></span> 
</dt> <dd>

<span data-ttu-id="66de0-117">Um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que é passado para a chamada assíncrona original.</span><span class="sxs-lookup"><span data-stu-id="66de0-117">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is passed to the original asynchronous call.</span></span> <span data-ttu-id="66de0-118">Use esse parâmetro para identificar a origem da chamada assíncrona que dispara esse evento quando várias chamadas assíncronas são feitas usando esse coletor de objeto.</span><span class="sxs-lookup"><span data-stu-id="66de0-118">Use this parameter to identify the origin of the asynchronous call that triggers this event when multiple asynchronous calls are made using this object sink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66de0-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="66de0-119">Return value</span></span>

<span data-ttu-id="66de0-120">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="66de0-120">This event does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="66de0-121">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="66de0-121">Error codes</span></span>

<span data-ttu-id="66de0-122">Após a conclusão do evento **OnProgress** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro abaixo.</span><span class="sxs-lookup"><span data-stu-id="66de0-122">After the completion of the **OnProgress** event, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="66de0-123">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="66de0-123">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="66de0-124">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="66de0-124">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="66de0-125">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="66de0-125">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="66de0-126">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="66de0-126">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="66de0-127">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="66de0-127">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="66de0-128">Ocorreu um erro de rede, impedindo a operação normal.</span><span class="sxs-lookup"><span data-stu-id="66de0-128">Networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="66de0-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="66de0-129">Remarks</span></span>

<span data-ttu-id="66de0-130">O evento **OnProgress** é disparado quando uma chamada assíncrona retorna o status de uma chamada em andamento.</span><span class="sxs-lookup"><span data-stu-id="66de0-130">The **OnProgress** event is triggered when an asynchronous call returns the status of a call that is in progress.</span></span> <span data-ttu-id="66de0-131">Se os eventos, instâncias ou classes forem produzidos de um provedor que dá suporte a atualizações de status, você poderá colocar o código nesse evento para fornecer comentários aos usuários sobre o status de uma operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="66de0-131">If the events, instances, or classes are produced from a provider that supports status updates, you can place code in this event to give users feedback about the status of an asynchronous operation.</span></span>

> [!Note]  
> <span data-ttu-id="66de0-132">Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor.</span><span class="sxs-lookup"><span data-stu-id="66de0-132">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="66de0-133">Isso representa riscos de segurança para seus scripts e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="66de0-133">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="66de0-134">Para eliminar os riscos, use a comunicação semi-síncrona ou síncrona.</span><span class="sxs-lookup"><span data-stu-id="66de0-134">To eliminate the risks, use semi-synchronous or synchronous communication.</span></span> <span data-ttu-id="66de0-135">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="66de0-135">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="66de0-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66de0-136">Requirements</span></span>



| <span data-ttu-id="66de0-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="66de0-137">Requirement</span></span> | <span data-ttu-id="66de0-138">Valor</span><span class="sxs-lookup"><span data-stu-id="66de0-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66de0-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66de0-139">Minimum supported client</span></span><br/> | <span data-ttu-id="66de0-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66de0-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="66de0-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66de0-141">Minimum supported server</span></span><br/> | <span data-ttu-id="66de0-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66de0-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="66de0-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66de0-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="66de0-144"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="66de0-144"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="66de0-145">INSERI</span><span class="sxs-lookup"><span data-stu-id="66de0-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="66de0-146"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="66de0-146"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="66de0-147">DLL</span><span class="sxs-lookup"><span data-stu-id="66de0-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66de0-148"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66de0-148"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="66de0-149">CLSID</span><span class="sxs-lookup"><span data-stu-id="66de0-149">CLSID</span></span><br/>                    | <span data-ttu-id="66de0-150">\_SWBEMSINK CLSID</span><span class="sxs-lookup"><span data-stu-id="66de0-150">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="66de0-151">IID</span><span class="sxs-lookup"><span data-stu-id="66de0-151">IID</span></span><br/>                      | <span data-ttu-id="66de0-152">ISWbemSinkEvents de IID \_</span><span class="sxs-lookup"><span data-stu-id="66de0-152">IID\_ISWbemSinkEvents</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="66de0-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="66de0-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66de0-154">**SWbemSink**</span><span class="sxs-lookup"><span data-stu-id="66de0-154">**SWbemSink**</span></span>](swbemsink.md)
</dt> </dl>

 

