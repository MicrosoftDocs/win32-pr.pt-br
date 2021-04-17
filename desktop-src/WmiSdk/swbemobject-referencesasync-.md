---
description: O \_ método ReferencesAsync de SWbemObject fornece uma coleção de todas as classes ou instâncias de associação que se referem ao objeto atual. Esse método executa a mesma função que as referências WQL de consulta executam.
ms.assetid: 44989726-3f68-453b-b9f5-e76fb0fbb152
ms.tgt_platform: multiple
title: Método de SWbemObject.ReferencesAsync_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ReferencesAsync_
- ISWbemObject.ReferencesAsync_
- ISWbemObject.ReferencesAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: aa4b85475a0dc9f736254c8f207469a52897b7ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761843"
---
# <a name="swbemobjectreferencesasync_-method"></a><span data-ttu-id="315f1-104">Método SWbemObject. ReferencesAsync \_</span><span class="sxs-lookup"><span data-stu-id="315f1-104">SWbemObject.ReferencesAsync\_ method</span></span>

<span data-ttu-id="315f1-105">O **método \_ ReferencesAsync** de [**SWbemObject**](swbemobject.md) fornece uma coleção de todas as classes ou instâncias de associação que se referem ao objeto atual.</span><span class="sxs-lookup"><span data-stu-id="315f1-105">The **ReferencesAsync\_** method of [**SWbemObject**](swbemobject.md) supplies a collection of all association classes or instances that refer to the current object.</span></span> <span data-ttu-id="315f1-106">Esse método executa a mesma função que as [referências WQL de](references-of-statement.md) consulta executam.</span><span class="sxs-lookup"><span data-stu-id="315f1-106">This method performs the same function that the WQL [REFERENCES OF](references-of-statement.md) query performs.</span></span>

<span data-ttu-id="315f1-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="315f1-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="315f1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="315f1-108">Syntax</span></span>


```VB
SWbemObject.ReferencesAsync_( _
  ByVal objWbemSink, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="315f1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="315f1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="315f1-110">*objWbemSink* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="315f1-110">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="315f1-111">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="315f1-111">Required.</span></span> <span data-ttu-id="315f1-112">Coletor de objeto que recebe os objetos de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="315f1-112">Object sink that receives the objects asynchronously.</span></span>

</dd> <dt>

<span data-ttu-id="315f1-113">*strResultClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="315f1-113">*strResultClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="315f1-114">Cadeia de caracteres que contém um nome de classe.</span><span class="sxs-lookup"><span data-stu-id="315f1-114">String that contains a class name.</span></span> <span data-ttu-id="315f1-115">Se especificado, esse parâmetro indica que os objetos de associação retornados devem pertencer ou ser derivados da classe especificada nesse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="315f1-115">If specified, this parameter indicates that the returned association objects must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="315f1-116">*strRole* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="315f1-116">*strRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="315f1-117">Cadeia de caracteres que contém um nome de propriedade.</span><span class="sxs-lookup"><span data-stu-id="315f1-117">String that contains a property name.</span></span> <span data-ttu-id="315f1-118">Se especificado, esse parâmetro indica que os objetos de associação retornados devem ser limitados àqueles nos quais o objeto de origem desempenha uma função específica.</span><span class="sxs-lookup"><span data-stu-id="315f1-118">If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role.</span></span> <span data-ttu-id="315f1-119">O nome de uma propriedade de referência especificada define a função de uma associação.</span><span class="sxs-lookup"><span data-stu-id="315f1-119">The name of a specified reference property defines the role of an association.</span></span>

</dd> <dt>

<span data-ttu-id="315f1-120">*bClassesOnly* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="315f1-120">*bClassesOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="315f1-121">Valor booliano que indica se uma lista de nomes de classe deve ser retornada em vez de instâncias reais das classes.</span><span class="sxs-lookup"><span data-stu-id="315f1-121">Boolean value that indicates whether or not a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="315f1-122">Essas são as classes às quais os objetos de associação pertencem.</span><span class="sxs-lookup"><span data-stu-id="315f1-122">These are the classes to which the association objects belong.</span></span> <span data-ttu-id="315f1-123">O valor padrão para esse parâmetro é **false**.</span><span class="sxs-lookup"><span data-stu-id="315f1-123">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="315f1-124">*bSchemaOnly* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="315f1-124">*bSchemaOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="315f1-125">Valor booliano que indica se a consulta se aplica ou não ao esquema, e não aos dados.</span><span class="sxs-lookup"><span data-stu-id="315f1-125">Boolean value that indicates whether or not the query applies to the schema rather than the data.</span></span> <span data-ttu-id="315f1-126">O valor padrão para esse parâmetro é **false**.</span><span class="sxs-lookup"><span data-stu-id="315f1-126">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="315f1-127">Ele só poderá ser definido como **true** se o objeto no qual esse método for invocado for uma classe.</span><span class="sxs-lookup"><span data-stu-id="315f1-127">It can only be set to **TRUE** if the object on which this method is invoked is a class.</span></span> <span data-ttu-id="315f1-128">Quando definido como **true**, o conjunto de pontos de extremidade retornados representa classes que são adequadamente associadas à classe de origem no esquema.</span><span class="sxs-lookup"><span data-stu-id="315f1-128">When set to **TRUE**, the set of returned endpoints represents classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="315f1-129">*strRequiredQualifier* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="315f1-129">*strRequiredQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="315f1-130">Cadeia de caracteres que contém um nome de qualificador.</span><span class="sxs-lookup"><span data-stu-id="315f1-130">String that contains a qualifier name.</span></span> <span data-ttu-id="315f1-131">Se especificado, esse parâmetro indica que os objetos de associação retornados devem incluir o qualificador especificado.</span><span class="sxs-lookup"><span data-stu-id="315f1-131">If specified, this parameter indicates that the returned association objects must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="315f1-132">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="315f1-132">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="315f1-133">Inteiro que especifica sinalizadores adicionais para a operação.</span><span class="sxs-lookup"><span data-stu-id="315f1-133">Integer specifying additional flags to the operation.</span></span> <span data-ttu-id="315f1-134">Esse parâmetro pode aceitar os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="315f1-134">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="315f1-135"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="315f1-135"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="315f1-136">Faz com que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**SWbemSink. OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="315f1-136">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="315f1-137"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="315f1-137"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="315f1-138">Impede que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="315f1-138">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="315f1-139"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="315f1-139"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="315f1-140">Faz com que Instrumentação de Gerenciamento do Windows (WMI) retorne dados de alteração de classe com a definição de classe base.</span><span class="sxs-lookup"><span data-stu-id="315f1-140">Causes Windows Management Instrumentation (WMI) to return class amendment data with the base class definition.</span></span> <span data-ttu-id="315f1-141">Para obter mais informações, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="315f1-141">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="315f1-142">*objwbemNamedValueSet* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="315f1-142">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="315f1-143">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="315f1-143">Typically, this is undefined.</span></span> <span data-ttu-id="315f1-144">Caso contrário, esse é um objeto [SWbemNamedValueSet](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="315f1-144">Otherwise, this is an [SWbemNamedValueSet](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="315f1-145">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="315f1-145">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="315f1-146">*objWbemAsyncContext* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="315f1-146">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="315f1-147">Esse é um objeto [SWbemNamedValueSet](swbemnamedvalueset.md) que retorna ao coletor de objeto para identificar a origem da chamada assíncrona original.</span><span class="sxs-lookup"><span data-stu-id="315f1-147">This is an [SWbemNamedValueSet](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="315f1-148">Use esse parâmetro se você estiver fazendo várias chamadas assíncronas usando o mesmo coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="315f1-148">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="315f1-149">Para usar esse parâmetro, crie um objeto SWbemNamedValueSet e use o método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo.</span><span class="sxs-lookup"><span data-stu-id="315f1-149">To use this parameter, create an SWbemNamedValueSet object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="315f1-150">Esse objeto SWbemNamedValueSet é retornado para o coletor de objeto e a origem da chamada pode ser extraída usando o método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="315f1-150">This SWbemNamedValueSet object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="315f1-151">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="315f1-151">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="315f1-152">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="315f1-152">Return value</span></span>

<span data-ttu-id="315f1-153">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="315f1-153">This method does not return a value.</span></span> <span data-ttu-id="315f1-154">Se for bem-sucedido, o coletor receberá um evento [**OnObjectReady**](swbemsink-onobjectready.md) por instância.</span><span class="sxs-lookup"><span data-stu-id="315f1-154">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="315f1-155">Após a última instância, o coletor de objeto recebe um evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="315f1-155">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="315f1-156">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="315f1-156">Error codes</span></span>

<span data-ttu-id="315f1-157">Após a conclusão do método **ReferencesAsync \_** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="315f1-157">After the completion of the **ReferencesAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="315f1-158">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="315f1-158">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="315f1-159">O usuário atual não tem permissão para exibir uma ou mais das classes retornadas pela chamada.</span><span class="sxs-lookup"><span data-stu-id="315f1-159">Current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="315f1-160">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="315f1-160">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="315f1-161">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="315f1-161">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="315f1-162">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="315f1-162">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="315f1-163">Foi especificado um parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="315f1-163">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="315f1-164">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="315f1-164">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="315f1-165">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="315f1-165">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="315f1-166">Comentários</span><span class="sxs-lookup"><span data-stu-id="315f1-166">Remarks</span></span>

<span data-ttu-id="315f1-167">Essa chamada retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="315f1-167">This call returns immediately.</span></span> <span data-ttu-id="315f1-168">Os objetos e status solicitados são retornados ao chamador por meio de retornos de chamada entregues ao coletor especificado em *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="315f1-168">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="315f1-169">Para processar cada objeto quando ele chegar, crie um *objWbemSink*. Sub-rotina de evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="315f1-169">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="315f1-170">Depois que todos os objetos forem retornados, você poderá executar o processamento final em sua implementação do *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="315f1-170">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="315f1-171">Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor.</span><span class="sxs-lookup"><span data-stu-id="315f1-171">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="315f1-172">Isso representa riscos de segurança para seus scripts e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="315f1-172">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="315f1-173">Para eliminar os riscos, use a comunicação do semisynchronous ou a comunicação síncrona.</span><span class="sxs-lookup"><span data-stu-id="315f1-173">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="315f1-174">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="315f1-174">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="315f1-175">Para obter mais informações sobre as referências de consulta WQL associada, instâncias de origem e objetos de associação, consulte [associars of Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="315f1-175">For more information about the REFERENCES OF associated WQL query, source instances, and association objects, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="315f1-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="315f1-176">Requirements</span></span>



| <span data-ttu-id="315f1-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="315f1-177">Requirement</span></span> | <span data-ttu-id="315f1-178">Valor</span><span class="sxs-lookup"><span data-stu-id="315f1-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="315f1-179">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="315f1-179">Minimum supported client</span></span><br/> | <span data-ttu-id="315f1-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="315f1-180">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="315f1-181">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="315f1-181">Minimum supported server</span></span><br/> | <span data-ttu-id="315f1-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="315f1-182">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="315f1-183">parâmetro</span><span class="sxs-lookup"><span data-stu-id="315f1-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="315f1-184"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="315f1-184"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="315f1-185">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="315f1-185">Type library</span></span><br/>             | <dl> <span data-ttu-id="315f1-186"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="315f1-186"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="315f1-187">DLL</span><span class="sxs-lookup"><span data-stu-id="315f1-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="315f1-188"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="315f1-188"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="315f1-189">CLSID</span><span class="sxs-lookup"><span data-stu-id="315f1-189">CLSID</span></span><br/>                    | <span data-ttu-id="315f1-190">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="315f1-190">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="315f1-191">IID</span><span class="sxs-lookup"><span data-stu-id="315f1-191">IID</span></span><br/>                      | <span data-ttu-id="315f1-192">ISWbemObject de IID \_</span><span class="sxs-lookup"><span data-stu-id="315f1-192">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="315f1-193">Confira também</span><span class="sxs-lookup"><span data-stu-id="315f1-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="315f1-194">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="315f1-194">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="315f1-195">**SWbemObject. ASSOCIATORS\_**</span><span class="sxs-lookup"><span data-stu-id="315f1-195">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="315f1-196">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="315f1-196">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
</dt> <dt>

[<span data-ttu-id="315f1-197">**SWbemServices. References**</span><span class="sxs-lookup"><span data-stu-id="315f1-197">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> <dt>

[<span data-ttu-id="315f1-198">**SWbemServices. ReferencesToAsync**</span><span class="sxs-lookup"><span data-stu-id="315f1-198">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencestoasync.md)
</dt> </dl>

 

