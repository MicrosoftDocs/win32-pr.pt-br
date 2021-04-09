---
description: O método Associars \_ do objeto SWbemObject retorna uma coleção de objetos (classes ou instâncias) que estão associados ao objeto atual.
ms.assetid: 79f01853-c649-4cbe-b2fa-cff38fb4b733
ms.tgt_platform: multiple
title: Método de SWbemObject.Associators_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Associators_
- ISWbemObject.Associators_
- ISWbemObject.Associators_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1f9ff4536936661ece54b5bff29e500ce6e98d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922416"
---
# <a name="swbemobjectassociators_-method"></a><span data-ttu-id="5cbe1-103">Método SWbemObject. Associations \_</span><span class="sxs-lookup"><span data-stu-id="5cbe1-103">SWbemObject.Associators\_ method</span></span>

<span data-ttu-id="5cbe1-104">O método **associars \_** do objeto [**SWbemObject**](swbemobject.md) retorna uma coleção de objetos (classes ou instâncias) que estão associados ao objeto atual.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-104">The **Associators\_** method of the [**SWbemObject**](swbemobject.md) object returns a collection of objects (classes or instances) that are associated with the current object.</span></span> <span data-ttu-id="5cbe1-105">Esses objetos retornados são chamados de pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-105">These returned objects are called endpoints.</span></span> <span data-ttu-id="5cbe1-106">Esse método executa a mesma função que os ASSOCIAdores da consulta WQL executam.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-106">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="5cbe1-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5cbe1-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5cbe1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5cbe1-108">Syntax</span></span>


```VB
objWbemObjectSet = .Associators_( _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="5cbe1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5cbe1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cbe1-110">*strAssocClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5cbe1-110">*strAssocClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5cbe1-111">Cadeia de caracteres que contém uma classe de associação.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-111">String that contains an association class.</span></span> <span data-ttu-id="5cbe1-112">Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem ser associados à origem por meio da classe de associação especificada ou de uma classe derivada dessa classe de associação.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-112">If specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="5cbe1-113">*strResultClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5cbe1-113">*strResultClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5cbe1-114">Cadeia de caracteres que contém um nome de classe.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-114">String that contains a class name.</span></span> <span data-ttu-id="5cbe1-115">Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem pertencer ou ser derivados da classe especificada nesse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-115">If specified, this parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5cbe1-116">*strResultRole* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5cbe1-116">*strResultRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5cbe1-117">Cadeia de caracteres que contém um nome de propriedade.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-117">String that contains a property name.</span></span> <span data-ttu-id="5cbe1-118">Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem reproduzir uma função específica em sua associação com o objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-118">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="5cbe1-119">A função é definida pelo nome de uma propriedade especificada (que deve ser uma propriedade de referência) de uma associação.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-119">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="5cbe1-120">*strRole* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5cbe1-120">*strRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5cbe1-121">Cadeia de caracteres que contém um nome de propriedade.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-121">String that contains a property name.</span></span> <span data-ttu-id="5cbe1-122">Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem participar de uma associação com o objeto de origem no qual o objeto de origem desempenha uma função específica.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-122">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="5cbe1-123">A função é definida pelo nome de uma propriedade especificada (que deve ser uma propriedade de referência) de uma associação.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-123">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="5cbe1-124">*bClassesOnly* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5cbe1-124">*bClassesOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5cbe1-125">Valor booliano que indica se uma lista de nomes de classe deve ser retornada em vez de instâncias reais das classes.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-125">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="5cbe1-126">Essas são as classes às quais as instâncias de ponto de extremidade pertencem.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-126">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="5cbe1-127">O valor padrão para esse parâmetro é **false**.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-127">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="5cbe1-128">*bSchemaOnly* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5cbe1-128">*bSchemaOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5cbe1-129">Esse é um valor booliano que indica se a consulta se aplica ao esquema em vez dos dados.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-129">This is a Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="5cbe1-130">O valor padrão para esse parâmetro é **false**.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-130">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="5cbe1-131">Ele só poderá ser definido como **true** se o objeto no qual esse método for invocado for uma classe.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-131">It can only be set to **TRUE** if the object on which this method is invoked is a class.</span></span> <span data-ttu-id="5cbe1-132">Quando definido como **true**, o conjunto de pontos de extremidade retornados representa classes que são adequadamente associadas à classe de origem no esquema.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-132">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="5cbe1-133">*strRequiredAssocQualifier* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5cbe1-133">*strRequiredAssocQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5cbe1-134">Cadeia de caracteres que contém um nome de qualificador.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-134">String that contains a qualifier name.</span></span> <span data-ttu-id="5cbe1-135">Esse parâmetro, se especificado, indica que os pontos de extremidade retornados devem ser associados ao objeto de origem por meio de uma classe de associação que inclui o qualificador especificado.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-135">This parameter, if specified, indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="5cbe1-136">*strRequiredQualifier* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5cbe1-136">*strRequiredQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5cbe1-137">Cadeia de caracteres que contém um nome de qualificador.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-137">String that contains a qualifier name.</span></span> <span data-ttu-id="5cbe1-138">Esse parâmetro, se especificado, indica que os pontos de extremidade retornados devem incluir o qualificador especificado.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-138">This parameter, if specified, indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="5cbe1-139">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5cbe1-139">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5cbe1-140">Inteiro que especifica sinalizadores adicionais para a operação.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-140">Integer specifying additional flags to the operation.</span></span> <span data-ttu-id="5cbe1-141">O padrão para esse parâmetro é **wbemFlagReturnImmediately**, que direciona a chamada para retornar imediatamente em vez de aguardar até que a consulta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-141">The default for this parameter is **wbemFlagReturnImmediately**, which directs the call to return immediately rather than wait until the query has completed.</span></span> <span data-ttu-id="5cbe1-142">Esse parâmetro pode aceitar os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-142">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="5cbe1-143"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="5cbe1-143"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="5cbe1-144">Faz com que um enumerador somente de encaminhamento seja retornado.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-144">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="5cbe1-145">Enumeradores de somente encaminhamento são geralmente muito mais rápidos e usam menos memória do que enumeradores convencionais, mas não permitem chamadas para [**SWbemObject. \_ clone**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="5cbe1-145">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="5cbe1-146"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="5cbe1-146"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="5cbe1-147">Faz com que o WMI retenha ponteiros para objetos da enumeração até que o cliente libere o enumerador.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-147">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="5cbe1-148"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="5cbe1-148"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="5cbe1-149">Faz com que a chamada retorne imediatamente.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-149">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="5cbe1-150"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="5cbe1-150"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="5cbe1-151">Faz com que essa chamada seja bloqueada até que a consulta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-151">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="5cbe1-152"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="5cbe1-152"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="5cbe1-153">Faz com que o WMI retorne dados de alteração de classe com a definição de classe base.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-153">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="5cbe1-154">Incluir esse sinalizador torna o texto qualificador de descrição localizado disponível para classes, propriedades e métodos.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-154">Including this flag makes the localized description qualifier text available for classes, properties and methods.</span></span> <span data-ttu-id="5cbe1-155">Para obter mais informações sobre qualificadores corrigidos, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="5cbe1-155">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5cbe1-156">*objwbemNamedValueSet* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5cbe1-156">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5cbe1-157">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-157">Typically, this is undefined.</span></span> <span data-ttu-id="5cbe1-158">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-158">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="5cbe1-159">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-159">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cbe1-160">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5cbe1-160">Return value</span></span>

<span data-ttu-id="5cbe1-161">Se a chamada for bem-sucedida, um objeto [**SWbemObjectSet**](swbemobjectset.md) será retornado.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-161">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5cbe1-162">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="5cbe1-162">Error codes</span></span>

<span data-ttu-id="5cbe1-163">Após a conclusão do método **ASSOCIATORS \_** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-163">After completion of the **Associators\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="5cbe1-164">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="5cbe1-164">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="5cbe1-165">O usuário atual não tem permissão para exibir uma ou mais das classes retornadas pela chamada.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-165">The current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="5cbe1-166">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="5cbe1-166">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="5cbe1-167">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-167">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="5cbe1-168">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="5cbe1-168">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="5cbe1-169">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-169">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5cbe1-170">**wbemErrOutOfMemory** -2147749894</span><span class="sxs-lookup"><span data-stu-id="5cbe1-170">**wbemErrOutOfMemory** - 2147749894</span></span>
</dt> <dd>

<span data-ttu-id="5cbe1-171">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="5cbe1-171">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5cbe1-172">Comentários</span><span class="sxs-lookup"><span data-stu-id="5cbe1-172">Remarks</span></span>

<span data-ttu-id="5cbe1-173">Para obter mais informações sobre os ASSOCIAdores de consulta WQL associada, instâncias de origem e pontos de extremidade, consulte [ASSOCIATORS of Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="5cbe1-173">For more information about the ASSOCIATORS OF associated WQL query, source instances, and endpoints, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5cbe1-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cbe1-174">Requirements</span></span>



| <span data-ttu-id="5cbe1-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cbe1-175">Requirement</span></span> | <span data-ttu-id="5cbe1-176">Valor</span><span class="sxs-lookup"><span data-stu-id="5cbe1-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5cbe1-177">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5cbe1-177">Minimum supported client</span></span><br/> | <span data-ttu-id="5cbe1-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5cbe1-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5cbe1-179">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5cbe1-179">Minimum supported server</span></span><br/> | <span data-ttu-id="5cbe1-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5cbe1-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5cbe1-181">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5cbe1-181">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cbe1-182"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cbe1-182"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5cbe1-183">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5cbe1-183">Type library</span></span><br/>             | <dl> <span data-ttu-id="5cbe1-184"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5cbe1-184"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5cbe1-185">DLL</span><span class="sxs-lookup"><span data-stu-id="5cbe1-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5cbe1-186"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5cbe1-186"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5cbe1-187">CLSID</span><span class="sxs-lookup"><span data-stu-id="5cbe1-187">CLSID</span></span><br/>                    | <span data-ttu-id="5cbe1-188">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="5cbe1-188">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="5cbe1-189">IID</span><span class="sxs-lookup"><span data-stu-id="5cbe1-189">IID</span></span><br/>                      | <span data-ttu-id="5cbe1-190">ISWbemObject de IID \_</span><span class="sxs-lookup"><span data-stu-id="5cbe1-190">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="5cbe1-191">Confira também</span><span class="sxs-lookup"><span data-stu-id="5cbe1-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cbe1-192">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="5cbe1-192">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="5cbe1-193">**SWbemObject. referências\_**</span><span class="sxs-lookup"><span data-stu-id="5cbe1-193">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="5cbe1-194">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="5cbe1-194">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
</dt> <dt>

[<span data-ttu-id="5cbe1-195">**SWbemServices. References**</span><span class="sxs-lookup"><span data-stu-id="5cbe1-195">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

 




