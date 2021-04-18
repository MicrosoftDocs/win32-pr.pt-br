---
description: O \_ método AssociatorsAsync de SWbemObject obtém objetos (classes ou instâncias) associados ao objeto atual. Esses objetos são chamados de pontos de extremidade. Esse método executa a mesma função que os ASSOCIAdores da consulta WQL executam.
ms.assetid: c71e11cd-39a5-40d8-b279-f5ee9ff3ae04
ms.tgt_platform: multiple
title: Método de SWbemObject.AssociatorsAsync_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.AssociatorsAsync_
- ISWbemObject.AssociatorsAsync_
- ISWbemObject.AssociatorsAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: fe7a592327b6952308e44ac054fb94e21aa6d6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791562"
---
# <a name="swbemobjectassociatorsasync_-method"></a><span data-ttu-id="b4299-105">Método SWbemObject. AssociatorsAsync \_</span><span class="sxs-lookup"><span data-stu-id="b4299-105">SWbemObject.AssociatorsAsync\_ method</span></span>

<span data-ttu-id="b4299-106">O **método \_ AssociatorsAsync** de [**SWbemObject**](swbemobject.md) obtém objetos (classes ou instâncias) associados ao objeto atual.</span><span class="sxs-lookup"><span data-stu-id="b4299-106">The **AssociatorsAsync\_** method of [**SWbemObject**](swbemobject.md) obtains objects (classes or instances) that are associated with the current object.</span></span> <span data-ttu-id="b4299-107">Esses objetos são chamados de pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="b4299-107">These objects are called endpoints.</span></span> <span data-ttu-id="b4299-108">Esse método executa a mesma função que os ASSOCIAdores da consulta WQL executam.</span><span class="sxs-lookup"><span data-stu-id="b4299-108">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="b4299-109">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b4299-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b4299-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4299-110">Syntax</span></span>


```VB
SWbemObject.AssociatorsAsync_( _
  ByVal objWbemSink, _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b4299-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4299-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4299-112">*objWbemSink* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b4299-112">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4299-113">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="b4299-113">Required.</span></span> <span data-ttu-id="b4299-114">Coletor de objeto que recebe os objetos de forma assíncrona como um retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="b4299-114">Object sink that receives the objects asynchronously as a callback.</span></span>

</dd> <dt>

<span data-ttu-id="b4299-115">*strAssocClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b4299-115">*strAssocClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b4299-116">Cadeia de caracteres que contém uma classe de associação.</span><span class="sxs-lookup"><span data-stu-id="b4299-116">String that contains an association class.</span></span> <span data-ttu-id="b4299-117">Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem ser associados à origem por meio da classe de associação especificada ou de uma classe derivada dessa classe de associação.</span><span class="sxs-lookup"><span data-stu-id="b4299-117">If specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="b4299-118">*strResultClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b4299-118">*strResultClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b4299-119">Cadeia de caracteres que contém um nome de classe.</span><span class="sxs-lookup"><span data-stu-id="b4299-119">String that contains a class name.</span></span> <span data-ttu-id="b4299-120">Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem pertencer ou ser derivados da classe especificada nesse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b4299-120">If specified, this parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b4299-121">*strResultRole* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b4299-121">*strResultRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b4299-122">Cadeia de caracteres que contém um nome de propriedade.</span><span class="sxs-lookup"><span data-stu-id="b4299-122">String that contains a property name.</span></span> <span data-ttu-id="b4299-123">Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem reproduzir uma função específica em sua associação com o objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="b4299-123">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="b4299-124">A função é definida pelo nome de uma propriedade especificada (que deve ser uma propriedade de referência) de uma associação.</span><span class="sxs-lookup"><span data-stu-id="b4299-124">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="b4299-125">*strRole* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b4299-125">*strRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b4299-126">Cadeia de caracteres que contém um nome de propriedade.</span><span class="sxs-lookup"><span data-stu-id="b4299-126">String that contains a property name.</span></span> <span data-ttu-id="b4299-127">Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem participar de uma associação com o objeto de origem no qual o objeto de origem desempenha uma função específica.</span><span class="sxs-lookup"><span data-stu-id="b4299-127">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="b4299-128">A função é definida pelo nome de uma propriedade especificada (que deve ser uma propriedade de referência) de uma associação.</span><span class="sxs-lookup"><span data-stu-id="b4299-128">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="b4299-129">*bClassesOnly* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b4299-129">*bClassesOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b4299-130">Valor booliano que indica se uma lista de nomes de classe deve ser retornada em vez de instâncias reais das classes.</span><span class="sxs-lookup"><span data-stu-id="b4299-130">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="b4299-131">Essas são as classes às quais as instâncias de ponto de extremidade pertencem.</span><span class="sxs-lookup"><span data-stu-id="b4299-131">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="b4299-132">O valor padrão para esse parâmetro é **false**.</span><span class="sxs-lookup"><span data-stu-id="b4299-132">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b4299-133">*bSchemaOnly* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b4299-133">*bSchemaOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b4299-134">Valor booliano que indica se a consulta se aplica ao esquema em vez dos dados.</span><span class="sxs-lookup"><span data-stu-id="b4299-134">Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="b4299-135">O valor padrão para esse parâmetro é **false**.</span><span class="sxs-lookup"><span data-stu-id="b4299-135">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="b4299-136">Ele só poderá ser definido como **true** se o objeto no qual esse método for invocado for uma classe.</span><span class="sxs-lookup"><span data-stu-id="b4299-136">It can only be set to **TRUE** if the object on which this method is invoked is a class.</span></span> <span data-ttu-id="b4299-137">Quando definido como **true**, o conjunto de pontos de extremidade retornados representa classes que são adequadamente associadas à classe de origem no esquema.</span><span class="sxs-lookup"><span data-stu-id="b4299-137">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="b4299-138">*strRequiredAssocQualifier* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b4299-138">*strRequiredAssocQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b4299-139">Cadeia de caracteres que contém um nome de qualificador.</span><span class="sxs-lookup"><span data-stu-id="b4299-139">String that contains a qualifier name.</span></span> <span data-ttu-id="b4299-140">Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem ser associados ao objeto de origem por meio de uma classe de associação que inclui o qualificador especificado.</span><span class="sxs-lookup"><span data-stu-id="b4299-140">If specified, this parameter indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="b4299-141">*strRequiredQualifier* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b4299-141">*strRequiredQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b4299-142">Cadeia de caracteres que contém um nome de qualificador.</span><span class="sxs-lookup"><span data-stu-id="b4299-142">String that contains a qualifier name.</span></span> <span data-ttu-id="b4299-143">Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem incluir o qualificador especificado.</span><span class="sxs-lookup"><span data-stu-id="b4299-143">If specified, this parameter indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="b4299-144">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b4299-144">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b4299-145">Inteiro que especifica sinalizadores adicionais para a operação.</span><span class="sxs-lookup"><span data-stu-id="b4299-145">Integer specifying additional flags to the operation.</span></span> <span data-ttu-id="b4299-146">Esse parâmetro pode aceitar os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b4299-146">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="b4299-147"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="b4299-147"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="b4299-148">Faz com que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**SWbemSink. OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="b4299-148">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="b4299-149"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="b4299-149"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b4299-150">Impede que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="b4299-150">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="b4299-151"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="b4299-151"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="b4299-152">Faz com que o WMI retorne as descrições de classe e Propriedade localizadas.</span><span class="sxs-lookup"><span data-stu-id="b4299-152">Causes WMI to return the localized class and property descriptions.</span></span> <span data-ttu-id="b4299-153">Para obter mais informações, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="b4299-153">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b4299-154">*objwbemNamedValueSet* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b4299-154">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b4299-155">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="b4299-155">Typically, this is undefined.</span></span> <span data-ttu-id="b4299-156">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="b4299-156">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="b4299-157">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="b4299-157">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="b4299-158">*objWbemAsyncContext* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b4299-158">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b4299-159">Esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que retorna ao coletor de objeto para identificar a origem da chamada assíncrona original.</span><span class="sxs-lookup"><span data-stu-id="b4299-159">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="b4299-160">Use esse parâmetro se você estiver fazendo várias chamadas assíncronas usando o mesmo coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="b4299-160">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="b4299-161">Para usar esse parâmetro, crie um objeto **SWbemNamedValueSet** e use o método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo.</span><span class="sxs-lookup"><span data-stu-id="b4299-161">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="b4299-162">Esse objeto **SWbemNamedValueSet** é retornado para o coletor de objeto e a origem da chamada pode ser extraída usando o método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="b4299-162">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="b4299-163">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b4299-163">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4299-164">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b4299-164">Return value</span></span>

<span data-ttu-id="b4299-165">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b4299-165">This method does not return a value.</span></span> <span data-ttu-id="b4299-166">Se for bem-sucedido, o coletor receberá um evento [**OnObjectReady**](swbemsink-onobjectready.md) por instância.</span><span class="sxs-lookup"><span data-stu-id="b4299-166">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="b4299-167">Após a última instância, o coletor de objeto recebe um evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="b4299-167">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b4299-168">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="b4299-168">Error codes</span></span>

<span data-ttu-id="b4299-169">Após a conclusão do **método \_ AssociatorsAsync** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="b4299-169">After completion of the **AssociatorsAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="b4299-170">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="b4299-170">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="b4299-171">O usuário atual não tem permissão para exibir uma ou mais das classes retornadas pela chamada.</span><span class="sxs-lookup"><span data-stu-id="b4299-171">The current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="b4299-172">**wbemErrFailed** -2147449889 (0x7FFF7C21)</span><span class="sxs-lookup"><span data-stu-id="b4299-172">**wbemErrFailed** - 2147449889 (0x7FFF7C21)</span></span>
</dt> <dd>

<span data-ttu-id="b4299-173">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="b4299-173">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="b4299-174">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="b4299-174">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="b4299-175">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="b4299-175">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b4299-176">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="b4299-176">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="b4299-177">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="b4299-177">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4299-178">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4299-178">Remarks</span></span>

<span data-ttu-id="b4299-179">Essa chamada retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="b4299-179">This call returns immediately.</span></span> <span data-ttu-id="b4299-180">Os objetos e status solicitados são retornados ao chamador por meio de retornos de chamada entregues ao coletor especificado em *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="b4299-180">The requested objects and status are returned to the caller through call-backs delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="b4299-181">Para processar cada objeto quando ele chegar, crie um *objWbemSink*. Sub-rotina de evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="b4299-181">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="b4299-182">Depois que todos os objetos forem retornados, você poderá executar o processamento final em sua implementação do *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="b4299-182">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="b4299-183">Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor.</span><span class="sxs-lookup"><span data-stu-id="b4299-183">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="b4299-184">Isso representa riscos de segurança para seus scripts e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="b4299-184">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="b4299-185">Para eliminar os riscos, use a comunicação do semisynchronous ou a comunicação síncrona.</span><span class="sxs-lookup"><span data-stu-id="b4299-185">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="b4299-186">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b4299-186">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="b4299-187">Para obter mais informações sobre os ASSOCIAdores de consultas WQL associadas, instâncias de origem e pontos de extremidade, consulte [ASSOCIATORS of Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b4299-187">For more information about the ASSOCIATORS OF associated WQL queries, source instances, and endpoints, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4299-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4299-188">Requirements</span></span>



| <span data-ttu-id="b4299-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4299-189">Requirement</span></span> | <span data-ttu-id="b4299-190">Valor</span><span class="sxs-lookup"><span data-stu-id="b4299-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4299-191">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4299-191">Minimum supported client</span></span><br/> | <span data-ttu-id="b4299-192">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b4299-192">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b4299-193">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4299-193">Minimum supported server</span></span><br/> | <span data-ttu-id="b4299-194">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4299-194">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b4299-195">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b4299-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4299-196"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4299-196"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b4299-197">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b4299-197">Type library</span></span><br/>             | <dl> <span data-ttu-id="b4299-198"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b4299-198"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b4299-199">DLL</span><span class="sxs-lookup"><span data-stu-id="b4299-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4299-200"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4299-200"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b4299-201">CLSID</span><span class="sxs-lookup"><span data-stu-id="b4299-201">CLSID</span></span><br/>                    | <span data-ttu-id="b4299-202">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="b4299-202">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="b4299-203">IID</span><span class="sxs-lookup"><span data-stu-id="b4299-203">IID</span></span><br/>                      | <span data-ttu-id="b4299-204">ISWbemObject de IID \_</span><span class="sxs-lookup"><span data-stu-id="b4299-204">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="b4299-205">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4299-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4299-206">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="b4299-206">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="b4299-207">**SWbemServices. AssociatorsOfAsync**</span><span class="sxs-lookup"><span data-stu-id="b4299-207">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md)
</dt> <dt>

[<span data-ttu-id="b4299-208">**SWbemObject. referências\_**</span><span class="sxs-lookup"><span data-stu-id="b4299-208">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="b4299-209">**SWbemServices. References**</span><span class="sxs-lookup"><span data-stu-id="b4299-209">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

