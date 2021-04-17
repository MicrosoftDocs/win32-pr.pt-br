---
description: Retorna uma coleção de objetos (classes ou instâncias) chamadas de pontos de extremidade que estão associados a um objeto especificado.
ms.assetid: a78e6701-6779-4a02-b811-23b2da4f4167
ms.tgt_platform: multiple
title: Método SWbemServices. AssociatorsOf (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.AssociatorsOf
- ISWbemServices.AssociatorsOf
- ISWbemServices.AssociatorsOf
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0208ef23158d71a5174fcb6759acba1d64bd09a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770314"
---
# <a name="swbemservicesassociatorsof-method"></a><span data-ttu-id="bcbd4-103">Método SWbemServices. AssociatorsOf</span><span class="sxs-lookup"><span data-stu-id="bcbd4-103">SWbemServices.AssociatorsOf method</span></span>

<span data-ttu-id="bcbd4-104">O método **AssociatorsOf** do objeto [**SWbemServices**](swbemservices.md) retorna uma coleção de objetos (classes ou instâncias) chamada pontos de extremidade que estão associados a um objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-104">The **AssociatorsOf** method of the [**SWbemServices**](swbemservices.md) object returns a collection of objects (classes or instances) called endpoints that are associated with a specified object.</span></span> <span data-ttu-id="bcbd4-105">Esse método executa a mesma função que os ASSOCIAdores da consulta WQL executam.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-105">This method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="bcbd4-106">Esse método é chamado no modo semisynchronous por padrão.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-106">This method is called in the semisynchronous mode by default.</span></span> <span data-ttu-id="bcbd4-107">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="bcbd4-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="bcbd4-108">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="bcbd4-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bcbd4-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bcbd4-109">Syntax</span></span>


```VB
objWbemObjectSet = .AssociatorsOf( _
  ByVal strObjectPath, _
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



## <a name="parameters"></a><span data-ttu-id="bcbd4-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bcbd4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcbd4-111">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="bcbd4-111">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="bcbd4-112">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-112">Required.</span></span> <span data-ttu-id="bcbd4-113">Cadeia de caracteres que contém o caminho do objeto da classe ou instância de origem.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-113">String that contains the object path of the source class or instance.</span></span> <span data-ttu-id="bcbd4-114">Para obter mais informações, consulte [descrevendo o local de um objeto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="bcbd4-114">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="bcbd4-115">*strAssocClass* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="bcbd4-115">*strAssocClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bcbd4-116">Cadeia de caracteres que contém uma classe de associação.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-116">String that contains an association class.</span></span> <span data-ttu-id="bcbd4-117">Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem ser associados à origem por meio da classe de associação especificada ou de uma classe derivada dessa classe de associação.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-117">If specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class that is derived from this association class.</span></span>

</dd> <dt>

<span data-ttu-id="bcbd4-118">*strResultClass* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="bcbd4-118">*strResultClass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bcbd4-119">Cadeia de caracteres que contém um nome de classe.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-119">String that contains a class name.</span></span> <span data-ttu-id="bcbd4-120">Se especificado, esse parâmetro opcional indica que os pontos de extremidade retornados devem pertencer ou ser derivados da classe especificada nesse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-120">If specified, this optional parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="bcbd4-121">*strResultRole* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="bcbd4-121">*strResultRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bcbd4-122">Cadeia de caracteres que contém um nome de propriedade.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-122">String that contains a property name.</span></span> <span data-ttu-id="bcbd4-123">Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem reproduzir uma função específica em sua associação com o objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-123">If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object.</span></span> <span data-ttu-id="bcbd4-124">A função é definida pelo nome de uma propriedade especificada (que deve ser uma propriedade de referência) de uma associação.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-124">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="bcbd4-125">*strRole* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="bcbd4-125">*strRole* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bcbd4-126">Cadeia de caracteres que contém um nome de propriedade.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-126">String that contains a property name.</span></span> <span data-ttu-id="bcbd4-127">Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem participar de uma associação com o objeto de origem no qual o objeto de origem desempenha uma função específica.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-127">If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role.</span></span> <span data-ttu-id="bcbd4-128">A função é definida pelo nome de uma propriedade especificada (que deve ser uma propriedade de referência) de uma associação.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-128">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="bcbd4-129">*bClassesOnly* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="bcbd4-129">*bClassesOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bcbd4-130">Valor booliano que indica se uma lista de nomes de classe deve ser retornada em vez de instâncias reais das classes.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-130">Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="bcbd4-131">Essas são as classes às quais as instâncias de ponto de extremidade pertencem.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-131">These are the classes to which the endpoint instances belong.</span></span> <span data-ttu-id="bcbd4-132">O valor padrão para esse parâmetro é **false**.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-132">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="bcbd4-133">*bSchemaOnly* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="bcbd4-133">*bSchemaOnly* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bcbd4-134">Valor booliano que indica se a consulta se aplica ao esquema em vez dos dados.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-134">Boolean value that indicates whether the query applies to the schema rather than the data.</span></span> <span data-ttu-id="bcbd4-135">O valor padrão para esse parâmetro é **false**.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-135">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="bcbd4-136">Ele só poderá ser definido como **true** se o parâmetro *strObjectPath* especificar o caminho do objeto de uma classe.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-136">It can only be set to **TRUE** if the *strObjectPath* parameter specifies the object path of a class.</span></span> <span data-ttu-id="bcbd4-137">Quando definido como **true**, o conjunto de pontos de extremidade retornados representa classes que são adequadamente associadas à classe de origem no esquema.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-137">When set to **TRUE**, the set of returned endpoints represent classes that are suitably associated with the source class in schema.</span></span>

</dd> <dt>

<span data-ttu-id="bcbd4-138">*strRequiredAssocQualifier* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="bcbd4-138">*strRequiredAssocQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bcbd4-139">Cadeia de caracteres que contém um nome de qualificador.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-139">String that contains a qualifier name.</span></span> <span data-ttu-id="bcbd4-140">Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem ser associados ao objeto de origem por meio de uma classe de associação que inclui o qualificador especificado.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-140">If specified, this parameter indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="bcbd4-141">*strRequiredQualifier* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="bcbd4-141">*strRequiredQualifier* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bcbd4-142">Cadeia de caracteres que contém um nome de qualificador.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-142">String that contains a qualifier name.</span></span> <span data-ttu-id="bcbd4-143">Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem incluir o qualificador especificado.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-143">If specified, this parameter indicates that the returned endpoints must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="bcbd4-144">*iFlags* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="bcbd4-144">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bcbd4-145">Inteiro que especifica sinalizadores adicionais para a operação.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-145">Integer that specifies additional flags to the operation.</span></span> <span data-ttu-id="bcbd4-146">O valor padrão para esse parâmetro é **wbemFlagReturnImmediately**, que chama o método no modo semisynchronous.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-146">The default value for this parameter is **wbemFlagReturnImmediately**, which calls the method in the semisynchronous mode.</span></span> <span data-ttu-id="bcbd4-147">Esse parâmetro pode aceitar os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-147">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="bcbd4-148"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="bcbd4-148"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="bcbd4-149">Faz com que um enumerador somente de encaminhamento seja retornado.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-149">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="bcbd4-150">Enumeradores de somente encaminhamento são geralmente muito mais rápidos e usam menos memória do que enumeradores convencionais, mas não permitem chamadas para [**SWbemObject. \_ clone**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="bcbd4-150">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="bcbd4-151"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="bcbd4-151"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="bcbd4-152">Faz com que o WMI retenha ponteiros para objetos da enumeração até que o cliente libere o enumerador.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-152">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="bcbd4-153"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="bcbd4-153"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="bcbd4-154">Faz com que a chamada retorne imediatamente.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-154">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="bcbd4-155"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="bcbd4-155"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="bcbd4-156">Faz com que essa chamada seja bloqueada até que a consulta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-156">Causes this call to block until the query has completed.</span></span> <span data-ttu-id="bcbd4-157">Esse sinalizador chama o método no modo síncrono.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-157">This flag calls the method in synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="bcbd4-158"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="bcbd4-158"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="bcbd4-159">Faz com que o WMI retorne dados de alteração de classe junto com a definição de classe base.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-159">Causes WMI to return class amendment data along with the base class definition.</span></span> <span data-ttu-id="bcbd4-160">Para obter mais informações, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="bcbd4-160">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="bcbd4-161">*objwbemNamedValueSet* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="bcbd4-161">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bcbd4-162">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-162">Typically, this is undefined.</span></span> <span data-ttu-id="bcbd4-163">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-163">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="bcbd4-164">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-164">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcbd4-165">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bcbd4-165">Return value</span></span>

<span data-ttu-id="bcbd4-166">Se a chamada for bem-sucedida, um objeto [**SWbemObjectSet**](swbemobjectset.md) será retornado.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-166">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bcbd4-167">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="bcbd4-167">Error codes</span></span>

<span data-ttu-id="bcbd4-168">Após a conclusão do método **AssociatorsOf** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-168">After the completion of the **AssociatorsOf** method, the **Err** object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="bcbd4-169">Uma coleção retornada com zero elementos não é um erro.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-169">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="bcbd4-170">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="bcbd4-170">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="bcbd4-171">O usuário atual não tem permissão para exibir uma ou mais das classes retornadas pela chamada.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-171">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="bcbd4-172">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="bcbd4-172">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="bcbd4-173">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-173">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="bcbd4-174">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="bcbd4-174">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="bcbd4-175">Foi especificado um parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-175">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="bcbd4-176">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="bcbd4-176">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="bcbd4-177">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-177">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bcbd4-178">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="bcbd4-178">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="bcbd4-179">O item solicitado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-179">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bcbd4-180">Comentários</span><span class="sxs-lookup"><span data-stu-id="bcbd4-180">Remarks</span></span>

<span data-ttu-id="bcbd4-181">O método recupera as instâncias de recursos gerenciados que estão associados a um recurso especificado por meio de uma ou mais classes de associação.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-181">The method retrieves the instances of managed resources that are associated with a specified resource through one or more association classes.</span></span> <span data-ttu-id="bcbd4-182">Você fornece o caminho do objeto para o ponto de extremidade de origem e AssociatorsOf retorna os recursos gerenciados no ponto de extremidade oposto.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-182">You provide the object path for the originating endpoint, and AssociatorsOf returns the managed resources at the opposite endpoint.</span></span> <span data-ttu-id="bcbd4-183">O método AssociatorsOf executa a mesma função que os ASSOCIAdores da consulta WQL executam.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-183">The AssociatorsOf method performs the same function that the ASSOCIATORS OF WQL query performs.</span></span>

<span data-ttu-id="bcbd4-184">Para obter mais informações sobre os ASSOCIAdores de consulta WQL, instâncias de origem e pontos de extremidade, consulte [ASSOCIATORS of Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="bcbd4-184">For more information about the ASSOCIATORS OF WQL query, source instances, and endpoints, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bcbd4-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcbd4-185">Requirements</span></span>



| <span data-ttu-id="bcbd4-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcbd4-186">Requirement</span></span> | <span data-ttu-id="bcbd4-187">Valor</span><span class="sxs-lookup"><span data-stu-id="bcbd4-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcbd4-188">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bcbd4-188">Minimum supported client</span></span><br/> | <span data-ttu-id="bcbd4-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bcbd4-189">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bcbd4-190">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bcbd4-190">Minimum supported server</span></span><br/> | <span data-ttu-id="bcbd4-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bcbd4-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bcbd4-192">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bcbd4-192">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcbd4-193"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcbd4-193"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bcbd4-194">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="bcbd4-194">Type library</span></span><br/>             | <dl> <span data-ttu-id="bcbd4-195"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bcbd4-195"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bcbd4-196">DLL</span><span class="sxs-lookup"><span data-stu-id="bcbd4-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcbd4-197"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcbd4-197"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bcbd4-198">CLSID</span><span class="sxs-lookup"><span data-stu-id="bcbd4-198">CLSID</span></span><br/>                    | <span data-ttu-id="bcbd4-199">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="bcbd4-199">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="bcbd4-200">IID</span><span class="sxs-lookup"><span data-stu-id="bcbd4-200">IID</span></span><br/>                      | <span data-ttu-id="bcbd4-201">ISWbemServices de IID \_</span><span class="sxs-lookup"><span data-stu-id="bcbd4-201">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="bcbd4-202">Confira também</span><span class="sxs-lookup"><span data-stu-id="bcbd4-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcbd4-203">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="bcbd4-203">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="bcbd4-204">**SWbemObject. ASSOCIATORS\_**</span><span class="sxs-lookup"><span data-stu-id="bcbd4-204">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="bcbd4-205">**SWbemObject. AssociatorsAsync\_**</span><span class="sxs-lookup"><span data-stu-id="bcbd4-205">**SWbemObject.AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)
</dt> <dt>

[<span data-ttu-id="bcbd4-206">**SWbemServices. AssociatorsOfAsync**</span><span class="sxs-lookup"><span data-stu-id="bcbd4-206">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md)
</dt> <dt>

[<span data-ttu-id="bcbd4-207">**SWbemObject. referências\_**</span><span class="sxs-lookup"><span data-stu-id="bcbd4-207">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
</dt> <dt>

[<span data-ttu-id="bcbd4-208">**SWbemServices. References**</span><span class="sxs-lookup"><span data-stu-id="bcbd4-208">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

 




