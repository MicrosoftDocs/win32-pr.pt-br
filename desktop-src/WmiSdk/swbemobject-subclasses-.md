---
description: O método subclasses \_ do objeto SWbemObject retorna um objeto SWbemObjectSet.
ms.assetid: c17e5d4a-016f-42ae-bc11-e21a44772ce5
ms.tgt_platform: multiple
title: Método de SWbemObject.Subclasses_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Subclasses_
- ISWbemObject.Subclasses_
- ISWbemObject.Subclasses_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: efae27b26235cbf1c298c7b45de69e1cf49c8570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810626"
---
# <a name="swbemobjectsubclasses_-method"></a><span data-ttu-id="7a2fb-103">Método SWbemObject. subclasses \_</span><span class="sxs-lookup"><span data-stu-id="7a2fb-103">SWbemObject.Subclasses\_ method</span></span>

<span data-ttu-id="7a2fb-104">O método **subclasses \_** do objeto [**SWbemObject**](swbemobject.md) retorna um objeto [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="7a2fb-104">The **Subclasses\_** method of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemObjectSet**](swbemobjectset.md) object.</span></span> <span data-ttu-id="7a2fb-105">Esse objeto é uma coleção de subclasses do objeto atual, que deve ser uma classe.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-105">This object is a collection of subclasses of the current object, which must be a class.</span></span> <span data-ttu-id="7a2fb-106">Os itens na coleção retornada podem ser obtidos usando métodos de coleta padrão.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-106">Items in the returned collection can be obtained using standard collection methods.</span></span> <span data-ttu-id="7a2fb-107">Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="7a2fb-107">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

<span data-ttu-id="7a2fb-108">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="7a2fb-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7a2fb-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a2fb-109">Syntax</span></span>


```VB
objWbemObjectSet = .Subclasses_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="7a2fb-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a2fb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a2fb-111">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7a2fb-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7a2fb-112">Inteiro que determina o quão detalhado a chamada enumera.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-112">Integer that determines how detailed the call enumerates.</span></span> <span data-ttu-id="7a2fb-113">Esse parâmetro pode aceitar os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-113">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="7a2fb-114"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="7a2fb-114"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="7a2fb-115">Força a enumeração recursiva em todas as subclasses derivadas da classe pai especificada.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-115">Forces recursive enumeration into all subclasses derived from the specified parent class.</span></span> <span data-ttu-id="7a2fb-116">A própria classe pai não é retornada na enumeração.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-116">The parent class itself is not returned in the enumeration.</span></span>

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="7a2fb-117"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="7a2fb-117"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="7a2fb-118">Valor padrão para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-118">Default value for this parameter.</span></span> <span data-ttu-id="7a2fb-119">Ele força a enumeração a incluir apenas subclasses imediatas da classe pai especificada.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-119">It forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="WbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="7a2fb-120"><span id="WbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>WbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="7a2fb-120"><span id="WbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*WbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="7a2fb-121">Faz com que a chamada retorne imediatamente</span><span class="sxs-lookup"><span data-stu-id="7a2fb-121">Causes the call to return immediately</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="7a2fb-122"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="7a2fb-122"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="7a2fb-123">Faz com que essa chamada seja bloqueada até que a chamada seja concluída.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-123">Causes this call to block until the call has completed.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="7a2fb-124"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="7a2fb-124"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="7a2fb-125">Faz com que o WMI retorne dados de alteração de classe junto com a definição de classe base.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-125">Causes WMI to return class amendment data along with the base class definition.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7a2fb-126">*objwbemNamedValueSet* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7a2fb-126">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7a2fb-127">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-127">Typically, this is undefined.</span></span> <span data-ttu-id="7a2fb-128">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-128">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="7a2fb-129">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-129">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a2fb-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7a2fb-130">Return value</span></span>

<span data-ttu-id="7a2fb-131">Se a chamada for bem-sucedida, um objeto [**SWbemObjectSet**](swbemobjectset.md) será retornado.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-131">If the call is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7a2fb-132">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="7a2fb-132">Error codes</span></span>

<span data-ttu-id="7a2fb-133">Após a conclusão do método **subclasses \_** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-133">After the completion of the **Subclasses\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="7a2fb-134">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="7a2fb-134">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="7a2fb-135">O usuário atual não tem permissão para exibir uma ou mais das classes retornadas pela chamada.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-135">Current user does not have permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="7a2fb-136">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="7a2fb-136">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="7a2fb-137">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-137">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="7a2fb-138">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="7a2fb-138">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="7a2fb-139">A classe especificada não existia.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-139">Specified class did not exist.</span></span>

</dd> <dt>

<span data-ttu-id="7a2fb-140">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="7a2fb-140">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="7a2fb-141">Foi especificado um parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-141">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="7a2fb-142">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="7a2fb-142">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="7a2fb-143">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-143">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a2fb-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a2fb-144">Remarks</span></span>

<span data-ttu-id="7a2fb-145">Não é um erro para a coleção retornada ter zero elementos se não houver subclasses do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-145">It is not an error for the returned collection to have zero elements if there are no subclasses of the current object.</span></span> <span data-ttu-id="7a2fb-146">O método **subclasses \_** só funciona para objetos de classe.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-146">The **Subclasses\_** method only works for class objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a2fb-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a2fb-147">Requirements</span></span>



| <span data-ttu-id="7a2fb-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a2fb-148">Requirement</span></span> | <span data-ttu-id="7a2fb-149">Valor</span><span class="sxs-lookup"><span data-stu-id="7a2fb-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a2fb-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a2fb-150">Minimum supported client</span></span><br/> | <span data-ttu-id="7a2fb-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a2fb-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7a2fb-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a2fb-152">Minimum supported server</span></span><br/> | <span data-ttu-id="7a2fb-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a2fb-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7a2fb-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7a2fb-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a2fb-155"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a2fb-155"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7a2fb-156">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7a2fb-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="7a2fb-157"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7a2fb-157"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7a2fb-158">DLL</span><span class="sxs-lookup"><span data-stu-id="7a2fb-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a2fb-159"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a2fb-159"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7a2fb-160">CLSID</span><span class="sxs-lookup"><span data-stu-id="7a2fb-160">CLSID</span></span><br/>                    | <span data-ttu-id="7a2fb-161">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="7a2fb-161">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="7a2fb-162">IID</span><span class="sxs-lookup"><span data-stu-id="7a2fb-162">IID</span></span><br/>                      | <span data-ttu-id="7a2fb-163">ISWbemObject de IID \_</span><span class="sxs-lookup"><span data-stu-id="7a2fb-163">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="7a2fb-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a2fb-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a2fb-165">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="7a2fb-165">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="7a2fb-166">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="7a2fb-166">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

 




