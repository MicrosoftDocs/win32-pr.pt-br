---
description: Retorna todas as classes de associação ou instâncias que se referem a uma classe ou instância de origem específica.
ms.assetid: 2ad66ea1-b8f0-4b6b-b68f-29496afbe4bf
ms.tgt_platform: multiple
title: Método SWbemServices. ReferencesToAsync (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ReferencesToAsync
- ISWbemServices.ReferencesToAsync
- ISWbemServices.ReferencesToAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 64a8b9b336a1e7aa6007b17d2e878f1ace5e6163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785125"
---
# <a name="swbemservicesreferencestoasync-method"></a><span data-ttu-id="4c4a0-103">Método SWbemServices. ReferencesToAsync</span><span class="sxs-lookup"><span data-stu-id="4c4a0-103">SWbemServices.ReferencesToAsync method</span></span>

<span data-ttu-id="4c4a0-104">O método **ReferencesToAsync** do objeto [**SWbemServices**](swbemservices.md) retorna todas as classes ou instâncias de associação que se referem a uma classe ou instância de origem específica.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-104">The **ReferencesToAsync** method of the [**SWbemServices**](swbemservices.md) object returns all association classes or instances that refer to a specific source class or instance.</span></span> <span data-ttu-id="4c4a0-105">Esse método executa a mesma função que as [referências da](references-of-statement.md) consulta WQL executa.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-105">This method performs the same function that the [REFERENCES OF](references-of-statement.md) WQL query performs.</span></span>

<span data-ttu-id="4c4a0-106">Para obter mais informações sobre o modo assíncrono, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="4c4a0-106">For more information about the asynchronous mode, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="4c4a0-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="4c4a0-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4c4a0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c4a0-108">Syntax</span></span>


```VB
SWbemServices.ReferencesToAsync( _
  ByVal ObjWbemSink, _
  ByVal strObjectPath, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="4c4a0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c4a0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c4a0-110">*ObjWbemSink*</span><span class="sxs-lookup"><span data-stu-id="4c4a0-110">*ObjWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="4c4a0-111">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-111">Required.</span></span> <span data-ttu-id="4c4a0-112">Coletor de objeto que recebe os objetos de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-112">Object sink that receives the objects asynchronously.</span></span> <span data-ttu-id="4c4a0-113">Crie um objeto [**SWbemSink**](swbemsink.md) para receber os objetos.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-113">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="4c4a0-114">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="4c4a0-114">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="4c4a0-115">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-115">Required.</span></span> <span data-ttu-id="4c4a0-116">Cadeia de caracteres que contém o caminho do objeto da origem para esse método.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-116">String that contains the object path of the source for this method.</span></span> <span data-ttu-id="4c4a0-117">Para obter mais informações, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="4c4a0-117">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c4a0-118">*strResultClass* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="4c4a0-118">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4c4a0-119">Cadeia de caracteres que contém um nome de classe.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-119">String that contains a class name.</span></span> <span data-ttu-id="4c4a0-120">Se especificado, esse parâmetro indica que os objetos de associação retornados devem pertencer ou ser derivados da classe especificada nesse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-120">If specified, this parameter indicates that the returned association objects must belong to or be derived from the class that is specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4c4a0-121">*strRole* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="4c4a0-121">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4c4a0-122">Cadeia de caracteres que contém um nome de propriedade.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-122">String that contains a property name.</span></span> <span data-ttu-id="4c4a0-123">Se especificado, esse parâmetro indica que os objetos de associação retornados devem ser limitados àqueles nos quais o objeto de origem desempenha uma função específica.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-123">If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role.</span></span> <span data-ttu-id="4c4a0-124">A função é definida pelo nome de uma propriedade de referência especificada de uma associação.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-124">The role is defined by the name of a specified reference property of an association.</span></span>

</dd> <dt>

<span data-ttu-id="4c4a0-125">*bClassesOnly* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="4c4a0-125">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4c4a0-126">Valor booliano que indica se uma lista de nomes de classe deve ser retornada em vez de instâncias reais das classes.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-126">Boolean value that indicates whether or not a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="4c4a0-127">Essas são as classes às quais os objetos de associação pertencem.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-127">These are the classes to which the association objects belong.</span></span> <span data-ttu-id="4c4a0-128">O valor padrão para esse parâmetro é **false**.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-128">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4c4a0-129">*bSchemaOnly* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="4c4a0-129">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4c4a0-130">Valor booliano que indica se a consulta se aplica ou não ao esquema, e não aos dados.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-130">Boolean value that indicates whether or not the query applies to the schema rather than the data.</span></span> <span data-ttu-id="4c4a0-131">O valor padrão para esse parâmetro é **false**.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-131">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="4c4a0-132">Ele só poderá ser definido como **true** se o parâmetro *strObjectPath* especificar o caminho do objeto de uma classe.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-132">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="4c4a0-133">Quando definido como **true**, o conjunto de pontos de extremidade retornados representa as classes associadas à classe de origem no esquema.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-133">When set to **TRUE**, the set of returned endpoints represents classes that are associated with the source class in schema.</span></span>

</dd> <dt>

<span data-ttu-id="4c4a0-134">*strRequiredQualifier* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="4c4a0-134">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4c4a0-135">Cadeia de caracteres que contém um nome de qualificador.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-135">String that contains a qualifier name.</span></span> <span data-ttu-id="4c4a0-136">Se especificado, esse parâmetro indica que os objetos de associação retornados devem incluir o qualificador especificado.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-136">If specified, this parameter indicates that the returned association objects must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="4c4a0-137">*iFlags* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="4c4a0-137">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4c4a0-138">Inteiro que especifica sinalizadores adicionais para a operação.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-138">Integer that specifies additional flags to the operation.</span></span> <span data-ttu-id="4c4a0-139">O padrão para esse parâmetro é **wbemFlagBidirectional**.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-139">The default for this parameter is **wbemFlagBidirectional**.</span></span> <span data-ttu-id="4c4a0-140">Esse parâmetro pode aceitar os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-140">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="4c4a0-141"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="4c4a0-141"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="4c4a0-142">Faz com que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-142">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="4c4a0-143"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="4c4a0-143"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="4c4a0-144">Impede que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-144">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="4c4a0-145"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="4c4a0-145"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="4c4a0-146">Faz com que Instrumentação de Gerenciamento do Windows (WMI) retorne dados de alteração de classe junto com a definição de classe base.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-146">Causes Windows Management Instrumentation (WMI) to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="4c4a0-147">Para obter mais informações, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="4c4a0-147">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4c4a0-148">*objWbemNamedValueSet* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="4c4a0-148">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4c4a0-149">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-149">Typically, this is undefined.</span></span> <span data-ttu-id="4c4a0-150">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-150">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="4c4a0-151">Um provedor que dá suporte ou exige informações de contexto deve documentar os nomes de valores reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-151">A provider that supports or requires context information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="4c4a0-152">*objWbemAsyncContext* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="4c4a0-152">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4c4a0-153">Esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que retorna ao coletor de objeto para identificar a origem da chamada assíncrona original.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-153">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="4c4a0-154">Use esse parâmetro para fazer várias chamadas assíncronas usando o mesmo coletor de objeto.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-154">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="4c4a0-155">Para usar esse parâmetro, crie um objeto **SWbemNamedValueSet** e use o método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-155">To use this parameter, create an **SWbemNamedValueSet** object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="4c4a0-156">Esse objeto **SWbemNamedValueSet** é retornado para o coletor de objeto e a origem da chamada pode ser extraída usando o método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="4c4a0-156">This **SWbemNamedValueSet** object is returned to the object sink, and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="4c4a0-157">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="4c4a0-157">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c4a0-158">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4c4a0-158">Return value</span></span>

<span data-ttu-id="4c4a0-159">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-159">This method does not return a value.</span></span> <span data-ttu-id="4c4a0-160">Se for bem-sucedido, o coletor receberá um evento [**OnObjectReady**](swbemsink-onobjectready.md) por instância.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-160">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="4c4a0-161">Após a última instância, o coletor de objeto recebe um evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="4c4a0-161">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4c4a0-162">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="4c4a0-162">Error codes</span></span>

<span data-ttu-id="4c4a0-163">Após a conclusão do método **ReferencesToAsync** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-163">After the completion of the **ReferencesToAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="4c4a0-164">Uma coleção retornada com zero elementos não é um erro.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-164">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="4c4a0-165">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="4c4a0-165">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="4c4a0-166">O usuário atual não tem permissão para exibir uma ou mais das classes retornadas pela chamada.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-166">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="4c4a0-167">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="4c4a0-167">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="4c4a0-168">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-168">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="4c4a0-169">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="4c4a0-169">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="4c4a0-170">Foi especificado um parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-170">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="4c4a0-171">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="4c4a0-171">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="4c4a0-172">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-172">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4c4a0-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c4a0-173">Remarks</span></span>

<span data-ttu-id="4c4a0-174">Essa chamada retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-174">This call returns immediately.</span></span> <span data-ttu-id="4c4a0-175">Os objetos e status solicitados são retornados ao chamador por meio de retornos de chamada entregues ao coletor especificado em *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-175">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="4c4a0-176">Para processar cada objeto quando ele retornar, crie um *objWbemSink*. Sub-rotina de evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="4c4a0-176">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="4c4a0-177">Depois que todos os objetos forem retornados, você poderá executar o processamento final em sua implementação do *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="4c4a0-177">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="4c4a0-178">Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-178">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="4c4a0-179">Isso representa riscos de segurança para seus scripts e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="4c4a0-179">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="4c4a0-180">Para eliminar os riscos, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="4c4a0-180">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c4a0-181">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c4a0-181">Requirements</span></span>



| <span data-ttu-id="4c4a0-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c4a0-182">Requirement</span></span> | <span data-ttu-id="4c4a0-183">Valor</span><span class="sxs-lookup"><span data-stu-id="4c4a0-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c4a0-184">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c4a0-184">Minimum supported client</span></span><br/> | <span data-ttu-id="4c4a0-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4c4a0-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4c4a0-186">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c4a0-186">Minimum supported server</span></span><br/> | <span data-ttu-id="4c4a0-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c4a0-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4c4a0-188">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4c4a0-188">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c4a0-189"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c4a0-189"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4c4a0-190">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4c4a0-190">Type library</span></span><br/>             | <dl> <span data-ttu-id="4c4a0-191"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4c4a0-191"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4c4a0-192">DLL</span><span class="sxs-lookup"><span data-stu-id="4c4a0-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c4a0-193"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c4a0-193"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4c4a0-194">CLSID</span><span class="sxs-lookup"><span data-stu-id="4c4a0-194">CLSID</span></span><br/>                    | <span data-ttu-id="4c4a0-195">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="4c4a0-195">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="4c4a0-196">IID</span><span class="sxs-lookup"><span data-stu-id="4c4a0-196">IID</span></span><br/>                      | <span data-ttu-id="4c4a0-197">ISWbemServices de IID \_</span><span class="sxs-lookup"><span data-stu-id="4c4a0-197">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="4c4a0-198">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c4a0-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c4a0-199">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="4c4a0-199">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="4c4a0-200">**SWbemObject. ASSOCIATORS\_**</span><span class="sxs-lookup"><span data-stu-id="4c4a0-200">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="4c4a0-201">**SWbemObject. referências\_**</span><span class="sxs-lookup"><span data-stu-id="4c4a0-201">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="4c4a0-202">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="4c4a0-202">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

