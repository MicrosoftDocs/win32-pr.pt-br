---
description: O \_ método SubclassesAsync de SWbemObject fornece de forma assíncrona as subclasses do objeto atual, que deve ser uma classe.
ms.assetid: 14d4a609-3aa4-49bd-bea4-6a71bc24d9dd
ms.tgt_platform: multiple
title: Método de SWbemObject.SubclassesAsync_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SubclassesAsync_
- ISWbemObject.SubclassesAsync_
- ISWbemObject.SubclassesAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6e922953e9f25aae2e47ea572678790b1228a581
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171787"
---
# <a name="swbemobjectsubclassesasync_-method"></a><span data-ttu-id="f2832-103">Método SWbemObject. SubclassesAsync \_</span><span class="sxs-lookup"><span data-stu-id="f2832-103">SWbemObject.SubclassesAsync\_ method</span></span>

<span data-ttu-id="f2832-104">O **método \_ SubclassesAsync** de [**SWbemObject**](swbemobject.md) fornece de forma assíncrona as subclasses do objeto atual, que deve ser uma classe.</span><span class="sxs-lookup"><span data-stu-id="f2832-104">The **SubclassesAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously supplies the subclasses of the current object, which must be a class.</span></span>

<span data-ttu-id="f2832-105">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="f2832-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f2832-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2832-106">Syntax</span></span>


```VB
SWbemObject.SubclassesAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="f2832-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2832-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2832-108">*objWbemSink* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f2832-108">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2832-109">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="f2832-109">Required.</span></span> <span data-ttu-id="f2832-110">Coletor de objeto que recebe os objetos de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="f2832-110">Object sink that receives the objects asynchronously.</span></span>

</dd> <dt>

<span data-ttu-id="f2832-111">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f2832-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f2832-112">Determina o quão detalhado a chamada enumera.</span><span class="sxs-lookup"><span data-stu-id="f2832-112">Determines how detailed the call enumerates.</span></span> <span data-ttu-id="f2832-113">Esse parâmetro pode aceitar os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f2832-113">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="f2832-114"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="f2832-114"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="f2832-115">Força a enumeração recursiva em todas as subclasses derivadas da classe pai especificada.</span><span class="sxs-lookup"><span data-stu-id="f2832-115">Forces recursive enumeration into all subclasses derived from the specified parent class.</span></span> <span data-ttu-id="f2832-116">A própria classe pai não é retornada na enumeração.</span><span class="sxs-lookup"><span data-stu-id="f2832-116">The parent class itself is not returned in the enumeration.</span></span>

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="f2832-117"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="f2832-117"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="f2832-118">Padrão para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f2832-118">Default for this parameter.</span></span> <span data-ttu-id="f2832-119">Ele força a enumeração a incluir apenas subclasses imediatas da classe pai especificada.</span><span class="sxs-lookup"><span data-stu-id="f2832-119">It forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="f2832-120"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="f2832-120"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="f2832-121">Faz com que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**SWbemSink. OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="f2832-121">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="f2832-122"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="f2832-122"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="f2832-123">Impede que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="f2832-123">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="f2832-124"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="f2832-124"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="f2832-125">Faz com que o WMI retorne dados de alteração de classe com a definição de classe base.</span><span class="sxs-lookup"><span data-stu-id="f2832-125">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="f2832-126">Para obter mais informações sobre qualificadores corrigidos, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="f2832-126">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f2832-127">*objWbemNamedValueSet* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f2832-127">*objWbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f2832-128">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="f2832-128">Typically, this is undefined.</span></span> <span data-ttu-id="f2832-129">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="f2832-129">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="f2832-130">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="f2832-130">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="f2832-131">*objWbemAsyncContext* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f2832-131">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f2832-132">Esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que retorna ao coletor de objeto para identificar a origem da chamada assíncrona original.</span><span class="sxs-lookup"><span data-stu-id="f2832-132">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="f2832-133">Use esse parâmetro ao fazer várias chamadas assíncronas usando o mesmo coletor de objeto.</span><span class="sxs-lookup"><span data-stu-id="f2832-133">Use this parameter when you make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="f2832-134">Para usar esse parâmetro, crie um objeto **SWbemNamedValueSet** e use o método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo.</span><span class="sxs-lookup"><span data-stu-id="f2832-134">To use this parameter, create an **SWbemNamedValueSet** object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="f2832-135">Esse objeto **SWbemNamedValueSet** é retornado para o coletor de objeto e a origem da chamada pode ser extraída usando o método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="f2832-135">This **SWbemNamedValueSet** object is returned to the object sink, and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="f2832-136">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="f2832-136">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2832-137">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f2832-137">Return value</span></span>

<span data-ttu-id="f2832-138">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f2832-138">This method does not return a value.</span></span> <span data-ttu-id="f2832-139">Se for bem-sucedido, o coletor receberá um evento [**OnObjectReady**](swbemsink-onobjectready.md) para cada instância.</span><span class="sxs-lookup"><span data-stu-id="f2832-139">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event for each instance.</span></span> <span data-ttu-id="f2832-140">Após a última instância, o coletor de objeto recebe um evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="f2832-140">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f2832-141">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="f2832-141">Error codes</span></span>

<span data-ttu-id="f2832-142">Após a conclusão do método **SubclassesAsync \_** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="f2832-142">After the completion of the **SubclassesAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="f2832-143">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="f2832-143">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="f2832-144">O usuário atual não tem permissão para exibir uma ou mais das classes retornadas pela chamada.</span><span class="sxs-lookup"><span data-stu-id="f2832-144">Current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="f2832-145">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="f2832-145">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="f2832-146">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="f2832-146">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="f2832-147">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="f2832-147">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="f2832-148">A classe especificada não existe.</span><span class="sxs-lookup"><span data-stu-id="f2832-148">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="f2832-149">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="f2832-149">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="f2832-150">Foi especificado um parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="f2832-150">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="f2832-151">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="f2832-151">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="f2832-152">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="f2832-152">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2832-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2832-153">Remarks</span></span>

<span data-ttu-id="f2832-154">Essa chamada retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="f2832-154">This call returns immediately.</span></span> <span data-ttu-id="f2832-155">Os objetos e status solicitados são retornados ao chamador por meio de retornos de chamada entregues ao coletor especificado em *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="f2832-155">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="f2832-156">Para processar cada objeto quando ele chegar, crie um *objWbemSink*. Sub-rotina de evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="f2832-156">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="f2832-157">Depois que todos os objetos forem retornados, você poderá executar o processamento final em sua implementação do *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="f2832-157">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="f2832-158">Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor.</span><span class="sxs-lookup"><span data-stu-id="f2832-158">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="f2832-159">Isso representa riscos de segurança para seus scripts e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f2832-159">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="f2832-160">Para eliminar os riscos, use a comunicação do semisynchronous ou a comunicação síncrona.</span><span class="sxs-lookup"><span data-stu-id="f2832-160">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="f2832-161">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="f2832-161">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="f2832-162">É recomendável que os scripts verifiquem a origem da chamada usando um parâmetro *objWbemAsyncContext* .</span><span class="sxs-lookup"><span data-stu-id="f2832-162">It is recommended that scripts verify the source of the call by using an *objWbemAsyncContext* parameter.</span></span>

<span data-ttu-id="f2832-163">Não é um erro para a coleção retornada ter zero elementos se não houver subclasses do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="f2832-163">It is not an error for the returned collection to have zero elements if there are no subclasses of the current object.</span></span> <span data-ttu-id="f2832-164">O **método \_ SubclassesAsync** só funciona para objetos de classe.</span><span class="sxs-lookup"><span data-stu-id="f2832-164">The **SubclassesAsync\_** method only works for class objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2832-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2832-165">Requirements</span></span>



| <span data-ttu-id="f2832-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2832-166">Requirement</span></span> | <span data-ttu-id="f2832-167">Valor</span><span class="sxs-lookup"><span data-stu-id="f2832-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2832-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2832-168">Minimum supported client</span></span><br/> | <span data-ttu-id="f2832-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f2832-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f2832-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2832-170">Minimum supported server</span></span><br/> | <span data-ttu-id="f2832-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2832-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f2832-172">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f2832-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2832-173"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2832-173"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f2832-174">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f2832-174">Type library</span></span><br/>             | <dl> <span data-ttu-id="f2832-175"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f2832-175"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f2832-176">DLL</span><span class="sxs-lookup"><span data-stu-id="f2832-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2832-177"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2832-177"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f2832-178">CLSID</span><span class="sxs-lookup"><span data-stu-id="f2832-178">CLSID</span></span><br/>                    | <span data-ttu-id="f2832-179">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="f2832-179">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="f2832-180">IID</span><span class="sxs-lookup"><span data-stu-id="f2832-180">IID</span></span><br/>                      | <span data-ttu-id="f2832-181">ISWbemObject de IID \_</span><span class="sxs-lookup"><span data-stu-id="f2832-181">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="f2832-182">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2832-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2832-183">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="f2832-183">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="f2832-184">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="f2832-184">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> <dt>

[<span data-ttu-id="f2832-185">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="f2832-185">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> </dl>

 

