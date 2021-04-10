---
description: O evento OnObjectReady de um objeto SWbemSink é disparado quando uma operação assíncrona retorna um objeto.
ms.assetid: 14110ee7-a808-4786-b695-2ce54189d826
ms.tgt_platform: multiple
title: 'Evento ISWbemSinkEvents:: OnObjectReady (Wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnObjectReady
- ISWbemSinkEvents.OnObjectReady
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1fa803339e7007a030881c3d5b47d67f354b5661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091277"
---
# <a name="iswbemsinkeventsonobjectready-event"></a><span data-ttu-id="21b1d-103">Evento ISWbemSinkEvents:: OnObjectReady</span><span class="sxs-lookup"><span data-stu-id="21b1d-103">ISWbemSinkEvents::OnObjectReady event</span></span>

<span data-ttu-id="21b1d-104">O evento **OnObjectReady** de um objeto [**SWbemSink**](swbemsink.md) é disparado quando uma operação assíncrona retorna um objeto.</span><span class="sxs-lookup"><span data-stu-id="21b1d-104">The **OnObjectReady** event of an [**SWbemSink**](swbemsink.md) object is triggered when an asynchronous operation returns an object.</span></span> <span data-ttu-id="21b1d-105">Use esse evento para processar objetos de chamadas assíncronas, como [**SWbemObject \_ . InstancesAsync**](swbemobject-instancesasync-.md) ou [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md).</span><span class="sxs-lookup"><span data-stu-id="21b1d-105">Use this event to process objects from asynchronous calls such as [**SWbemObject.InstancesAsync\_**](swbemobject-instancesasync-.md) or [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md).</span></span> <span data-ttu-id="21b1d-106">**OnObjectReady** retorna um [**SWbemObject**](swbemobject.md) a cada vez até que a enumeração seja concluída.</span><span class="sxs-lookup"><span data-stu-id="21b1d-106">**OnObjectReady** returns one [**SWbemObject**](swbemobject.md) each time until the enumeration is complete.</span></span>

<span data-ttu-id="21b1d-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="21b1d-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="21b1d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21b1d-108">Syntax</span></span>


```VB
SWbemSink.OnObjectReady( _
  ByVal objWbemObject, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a><span data-ttu-id="21b1d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21b1d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21b1d-110">*objWbemObject*</span><span class="sxs-lookup"><span data-stu-id="21b1d-110">*objWbemObject*</span></span> 
</dt> <dd>

<span data-ttu-id="21b1d-111">Um objeto [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="21b1d-111">An [**SWbemObject**](swbemobject.md) object.</span></span> <span data-ttu-id="21b1d-112">Isso é semelhante ao que é retornado pelo equivalente síncrono da chamada assíncrona que dispara esse evento.</span><span class="sxs-lookup"><span data-stu-id="21b1d-112">This is similar to what is returned by the synchronous equivalent of the asynchronous call that triggers this event.</span></span> <span data-ttu-id="21b1d-113">Por exemplo, uma chamada para o método [**SWbemServices. getasync**](swbemservices-getasync.md) retorna um **SWbemObject** no parâmetro *objWbemObject* do evento **OnObjectReady** do objeto [**SWbemSink**](swbemsink.md) , que é passado como o parâmetro *objWbemObject* da chamada original.</span><span class="sxs-lookup"><span data-stu-id="21b1d-113">For example, a call to the [**SWbemServices.GetAsync**](swbemservices-getasync.md) method returns an **SWbemObject** in the *objWbemObject* parameter of the **OnObjectReady** event of the [**SWbemSink**](swbemsink.md) object, which is passed as the *objWbemObject* parameter of the original call.</span></span> <span data-ttu-id="21b1d-114">O mesmo objeto **SWbemObject** pode ser obtido usando uma chamada síncrona equivalente para [**SWbemServices. Get**](swbemservices-get.md).</span><span class="sxs-lookup"><span data-stu-id="21b1d-114">The same **SWbemObject** object can be obtained by using an equivalent synchronous call to [**SWbemServices.Get**](swbemservices-get.md).</span></span>

</dd> <dt>

<span data-ttu-id="21b1d-115">*objWbemAsyncContext*</span><span class="sxs-lookup"><span data-stu-id="21b1d-115">*objWbemAsyncContext*</span></span> 
</dt> <dd>

<span data-ttu-id="21b1d-116">Um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que é passado para a chamada assíncrona original.</span><span class="sxs-lookup"><span data-stu-id="21b1d-116">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is passed to the original asynchronous call.</span></span> <span data-ttu-id="21b1d-117">Use esse parâmetro para identificar a origem da chamada assíncrona que dispara esse evento quando várias chamadas assíncronas são feitas usando esse coletor de objeto.</span><span class="sxs-lookup"><span data-stu-id="21b1d-117">Use this parameter to identify the origin of the asynchronous call that triggers this event when multiple asynchronous calls are made using this object sink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21b1d-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="21b1d-118">Return value</span></span>

<span data-ttu-id="21b1d-119">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="21b1d-119">This event does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="21b1d-120">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="21b1d-120">Error codes</span></span>

<span data-ttu-id="21b1d-121">Após a conclusão do evento **OnObjectReady** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro abaixo.</span><span class="sxs-lookup"><span data-stu-id="21b1d-121">After the completion of the **OnObjectReady** event, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="21b1d-122">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="21b1d-122">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="21b1d-123">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="21b1d-123">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="21b1d-124">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="21b1d-124">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="21b1d-125">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="21b1d-125">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="21b1d-126">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="21b1d-126">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="21b1d-127">Ocorreu um erro de rede, impedindo a operação normal.</span><span class="sxs-lookup"><span data-stu-id="21b1d-127">Networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="21b1d-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="21b1d-128">Remarks</span></span>

<span data-ttu-id="21b1d-129">Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor.</span><span class="sxs-lookup"><span data-stu-id="21b1d-129">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="21b1d-130">Isso representa riscos de segurança para seus scripts e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="21b1d-130">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="21b1d-131">Para eliminar os riscos, use a comunicação semi-síncrona ou a comunicação síncrona.</span><span class="sxs-lookup"><span data-stu-id="21b1d-131">To eliminate the risks, use either semi-synchronous communication or synchronous communication.</span></span> <span data-ttu-id="21b1d-132">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="21b1d-132">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="21b1d-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21b1d-133">Requirements</span></span>



| <span data-ttu-id="21b1d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="21b1d-134">Requirement</span></span> | <span data-ttu-id="21b1d-135">Valor</span><span class="sxs-lookup"><span data-stu-id="21b1d-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21b1d-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21b1d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="21b1d-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="21b1d-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="21b1d-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21b1d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="21b1d-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21b1d-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="21b1d-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="21b1d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="21b1d-141"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="21b1d-141"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="21b1d-142">INSERI</span><span class="sxs-lookup"><span data-stu-id="21b1d-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="21b1d-143"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="21b1d-143"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="21b1d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="21b1d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21b1d-145"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21b1d-145"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="21b1d-146">CLSID</span><span class="sxs-lookup"><span data-stu-id="21b1d-146">CLSID</span></span><br/>                    | <span data-ttu-id="21b1d-147">\_SWBEMSINK CLSID</span><span class="sxs-lookup"><span data-stu-id="21b1d-147">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="21b1d-148">IID</span><span class="sxs-lookup"><span data-stu-id="21b1d-148">IID</span></span><br/>                      | <span data-ttu-id="21b1d-149">ISWbemSinkEvents de IID \_</span><span class="sxs-lookup"><span data-stu-id="21b1d-149">IID\_ISWbemSinkEvents</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="21b1d-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="21b1d-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21b1d-151">**SWbemSink**</span><span class="sxs-lookup"><span data-stu-id="21b1d-151">**SWbemSink**</span></span>](swbemsink.md)
</dt> </dl>

 

