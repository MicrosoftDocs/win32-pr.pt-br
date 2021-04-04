---
description: O método References \_ do objeto SWbemObject retorna uma coleção de todas as classes ou instâncias de associação que fazem referência ao objeto atual.
ms.assetid: ba02da47-0bb2-40e1-af50-1c42b4be2abd
ms.tgt_platform: multiple
title: Método de SWbemObject.References_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.References_
- ISWbemObject.References_
- ISWbemObject.References_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3349ff104a5f0730ee99735a230d265fffd1333f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837173"
---
# <a name="swbemobjectreferences_-method"></a><span data-ttu-id="eea5c-103">Método SWbemObject. References \_</span><span class="sxs-lookup"><span data-stu-id="eea5c-103">SWbemObject.References\_ method</span></span>

<span data-ttu-id="eea5c-104">O **método \_ References** do objeto [**SWbemObject**](swbemobject.md) retorna uma coleção de todas as classes ou instâncias de associação que fazem referência ao objeto atual.</span><span class="sxs-lookup"><span data-stu-id="eea5c-104">The **References\_** method of the [**SWbemObject**](swbemobject.md) object returns a collection of all association classes or instances that refer to the current object.</span></span>

<span data-ttu-id="eea5c-105">Esse método executa a mesma função [das referências da](references-of-statement.md) consulta WQL.</span><span class="sxs-lookup"><span data-stu-id="eea5c-105">This method performs the same function as the [REFERENCES OF](references-of-statement.md) WQL query.</span></span>

<span data-ttu-id="eea5c-106">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="eea5c-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="eea5c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eea5c-107">Syntax</span></span>


```VB
objWbemObjectSet = .References_( _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="eea5c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eea5c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eea5c-109">*strResultClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="eea5c-109">*strResultClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eea5c-110">Cadeia de caracteres que contém um nome de classe.</span><span class="sxs-lookup"><span data-stu-id="eea5c-110">String that contains a class name.</span></span> <span data-ttu-id="eea5c-111">Se especificado, esse parâmetro indica que os objetos de associação retornados devem pertencer ou ser derivados da classe especificada nesse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="eea5c-111">If specified, this parameter indicates that the returned association objects must belong to or be derived from the class specified in this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="eea5c-112">*strRole* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="eea5c-112">*strRole* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eea5c-113">Cadeia de caracteres que contém um nome de propriedade.</span><span class="sxs-lookup"><span data-stu-id="eea5c-113">String that contains a property name.</span></span> <span data-ttu-id="eea5c-114">Se especificado, esse parâmetro indica que os objetos de associação retornados devem ser limitados àqueles nos quais o objeto de origem desempenha uma função específica.</span><span class="sxs-lookup"><span data-stu-id="eea5c-114">If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role.</span></span> <span data-ttu-id="eea5c-115">A função é definida pelo nome de uma propriedade especificada (que deve ser uma propriedade de referência) de uma associação.</span><span class="sxs-lookup"><span data-stu-id="eea5c-115">The role is defined by the name of a specified property (which must be a reference property) of an association.</span></span>

</dd> <dt>

<span data-ttu-id="eea5c-116">*bClassesOnly* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="eea5c-116">*bClassesOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eea5c-117">Valor booliano que indica se uma lista de nomes de classe deve ser retornada em vez de instâncias reais das classes.</span><span class="sxs-lookup"><span data-stu-id="eea5c-117">Boolean value that indicates whether or not a list of class names should be returned rather than actual instances of the classes.</span></span> <span data-ttu-id="eea5c-118">Essas são as classes às quais os objetos de associação pertencem.</span><span class="sxs-lookup"><span data-stu-id="eea5c-118">These are the classes to which the association objects belong.</span></span> <span data-ttu-id="eea5c-119">O valor padrão para esse parâmetro é **false**.</span><span class="sxs-lookup"><span data-stu-id="eea5c-119">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="eea5c-120">*bSchemaOnly* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="eea5c-120">*bSchemaOnly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eea5c-121">Valor booliano que indica se a consulta se aplica ou não ao esquema, e não aos dados.</span><span class="sxs-lookup"><span data-stu-id="eea5c-121">Boolean value that indicates whether or not the query applies to the schema rather than the data.</span></span> <span data-ttu-id="eea5c-122">O valor padrão para esse parâmetro é **false**.</span><span class="sxs-lookup"><span data-stu-id="eea5c-122">The default value for this parameter is **FALSE**.</span></span> <span data-ttu-id="eea5c-123">Ele só poderá ser definido como **true** se o objeto no qual esse método for invocado for uma classe.</span><span class="sxs-lookup"><span data-stu-id="eea5c-123">It can only be set to **TRUE** if the object on which this method is invoked is a class.</span></span> <span data-ttu-id="eea5c-124">Quando definido como **true**, o conjunto de pontos de extremidade retornados representa classes que são adequadamente associadas à classe de origem no esquema.</span><span class="sxs-lookup"><span data-stu-id="eea5c-124">When set to **TRUE**, the set of returned endpoints represents classes that are suitably associated with the source class in the schema.</span></span>

</dd> <dt>

<span data-ttu-id="eea5c-125">*strRequiredQualifier* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="eea5c-125">*strRequiredQualifier* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eea5c-126">Cadeia de caracteres que contém um nome de qualificador.</span><span class="sxs-lookup"><span data-stu-id="eea5c-126">String that contains a qualifier name.</span></span> <span data-ttu-id="eea5c-127">Se especificado, esse parâmetro indica que os objetos de associação retornados devem incluir o qualificador especificado.</span><span class="sxs-lookup"><span data-stu-id="eea5c-127">If specified, this parameter indicates that the returned association objects must include the specified qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="eea5c-128">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="eea5c-128">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eea5c-129">Inteiro que especifica sinalizadores adicionais para a operação.</span><span class="sxs-lookup"><span data-stu-id="eea5c-129">Integer specifying additional flags to the operation.</span></span> <span data-ttu-id="eea5c-130">O padrão para esse parâmetro é **wbemFlagReturnImmediately**, que direciona a chamada para retornar imediatamente em vez de aguardar até que a consulta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="eea5c-130">The default for this parameter is **wbemFlagReturnImmediately**, which directs the call to return immediately rather than wait until the query has completed.</span></span> <span data-ttu-id="eea5c-131">Esse parâmetro pode aceitar os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="eea5c-131">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="eea5c-132"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="eea5c-132"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="eea5c-133">Faz com que um enumerador somente de encaminhamento seja retornado.</span><span class="sxs-lookup"><span data-stu-id="eea5c-133">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="eea5c-134">Enumeradores de somente encaminhamento são geralmente muito mais rápidos e usam menos memória do que enumeradores convencionais, mas não permitem chamadas para [**SWbemObject. \_ clone**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="eea5c-134">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="eea5c-135"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="eea5c-135"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="eea5c-136">Faz com que Instrumentação de Gerenciamento do Windows (WMI) retenha ponteiros para objetos da enumeração até que o cliente libere o enumerador.</span><span class="sxs-lookup"><span data-stu-id="eea5c-136">Causes Windows Management Instrumentation (WMI) to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="eea5c-137"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="eea5c-137"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="eea5c-138">Faz com que a chamada retorne imediatamente.</span><span class="sxs-lookup"><span data-stu-id="eea5c-138">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="eea5c-139"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="eea5c-139"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="eea5c-140">Faz com que essa chamada seja bloqueada até que a consulta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="eea5c-140">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="eea5c-141"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="eea5c-141"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="eea5c-142">Faz com que o WMI retorne dados de alteração de classe com a definição de classe base.</span><span class="sxs-lookup"><span data-stu-id="eea5c-142">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="eea5c-143">Para obter mais informações sobre qualificadores corrigidos, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="eea5c-143">For more information about amended qualifiers, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="eea5c-144">*objwbemNamedValueSet* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="eea5c-144">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eea5c-145">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="eea5c-145">Typically, this is undefined.</span></span> <span data-ttu-id="eea5c-146">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="eea5c-146">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="eea5c-147">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="eea5c-147">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eea5c-148">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eea5c-148">Return value</span></span>

<span data-ttu-id="eea5c-149">Se a chamada for bem-sucedida, um objeto [**SWbemObjectSet**](swbemobjectset.md) será retornado.</span><span class="sxs-lookup"><span data-stu-id="eea5c-149">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="eea5c-150">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="eea5c-150">Error codes</span></span>

<span data-ttu-id="eea5c-151">Após a conclusão do método **References \_** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="eea5c-151">After the completion of the **References\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="eea5c-152">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="eea5c-152">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="eea5c-153">O usuário atual não tem permissão para exibir uma ou mais das classes retornadas pela chamada.</span><span class="sxs-lookup"><span data-stu-id="eea5c-153">Current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="eea5c-154">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="eea5c-154">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="eea5c-155">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="eea5c-155">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="eea5c-156">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="eea5c-156">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="eea5c-157">Foi especificado um parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="eea5c-157">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="eea5c-158">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="eea5c-158">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="eea5c-159">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="eea5c-159">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eea5c-160">Comentários</span><span class="sxs-lookup"><span data-stu-id="eea5c-160">Remarks</span></span>

<span data-ttu-id="eea5c-161">Para obter mais informações sobre as referências de consulta WQL associada, instâncias de origem e objetos de associação, consulte [associars of Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="eea5c-161">For more information about the REFERENCES OF associated WQL query, source instances, and association objects, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eea5c-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eea5c-162">Requirements</span></span>



| <span data-ttu-id="eea5c-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="eea5c-163">Requirement</span></span> | <span data-ttu-id="eea5c-164">Valor</span><span class="sxs-lookup"><span data-stu-id="eea5c-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eea5c-165">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eea5c-165">Minimum supported client</span></span><br/> | <span data-ttu-id="eea5c-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eea5c-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eea5c-167">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eea5c-167">Minimum supported server</span></span><br/> | <span data-ttu-id="eea5c-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eea5c-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eea5c-169">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eea5c-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="eea5c-170"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="eea5c-170"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="eea5c-171">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="eea5c-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="eea5c-172"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="eea5c-172"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="eea5c-173">DLL</span><span class="sxs-lookup"><span data-stu-id="eea5c-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eea5c-174"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eea5c-174"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="eea5c-175">CLSID</span><span class="sxs-lookup"><span data-stu-id="eea5c-175">CLSID</span></span><br/>                    | <span data-ttu-id="eea5c-176">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="eea5c-176">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="eea5c-177">IID</span><span class="sxs-lookup"><span data-stu-id="eea5c-177">IID</span></span><br/>                      | <span data-ttu-id="eea5c-178">ISWbemObject de IID \_</span><span class="sxs-lookup"><span data-stu-id="eea5c-178">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="eea5c-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="eea5c-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eea5c-180">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="eea5c-180">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="eea5c-181">**SWbemObject. ASSOCIATORS\_**</span><span class="sxs-lookup"><span data-stu-id="eea5c-181">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
</dt> <dt>

[<span data-ttu-id="eea5c-182">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="eea5c-182">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
</dt> <dt>

[<span data-ttu-id="eea5c-183">**SWbemServices. References**</span><span class="sxs-lookup"><span data-stu-id="eea5c-183">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
</dt> </dl>

 

 




