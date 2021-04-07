---
description: Recupera instâncias de uma classe especificada de acordo com os critérios especificados pelo usuário.
ms.assetid: 631cd749-9a39-4606-9a38-0b4bb5b4b2cd
ms.tgt_platform: multiple
title: Método SWbemServices. InstancesOfAsync (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.InstancesOfAsync
- ISWbemServices.InstancesOfAsync
- ISWbemServices.InstancesOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c518cb38a0ecb221f4fcb0d0e7f9ce6dfc226ba9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827709"
---
# <a name="swbemservicesinstancesofasync-method"></a><span data-ttu-id="aee7d-103">Método SWbemServices. InstancesOfAsync</span><span class="sxs-lookup"><span data-stu-id="aee7d-103">SWbemServices.InstancesOfAsync method</span></span>

<span data-ttu-id="aee7d-104">O método **InstancesOfAsync** do objeto [**SWbemServices**](swbemservices.md) recupera instâncias de uma classe especificada de acordo com os critérios especificados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="aee7d-104">The **InstancesOfAsync** method of the [**SWbemServices**](swbemservices.md) object retrieves instances of a specified class according to user-specified criteria.</span></span>

<span data-ttu-id="aee7d-105">O método é chamado no modo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="aee7d-105">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="aee7d-106">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="aee7d-106">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="aee7d-107">Para obter a explicação da sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="aee7d-107">For the syntax explanation, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="aee7d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aee7d-108">Syntax</span></span>


```VB
SWbemServices.InstancesOfAsync( _
  ByVal ObjWbemSink, _
  ByVal strClass, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="aee7d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aee7d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aee7d-110">*ObjWbemSink*</span><span class="sxs-lookup"><span data-stu-id="aee7d-110">*ObjWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="aee7d-111">Coletor de objeto que recebe as instâncias de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="aee7d-111">Object sink that receives the instances asynchronously.</span></span> <span data-ttu-id="aee7d-112">Crie um objeto [**SWbemSink**](swbemsink.md) para receber os objetos.</span><span class="sxs-lookup"><span data-stu-id="aee7d-112">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="aee7d-113">*strClass*</span><span class="sxs-lookup"><span data-stu-id="aee7d-113">*strClass*</span></span> 
</dt> <dd>

<span data-ttu-id="aee7d-114">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="aee7d-114">Required.</span></span> <span data-ttu-id="aee7d-115">Cadeia de caracteres que contém o nome da classe para as instâncias que você deseja.</span><span class="sxs-lookup"><span data-stu-id="aee7d-115">String that contains the name of the class for the instances that you want.</span></span> <span data-ttu-id="aee7d-116">Este parâmetro não pode ficar em branco.</span><span class="sxs-lookup"><span data-stu-id="aee7d-116">This parameter cannot be blank.</span></span>

</dd> <dt>

<span data-ttu-id="aee7d-117">*iFlags* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="aee7d-117">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="aee7d-118">Determina a profundidade da enumeração de chamada e se a chamada retorna ou não imediatamente.</span><span class="sxs-lookup"><span data-stu-id="aee7d-118">Determines the depth of the call enumeration, and whether or not the call returns immediately.</span></span> <span data-ttu-id="aee7d-119">Esse parâmetro pode aceitar os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="aee7d-119">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="aee7d-120"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="aee7d-120"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="aee7d-121">Força a enumeração a incluir apenas subclasses imediatas da classe pai especificada.</span><span class="sxs-lookup"><span data-stu-id="aee7d-121">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="aee7d-122"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="aee7d-122"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="aee7d-123">Padrão para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="aee7d-123">Default for this parameter.</span></span> <span data-ttu-id="aee7d-124">Esse valor força a enumeração a incluir todas as classes na hierarquia.</span><span class="sxs-lookup"><span data-stu-id="aee7d-124">This value forces the enumeration to include all classes in the hierarchy.</span></span>

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="aee7d-125"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="aee7d-125"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="aee7d-126">Faz com que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="aee7d-126">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="aee7d-127"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="aee7d-127"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="aee7d-128">Impede que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="aee7d-128">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="aee7d-129"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="aee7d-129"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="aee7d-130">Faz com que o WMI retorne dados de alteração de classe com a definição de classe base.</span><span class="sxs-lookup"><span data-stu-id="aee7d-130">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="aee7d-131">Para obter mais informações, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="aee7d-131">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="aee7d-132">*objWbemNamedValueSet* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="aee7d-132">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="aee7d-133">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="aee7d-133">Typically, this is undefined.</span></span> <span data-ttu-id="aee7d-134">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="aee7d-134">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="aee7d-135">Um provedor que dá suporte ou exige informações de informações de contexto deve documentar os nomes de valores reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="aee7d-135">A provider that supports or requires context information information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="aee7d-136">*objWbemAsyncContext* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="aee7d-136">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="aee7d-137">Um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que retorna ao coletor de objeto para identificar a origem da chamada assíncrona original.</span><span class="sxs-lookup"><span data-stu-id="aee7d-137">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="aee7d-138">Use esse parâmetro se você estiver fazendo várias chamadas assíncronas usando o mesmo coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="aee7d-138">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="aee7d-139">Para usar esse parâmetro, crie um objeto **SWbemNamedValueSet** e use o método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo.</span><span class="sxs-lookup"><span data-stu-id="aee7d-139">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="aee7d-140">Esse objeto **SWbemNamedValueSet** é retornado para o coletor de objeto e a origem da chamada pode ser extraída usando o método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="aee7d-140">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aee7d-141">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aee7d-141">Return value</span></span>

<span data-ttu-id="aee7d-142">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="aee7d-142">This method does not return a value.</span></span> <span data-ttu-id="aee7d-143">Se for bem-sucedido, o coletor receberá um evento [**OnObjectReady**](swbemsink-onobjectready.md) por instância.</span><span class="sxs-lookup"><span data-stu-id="aee7d-143">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="aee7d-144">Após a última instância, o coletor de objeto recebe um evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="aee7d-144">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="aee7d-145">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="aee7d-145">Error codes</span></span>

<span data-ttu-id="aee7d-146">Após a conclusão do método **InstancesOfAsync** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="aee7d-146">Upon the completion of the **InstancesOfAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="aee7d-147">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="aee7d-147">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="aee7d-148">O usuário atual não tem permissão para exibir instâncias da classe especificada.</span><span class="sxs-lookup"><span data-stu-id="aee7d-148">Current user does not have the permission to view instances of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="aee7d-149">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="aee7d-149">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="aee7d-150">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="aee7d-150">Unspecified error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="aee7d-151">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="aee7d-151">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="aee7d-152">A classe especificada não é válida.</span><span class="sxs-lookup"><span data-stu-id="aee7d-152">Specified class is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="aee7d-153">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="aee7d-153">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="aee7d-154">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="aee7d-154">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="aee7d-155">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="aee7d-155">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="aee7d-156">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="aee7d-156">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aee7d-157">Comentários</span><span class="sxs-lookup"><span data-stu-id="aee7d-157">Remarks</span></span>

<span data-ttu-id="aee7d-158">Essa chamada retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="aee7d-158">This call returns immediately.</span></span> <span data-ttu-id="aee7d-159">Os objetos e status solicitados são retornados ao chamador por meio de retornos de chamada entregues ao coletor especificado em *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="aee7d-159">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="aee7d-160">Para processar cada objeto quando ele retornar, crie um *objWbemSink*. Sub-rotina de evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="aee7d-160">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="aee7d-161">Depois que todos os objetos forem retornados, você poderá executar o processamento final em sua implementação do *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="aee7d-161">After all the objects are returned, you can perform the final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="aee7d-162">Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor.</span><span class="sxs-lookup"><span data-stu-id="aee7d-162">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="aee7d-163">Isso representa riscos de segurança para seus scripts e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="aee7d-163">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="aee7d-164">Para eliminar os riscos, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md)</span><span class="sxs-lookup"><span data-stu-id="aee7d-164">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md)</span></span>

<span data-ttu-id="aee7d-165">O método **InstancesOfAsync** só funciona para objetos de classe.</span><span class="sxs-lookup"><span data-stu-id="aee7d-165">The **InstancesOfAsync** method only works for class objects.</span></span> <span data-ttu-id="aee7d-166">Não é um erro para o enumerador retornado ter zero (0) elementos.</span><span class="sxs-lookup"><span data-stu-id="aee7d-166">It is not an error for the returned enumerator to have zero (0) elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="aee7d-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aee7d-167">Requirements</span></span>



| <span data-ttu-id="aee7d-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="aee7d-168">Requirement</span></span> | <span data-ttu-id="aee7d-169">Valor</span><span class="sxs-lookup"><span data-stu-id="aee7d-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aee7d-170">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aee7d-170">Minimum supported client</span></span><br/> | <span data-ttu-id="aee7d-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aee7d-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aee7d-172">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aee7d-172">Minimum supported server</span></span><br/> | <span data-ttu-id="aee7d-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aee7d-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aee7d-174">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aee7d-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="aee7d-175"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="aee7d-175"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="aee7d-176">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="aee7d-176">Type library</span></span><br/>             | <dl> <span data-ttu-id="aee7d-177"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="aee7d-177"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="aee7d-178">DLL</span><span class="sxs-lookup"><span data-stu-id="aee7d-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aee7d-179"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aee7d-179"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="aee7d-180">CLSID</span><span class="sxs-lookup"><span data-stu-id="aee7d-180">CLSID</span></span><br/>                    | <span data-ttu-id="aee7d-181">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="aee7d-181">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="aee7d-182">IID</span><span class="sxs-lookup"><span data-stu-id="aee7d-182">IID</span></span><br/>                      | <span data-ttu-id="aee7d-183">ISWbemServices de IID \_</span><span class="sxs-lookup"><span data-stu-id="aee7d-183">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="aee7d-184">Confira também</span><span class="sxs-lookup"><span data-stu-id="aee7d-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aee7d-185">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="aee7d-185">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="aee7d-186">Chamando um método</span><span class="sxs-lookup"><span data-stu-id="aee7d-186">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

