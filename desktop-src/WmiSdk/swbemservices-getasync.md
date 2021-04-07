---
description: Recupera um objeto, que é uma definição de classe ou uma instância, com base no caminho do objeto.
ms.assetid: 8da46851-52b8-4b5a-8c9d-1d492f57f4b6
ms.tgt_platform: multiple
title: Método SWbemServices. getasync (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.GetAsync
- ISWbemServices.GetAsync
- ISWbemServices.GetAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 451f13bde9458e7d57ec393f42b92a4092c99924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827710"
---
# <a name="swbemservicesgetasync-method"></a><span data-ttu-id="c0c75-103">Método SWbemServices. getasync</span><span class="sxs-lookup"><span data-stu-id="c0c75-103">SWbemServices.GetAsync method</span></span>

<span data-ttu-id="c0c75-104">O método **getasync** do objeto [**SWbemServices**](swbemservices.md) recupera um objeto, que é uma definição de classe ou uma instância, com base no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="c0c75-104">The **GetAsync** method of the [**SWbemServices**](swbemservices.md) object retrieves an object, that is a class definition or an instance, based on the object path.</span></span>

<span data-ttu-id="c0c75-105">Esse método recupera somente objetos do namespace que está associado ao objeto [**SWbemServices**](swbemservices.md) atual.</span><span class="sxs-lookup"><span data-stu-id="c0c75-105">This method retrieves only objects from the namespace that is associated with the current [**SWbemServices**](swbemservices.md) object.</span></span>

<span data-ttu-id="c0c75-106">Esse método é chamado no modo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="c0c75-106">This method is called in the asynchronous mode.</span></span> <span data-ttu-id="c0c75-107">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="c0c75-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="c0c75-108">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c0c75-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c0c75-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0c75-109">Syntax</span></span>


```VB
SWbemServices.GetAsync( _
  ByVal objWbemSink, _
  [ ByVal strObjectPath ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c0c75-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0c75-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0c75-111">*objWbemSink*</span><span class="sxs-lookup"><span data-stu-id="c0c75-111">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="c0c75-112">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="c0c75-112">Required.</span></span> <span data-ttu-id="c0c75-113">Coletor de objeto que obtém objetos de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="c0c75-113">Object sink that gets objects asynchronously.</span></span> <span data-ttu-id="c0c75-114">Crie um objeto [**SWbemSink**](swbemsink.md) para receber os objetos.</span><span class="sxs-lookup"><span data-stu-id="c0c75-114">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="c0c75-115">*strObjectPath* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="c0c75-115">*strObjectPath* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c0c75-116">Caminho do objeto que você deseja recuperar.</span><span class="sxs-lookup"><span data-stu-id="c0c75-116">Path of the object that you want to retrieve.</span></span> <span data-ttu-id="c0c75-117">Se esse valor estiver vazio, o objeto vazio retornado poderá se tornar uma nova classe.</span><span class="sxs-lookup"><span data-stu-id="c0c75-117">If this value is empty, the empty object that is returned can become a new class.</span></span> <span data-ttu-id="c0c75-118">Para obter mais informações, consulte [descrevendo o local de um objeto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="c0c75-118">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0c75-119">*iFlags* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="c0c75-119">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c0c75-120">Inteiro que determina o comportamento da chamada.</span><span class="sxs-lookup"><span data-stu-id="c0c75-120">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="c0c75-121">Esse parâmetro pode aceitar os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c0c75-121">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="c0c75-122"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="c0c75-122"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="c0c75-123">Faz com que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="c0c75-123">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="c0c75-124"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="c0c75-124"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="c0c75-125">Impede que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="c0c75-125">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="c0c75-126"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="c0c75-126"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="c0c75-127">Faz com que o WMI retorne dados de alteração de classe com a definição de classe base.</span><span class="sxs-lookup"><span data-stu-id="c0c75-127">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="c0c75-128">Para obter mais informações, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="c0c75-128">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c0c75-129">*objwbemNamedValueSet* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="c0c75-129">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c0c75-130">Normalmente, esse valor é indefinido.</span><span class="sxs-lookup"><span data-stu-id="c0c75-130">Typically, this value is undefined.</span></span> <span data-ttu-id="c0c75-131">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="c0c75-131">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="c0c75-132">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="c0c75-132">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="c0c75-133">*objWbemAsyncContext* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="c0c75-133">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c0c75-134">Um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que retorna ao coletor de objeto para identificar a origem da chamada assíncrona original.</span><span class="sxs-lookup"><span data-stu-id="c0c75-134">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="c0c75-135">Use esse parâmetro se você estiver fazendo várias chamadas assíncronas usando o mesmo coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="c0c75-135">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="c0c75-136">Para usar esse parâmetro, crie um objeto **SWbemNamedValueSet** e use o método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo.</span><span class="sxs-lookup"><span data-stu-id="c0c75-136">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="c0c75-137">Esse objeto **SWbemNamedValueSet** é retornado para o coletor de objeto e a origem da chamada pode ser extraída usando o método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="c0c75-137">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="c0c75-138">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="c0c75-138">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0c75-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c0c75-139">Return value</span></span>

<span data-ttu-id="c0c75-140">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c0c75-140">This method does not return a value.</span></span> <span data-ttu-id="c0c75-141">Se for bem-sucedido, o coletor receberá um evento [**OnObjectReady**](swbemsink-onobjectready.md) quando o objeto estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="c0c75-141">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event when the object is available.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c0c75-142">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="c0c75-142">Error codes</span></span>

<span data-ttu-id="c0c75-143">Após a conclusão do método **getasync** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="c0c75-143">After the completion of the **GetAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="c0c75-144">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="c0c75-144">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="c0c75-145">O usuário atual não tem permissão para acessar o objeto.</span><span class="sxs-lookup"><span data-stu-id="c0c75-145">Current user does not have the permission to access the object.</span></span>

</dd> <dt>

<span data-ttu-id="c0c75-146">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="c0c75-146">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="c0c75-147">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="c0c75-147">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="c0c75-148">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="c0c75-148">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="c0c75-149">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="c0c75-149">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c0c75-150">**wbemErrInvalidObjectPath** -2147749946 (0x8004103A)</span><span class="sxs-lookup"><span data-stu-id="c0c75-150">**wbemErrInvalidObjectPath** - 2147749946 (0x8004103A)</span></span>
</dt> <dd>

<span data-ttu-id="c0c75-151">O caminho especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="c0c75-151">Specified path was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c0c75-152">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="c0c75-152">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="c0c75-153">O objeto solicitado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="c0c75-153">Requested object could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="c0c75-154">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="c0c75-154">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="c0c75-155">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="c0c75-155">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0c75-156">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0c75-156">Remarks</span></span>

<span data-ttu-id="c0c75-157">Essa chamada retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="c0c75-157">This call returns immediately.</span></span> <span data-ttu-id="c0c75-158">O objeto solicitado e o status são retornados para o chamador por meio de um retorno de chamada entregue ao coletor especificado em *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="c0c75-158">The requested object and status are returned to the caller through a callback delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="c0c75-159">Para processar o objeto quando ele retornar, crie um *objWbemSink*. [**OnObjectReady**](swbemsink-onobjectready.md), ou um *objWbemSink*. Sub-rotina de evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="c0c75-159">To process the object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md), or an *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event subroutine.</span></span>

<span data-ttu-id="c0c75-160">Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor.</span><span class="sxs-lookup"><span data-stu-id="c0c75-160">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="c0c75-161">Isso representa riscos de segurança para seus scripts e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="c0c75-161">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="c0c75-162">Para eliminar os riscos, use semisynchronous ou comunicação síncrona.</span><span class="sxs-lookup"><span data-stu-id="c0c75-162">To eliminate the risks, use semisynchronous or synchronous communication.</span></span> <span data-ttu-id="c0c75-163">Para obter mais informações, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="c0c75-163">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0c75-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0c75-164">Requirements</span></span>



| <span data-ttu-id="c0c75-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0c75-165">Requirement</span></span> | <span data-ttu-id="c0c75-166">Valor</span><span class="sxs-lookup"><span data-stu-id="c0c75-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0c75-167">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0c75-167">Minimum supported client</span></span><br/> | <span data-ttu-id="c0c75-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0c75-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c0c75-169">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0c75-169">Minimum supported server</span></span><br/> | <span data-ttu-id="c0c75-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0c75-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c0c75-171">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c0c75-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0c75-172"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0c75-172"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0c75-173">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c0c75-173">Type library</span></span><br/>             | <dl> <span data-ttu-id="c0c75-174"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c0c75-174"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c0c75-175">DLL</span><span class="sxs-lookup"><span data-stu-id="c0c75-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0c75-176"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0c75-176"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c0c75-177">CLSID</span><span class="sxs-lookup"><span data-stu-id="c0c75-177">CLSID</span></span><br/>                    | <span data-ttu-id="c0c75-178">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="c0c75-178">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="c0c75-179">IID</span><span class="sxs-lookup"><span data-stu-id="c0c75-179">IID</span></span><br/>                      | <span data-ttu-id="c0c75-180">ISWbemServices de IID \_</span><span class="sxs-lookup"><span data-stu-id="c0c75-180">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="c0c75-181">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0c75-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0c75-182">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="c0c75-182">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="c0c75-183">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="c0c75-183">**SWbemObject**</span></span>](swbemobject.md)
</dt> </dl>

 

