---
description: O evento OnCompleted de um objeto SWbemSink é disparado quando uma chamada assíncrona é concluída. Esse evento indica ao aplicativo cliente, o resultado de uma operação assíncrona e fornece informações de erro quando a chamada assíncrona falha.
ms.assetid: 2723185d-5b8b-4cc7-ada3-51c3275272a9
ms.tgt_platform: multiple
title: 'Evento ISWbemSinkEvents:: OnCompleted (Wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnCompleted
- ISWbemSinkEvents.OnCompleted
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 16cb0362b5c1b1d432d72bb959103adbb7315069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091279"
---
# <a name="iswbemsinkeventsoncompleted-event"></a><span data-ttu-id="fbeaa-104">Evento ISWbemSinkEvents:: OnCompleted</span><span class="sxs-lookup"><span data-stu-id="fbeaa-104">ISWbemSinkEvents::OnCompleted event</span></span>

<span data-ttu-id="fbeaa-105">O evento **OnCompleted** de um objeto [**SWbemSink**](swbemsink.md) é disparado quando uma chamada assíncrona é concluída.</span><span class="sxs-lookup"><span data-stu-id="fbeaa-105">The **OnCompleted** event of an [**SWbemSink**](swbemsink.md) object is triggered when an asynchronous call is complete.</span></span> <span data-ttu-id="fbeaa-106">Esse evento indica ao aplicativo cliente, o resultado de uma operação assíncrona e fornece informações de erro quando a chamada assíncrona falha.</span><span class="sxs-lookup"><span data-stu-id="fbeaa-106">This event indicates to the client application, the result of an asynchronous operation, and provides error information when the asynchronous call fails.</span></span>

<span data-ttu-id="fbeaa-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="fbeaa-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fbeaa-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fbeaa-108">Syntax</span></span>


```VB
SWbemSink.OnCompleted( _
  ByVal iHResult, _
  ByVal objWbemErrorObject, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a><span data-ttu-id="fbeaa-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fbeaa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbeaa-110">*iHResult*</span><span class="sxs-lookup"><span data-stu-id="fbeaa-110">*iHResult*</span></span> 
</dt> <dd>

<span data-ttu-id="fbeaa-111">O HRESULT do método assíncrono concluído.</span><span class="sxs-lookup"><span data-stu-id="fbeaa-111">The HRESULT of the completed asynchronous method.</span></span> <span data-ttu-id="fbeaa-112">O HRESULT é o mesmo que o valor retornado de uma [API com equivalente para chamada de método WMI](com-api-for-wmi.md) .</span><span class="sxs-lookup"><span data-stu-id="fbeaa-112">The HRESULT is the same as the value that is returned from an equivalent [COM API for WMI](com-api-for-wmi.md) method call.</span></span> <span data-ttu-id="fbeaa-113">Verifique esse valor para determinar se a chamada assíncrona foi bem-sucedida ou não.</span><span class="sxs-lookup"><span data-stu-id="fbeaa-113">Check this value to determine whether or not the asynchronous call is successful.</span></span> <span data-ttu-id="fbeaa-114">Se a chamada assíncrona for bem-sucedida, esse parâmetro conterá o WBEM \_ S \_ sem \_ erro (0).</span><span class="sxs-lookup"><span data-stu-id="fbeaa-114">If the asynchronous call is successful, this parameter contains WBEM\_S\_NO\_ERROR (0).</span></span> <span data-ttu-id="fbeaa-115">Se a chamada assíncrona falhar, esse parâmetro conterá um código de erro.</span><span class="sxs-lookup"><span data-stu-id="fbeaa-115">If the asynchronous call fails, this parameter contains an error code.</span></span>

</dd> <dt>

<span data-ttu-id="fbeaa-116">*objWbemErrorObject*</span><span class="sxs-lookup"><span data-stu-id="fbeaa-116">*objWbemErrorObject*</span></span> 
</dt> <dd>

<span data-ttu-id="fbeaa-117">Contém um objeto [**SWbemLastError**](swbemlasterror.md) quando o método assíncrono falha.</span><span class="sxs-lookup"><span data-stu-id="fbeaa-117">Contains an [**SWbemLastError**](swbemlasterror.md) object when the asynchronous method fails.</span></span>

</dd> <dt>

<span data-ttu-id="fbeaa-118">*objWbemAsyncContext*</span><span class="sxs-lookup"><span data-stu-id="fbeaa-118">*objWbemAsyncContext*</span></span> 
</dt> <dd>

<span data-ttu-id="fbeaa-119">Esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que é passado para a chamada assíncrona original.</span><span class="sxs-lookup"><span data-stu-id="fbeaa-119">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is passed to the original asynchronous call.</span></span> <span data-ttu-id="fbeaa-120">Use esse parâmetro para identificar a origem da chamada assíncrona que dispara esse evento quando várias chamadas assíncronas são feitas usando esse coletor de objeto.</span><span class="sxs-lookup"><span data-stu-id="fbeaa-120">Use this parameter to identify the origin of the asynchronous call that triggers this event when multiple asynchronous calls are made using this object sink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbeaa-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fbeaa-121">Return value</span></span>

<span data-ttu-id="fbeaa-122">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="fbeaa-122">This event does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fbeaa-123">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="fbeaa-123">Error codes</span></span>

<span data-ttu-id="fbeaa-124">Após a conclusão do evento **OnCompleted** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro abaixo.</span><span class="sxs-lookup"><span data-stu-id="fbeaa-124">After completion of the **OnCompleted** event, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="fbeaa-125">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="fbeaa-125">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="fbeaa-126">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="fbeaa-126">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="fbeaa-127">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="fbeaa-127">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="fbeaa-128">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="fbeaa-128">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fbeaa-129">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="fbeaa-129">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="fbeaa-130">Ocorreu um erro de rede, impedindo a operação normal.</span><span class="sxs-lookup"><span data-stu-id="fbeaa-130">Networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fbeaa-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbeaa-131">Remarks</span></span>

<span data-ttu-id="fbeaa-132">Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor.</span><span class="sxs-lookup"><span data-stu-id="fbeaa-132">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="fbeaa-133">Isso representa riscos de segurança para seus scripts e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="fbeaa-133">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="fbeaa-134">Para eliminar os riscos, use semisynchronous ou comunicação síncrona.</span><span class="sxs-lookup"><span data-stu-id="fbeaa-134">To eliminate the risks, use semisynchronous or synchronous communication.</span></span> <span data-ttu-id="fbeaa-135">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="fbeaa-135">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fbeaa-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbeaa-136">Requirements</span></span>



| <span data-ttu-id="fbeaa-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbeaa-137">Requirement</span></span> | <span data-ttu-id="fbeaa-138">Valor</span><span class="sxs-lookup"><span data-stu-id="fbeaa-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbeaa-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbeaa-139">Minimum supported client</span></span><br/> | <span data-ttu-id="fbeaa-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fbeaa-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fbeaa-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbeaa-141">Minimum supported server</span></span><br/> | <span data-ttu-id="fbeaa-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fbeaa-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fbeaa-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fbeaa-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbeaa-144"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbeaa-144"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fbeaa-145">INSERI</span><span class="sxs-lookup"><span data-stu-id="fbeaa-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fbeaa-146"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fbeaa-146"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="fbeaa-147">DLL</span><span class="sxs-lookup"><span data-stu-id="fbeaa-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbeaa-148"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbeaa-148"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fbeaa-149">CLSID</span><span class="sxs-lookup"><span data-stu-id="fbeaa-149">CLSID</span></span><br/>                    | <span data-ttu-id="fbeaa-150">\_SWBEMSINK CLSID</span><span class="sxs-lookup"><span data-stu-id="fbeaa-150">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="fbeaa-151">IID</span><span class="sxs-lookup"><span data-stu-id="fbeaa-151">IID</span></span><br/>                      | <span data-ttu-id="fbeaa-152">ISWbemSinkEvents de IID \_</span><span class="sxs-lookup"><span data-stu-id="fbeaa-152">IID\_ISWbemSinkEvents</span></span><br/>                                                        |



 

