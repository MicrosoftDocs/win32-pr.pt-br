---
description: O método instances \_ do objeto SWbemObject cria um enumerador que retorna as instâncias do objeto de classe atual. Esse método implementa uma consulta simples. Consultas mais complexas podem exigir o uso de SWbemServices.ExecQuery.
ms.assetid: 30402d7d-f7cb-43b5-96b5-a8a76144e32d
ms.tgt_platform: multiple
title: Método de SWbemObject.Instances_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Instances_
- ISWbemObject.Instances_
- ISWbemObject.Instances_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c573c1e94cd473d22483c7b6a2c801c3e6bcb9dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785137"
---
# <a name="swbemobjectinstances_-method"></a><span data-ttu-id="80c7d-105">Método SWbemObject. Instances \_</span><span class="sxs-lookup"><span data-stu-id="80c7d-105">SWbemObject.Instances\_ method</span></span>

<span data-ttu-id="80c7d-106">O **método \_ Instances** do objeto [**SWbemObject**](swbemobject.md) cria um enumerador que retorna as instâncias do objeto de classe atual.</span><span class="sxs-lookup"><span data-stu-id="80c7d-106">The **Instances\_** method of the [**SWbemObject**](swbemobject.md) object creates an enumerator that returns the instances of the current class object.</span></span> <span data-ttu-id="80c7d-107">Esse método implementa uma consulta simples.</span><span class="sxs-lookup"><span data-stu-id="80c7d-107">This method implements a simple query.</span></span> <span data-ttu-id="80c7d-108">Consultas mais complexas podem exigir o uso de [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="80c7d-108">More complex queries may require the use of [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span>

<span data-ttu-id="80c7d-109">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="80c7d-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="80c7d-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80c7d-110">Syntax</span></span>


```VB
objWbemObjectSet = .Instances_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="80c7d-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80c7d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80c7d-112">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="80c7d-112">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="80c7d-113">Inteiro que determina o comportamento da chamada.</span><span class="sxs-lookup"><span data-stu-id="80c7d-113">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="80c7d-114">Esse parâmetro pode aceitar os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="80c7d-114">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="80c7d-115"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="80c7d-115"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="80c7d-116">Faz com que um enumerador somente de encaminhamento seja retornado.</span><span class="sxs-lookup"><span data-stu-id="80c7d-116">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="80c7d-117">Enumeradores de somente encaminhamento são geralmente muito mais rápidos e usam menos memória do que enumeradores convencionais, mas não permitem chamadas para [**SWbemObject. \_ clone**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="80c7d-117">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="80c7d-118"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="80c7d-118"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="80c7d-119">Faz com que o WMI retenha ponteiros para objetos da enumeração até que o cliente libere o enumerador.</span><span class="sxs-lookup"><span data-stu-id="80c7d-119">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="80c7d-120"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="80c7d-120"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="80c7d-121">Valor padrão para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="80c7d-121">Default value for this parameter.</span></span> <span data-ttu-id="80c7d-122">Esse sinalizador faz com que a chamada retorne imediatamente.</span><span class="sxs-lookup"><span data-stu-id="80c7d-122">This flag causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="80c7d-123"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="80c7d-123"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* ( 0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="80c7d-124">Faz com que essa chamada seja bloqueada até que a consulta seja concluída.</span><span class="sxs-lookup"><span data-stu-id="80c7d-124">Causes this call to block until the query has completed.</span></span>

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="80c7d-125"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="80c7d-125"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="80c7d-126">Força a enumeração a incluir apenas subclasses imediatas da classe pai especificada.</span><span class="sxs-lookup"><span data-stu-id="80c7d-126">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="80c7d-127"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="80c7d-127"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="80c7d-128">Padrão para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="80c7d-128">Default for this parameter.</span></span> <span data-ttu-id="80c7d-129">Esse valor força a enumeração a incluir todas as classes na hierarquia.</span><span class="sxs-lookup"><span data-stu-id="80c7d-129">This value forces the enumeration to include all classes in the hierarchy.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="80c7d-130"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="80c7d-130"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="80c7d-131">Faz com que o WMI retorne dados de alteração de classe com a definição de classe base.</span><span class="sxs-lookup"><span data-stu-id="80c7d-131">Causes WMI to return class amendment data with the base class definition.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="80c7d-132">*objwbemNamedValueSet* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="80c7d-132">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="80c7d-133">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="80c7d-133">Typically, this is undefined.</span></span> <span data-ttu-id="80c7d-134">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="80c7d-134">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="80c7d-135">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="80c7d-135">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80c7d-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="80c7d-136">Return value</span></span>

<span data-ttu-id="80c7d-137">Se o método for bem-sucedido, um objeto [**SWbemObjectSet**](swbemobjectset.md) retornará.</span><span class="sxs-lookup"><span data-stu-id="80c7d-137">If the method is successful, an [**SWbemObjectSet**](swbemobjectset.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="80c7d-138">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="80c7d-138">Error codes</span></span>

<span data-ttu-id="80c7d-139">Após a conclusão do método **Instances \_** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="80c7d-139">After the completion of the **Instances\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="80c7d-140">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="80c7d-140">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="80c7d-141">O usuário atual não tem permissão para exibir instâncias da classe especificada.</span><span class="sxs-lookup"><span data-stu-id="80c7d-141">Current user does not have permission to view instances of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="80c7d-142">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="80c7d-142">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="80c7d-143">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="80c7d-143">Unspecified error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="80c7d-144">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="80c7d-144">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="80c7d-145">A classe especificada não é válida.</span><span class="sxs-lookup"><span data-stu-id="80c7d-145">Specified class is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="80c7d-146">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="80c7d-146">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="80c7d-147">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="80c7d-147">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="80c7d-148">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="80c7d-148">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="80c7d-149">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="80c7d-149">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="80c7d-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="80c7d-150">Remarks</span></span>

<span data-ttu-id="80c7d-151">O **método \_ Instances** só funciona para objetos de classe.</span><span class="sxs-lookup"><span data-stu-id="80c7d-151">The **Instances\_** method only works for class objects.</span></span> <span data-ttu-id="80c7d-152">Não é um erro para a coleção retornada ter zero elementos.</span><span class="sxs-lookup"><span data-stu-id="80c7d-152">It is not an error for the returned collection to have zero elements.</span></span> <span data-ttu-id="80c7d-153">O comportamento padrão para esse método é [*semisynchronous*](gloss-s.md) devido ao valor *iFlags* padrão **wbemFlagReturnImmediately**.</span><span class="sxs-lookup"><span data-stu-id="80c7d-153">The default behavior for this method is [*semisynchronous*](gloss-s.md) because of the default *IFlags* value **wbemFlagReturnImmediately**.</span></span>

## <a name="requirements"></a><span data-ttu-id="80c7d-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80c7d-154">Requirements</span></span>



| <span data-ttu-id="80c7d-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="80c7d-155">Requirement</span></span> | <span data-ttu-id="80c7d-156">Valor</span><span class="sxs-lookup"><span data-stu-id="80c7d-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80c7d-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80c7d-157">Minimum supported client</span></span><br/> | <span data-ttu-id="80c7d-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="80c7d-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="80c7d-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80c7d-159">Minimum supported server</span></span><br/> | <span data-ttu-id="80c7d-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80c7d-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="80c7d-161">parâmetro</span><span class="sxs-lookup"><span data-stu-id="80c7d-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="80c7d-162"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="80c7d-162"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="80c7d-163">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="80c7d-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="80c7d-164"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="80c7d-164"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="80c7d-165">DLL</span><span class="sxs-lookup"><span data-stu-id="80c7d-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80c7d-166"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80c7d-166"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="80c7d-167">CLSID</span><span class="sxs-lookup"><span data-stu-id="80c7d-167">CLSID</span></span><br/>                    | <span data-ttu-id="80c7d-168">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="80c7d-168">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="80c7d-169">IID</span><span class="sxs-lookup"><span data-stu-id="80c7d-169">IID</span></span><br/>                      | <span data-ttu-id="80c7d-170">ISWbemObject de IID \_</span><span class="sxs-lookup"><span data-stu-id="80c7d-170">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="80c7d-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="80c7d-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80c7d-172">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="80c7d-172">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="80c7d-173">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="80c7d-173">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

 




