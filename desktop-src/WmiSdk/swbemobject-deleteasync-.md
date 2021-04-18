---
description: O \_ método DeleteAsync de SWbemObject exclui de forma assíncrona a classe atual ou a instância atual.
ms.assetid: b8d67fa5-5217-422b-acbe-5eea6028deeb
ms.tgt_platform: multiple
title: Método de SWbemObject.DeleteAsync_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.DeleteAsync_
- ISWbemObject.DeleteAsync_
- ISWbemObject.DeleteAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7951b84a2b5d9f06061f4cefb04c797ccfea3ecd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810918"
---
# <a name="swbemobjectdeleteasync_-method"></a><span data-ttu-id="22537-103">Método SWbemObject. DeleteAsync \_</span><span class="sxs-lookup"><span data-stu-id="22537-103">SWbemObject.DeleteAsync\_ method</span></span>

<span data-ttu-id="22537-104">O **método \_ DeleteAsync** de [**SWbemObject**](swbemobject.md) exclui de forma assíncrona a classe atual ou a instância atual.</span><span class="sxs-lookup"><span data-stu-id="22537-104">The **DeleteAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously deletes either the current class or the current instance.</span></span> <span data-ttu-id="22537-105">Se um provedor dinâmico fornecer a classe ou instância, às vezes não será possível excluir esse objeto, a menos que o provedor dê suporte à exclusão de classe ou instância.</span><span class="sxs-lookup"><span data-stu-id="22537-105">If a dynamic provider supplies the class or instance, sometimes it is not possible to delete this object unless the provider supports class or instance deletion.</span></span>

<span data-ttu-id="22537-106">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="22537-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="22537-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="22537-107">Syntax</span></span>


```VB
SWbemObject.DeleteAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="22537-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="22537-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22537-109">*objWbemSink* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="22537-109">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22537-110">Coletor de objeto que retorna o resultado da operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="22537-110">Object sink that returns the outcome of the delete operation.</span></span>

</dd> <dt>

<span data-ttu-id="22537-111">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="22537-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="22537-112">Inteiro que determina o comportamento da chamada.</span><span class="sxs-lookup"><span data-stu-id="22537-112">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="22537-113">Esse parâmetro pode aceitar os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="22537-113">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="22537-114"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="22537-114"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="22537-115">Faz com que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**SWbemSink. OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="22537-115">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="22537-116"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="22537-116"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* ( 0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="22537-117">Impede que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="22537-117">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="22537-118">*objwbemNamedValueSet* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="22537-118">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="22537-119">Esse parâmetro normalmente é indefinido.</span><span class="sxs-lookup"><span data-stu-id="22537-119">This parameter is typically undefined.</span></span> <span data-ttu-id="22537-120">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="22537-120">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="22537-121">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="22537-121">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="22537-122">*objWbemAsyncContext* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="22537-122">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="22537-123">Esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que retorna ao coletor de objeto para identificar a origem da chamada assíncrona original.</span><span class="sxs-lookup"><span data-stu-id="22537-123">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="22537-124">Use esse parâmetro se você estiver fazendo várias chamadas assíncronas usando o mesmo coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="22537-124">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="22537-125">Para usar esse parâmetro, crie um objeto **SWbemNamedValueSet** e use o método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo.</span><span class="sxs-lookup"><span data-stu-id="22537-125">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="22537-126">Esse objeto **SWbemNamedValueSet** é retornado para o coletor de objeto e a origem da chamada pode ser extraída usando o método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="22537-126">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="22537-127">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="22537-127">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22537-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="22537-128">Return value</span></span>

<span data-ttu-id="22537-129">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="22537-129">This method does not return a value.</span></span> <span data-ttu-id="22537-130">Se essa chamada for bem-sucedida, o resultado da operação de exclusão será fornecido por meio do coletor de objeto fornecido.</span><span class="sxs-lookup"><span data-stu-id="22537-130">If this call is successful, the result of the delete operation is provided through the supplied object sink.</span></span>

## <a name="error-codes"></a><span data-ttu-id="22537-131">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="22537-131">Error codes</span></span>

<span data-ttu-id="22537-132">Após a conclusão do método **DeleteAsync \_** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="22537-132">After the completion of the **DeleteAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="22537-133">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="22537-133">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="22537-134">O contexto atual não tem direitos de segurança adequados para excluir o objeto.</span><span class="sxs-lookup"><span data-stu-id="22537-134">Current context does not have adequate security rights to delete the object.</span></span>

</dd> <dt>

<span data-ttu-id="22537-135">**wbemErrFailed** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="22537-135">**wbemErrFailed** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="22537-136">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="22537-136">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="22537-137">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="22537-137">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="22537-138">A classe especificada não existe.</span><span class="sxs-lookup"><span data-stu-id="22537-138">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="22537-139">**wbemErrInvalidOperation** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="22537-139">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="22537-140">O objeto não pode ser excluído.</span><span class="sxs-lookup"><span data-stu-id="22537-140">Object cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="22537-141">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="22537-141">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="22537-142">O objeto não existia.</span><span class="sxs-lookup"><span data-stu-id="22537-142">Object did not exist.</span></span>

</dd> <dt>

<span data-ttu-id="22537-143">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="22537-143">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="22537-144">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="22537-144">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="22537-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="22537-145">Remarks</span></span>

<span data-ttu-id="22537-146">Essa chamada retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="22537-146">This call returns immediately.</span></span> <span data-ttu-id="22537-147">O status é retornado para o chamador por meio de um retorno de chamada entregue ao coletor especificado em *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="22537-147">The status is returned to the caller through a callback delivered to the sink that is specified in *objWbemSink*.</span></span>

<span data-ttu-id="22537-148">Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor.</span><span class="sxs-lookup"><span data-stu-id="22537-148">An asynchronous callback allows a nonauthenticated user to provide data to the sink.</span></span> <span data-ttu-id="22537-149">Isso representa riscos de segurança para seus scripts e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="22537-149">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="22537-150">Para eliminar os riscos, use a comunicação do semisynchronous ou a comunicação síncrona.</span><span class="sxs-lookup"><span data-stu-id="22537-150">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="22537-151">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="22537-151">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="22537-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22537-152">Requirements</span></span>



| <span data-ttu-id="22537-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="22537-153">Requirement</span></span> | <span data-ttu-id="22537-154">Valor</span><span class="sxs-lookup"><span data-stu-id="22537-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22537-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22537-155">Minimum supported client</span></span><br/> | <span data-ttu-id="22537-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="22537-156">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="22537-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22537-157">Minimum supported server</span></span><br/> | <span data-ttu-id="22537-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="22537-158">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="22537-159">parâmetro</span><span class="sxs-lookup"><span data-stu-id="22537-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="22537-160"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="22537-160"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="22537-161">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="22537-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="22537-162"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="22537-162"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="22537-163">DLL</span><span class="sxs-lookup"><span data-stu-id="22537-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22537-164"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22537-164"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="22537-165">CLSID</span><span class="sxs-lookup"><span data-stu-id="22537-165">CLSID</span></span><br/>                    | <span data-ttu-id="22537-166">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="22537-166">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="22537-167">IID</span><span class="sxs-lookup"><span data-stu-id="22537-167">IID</span></span><br/>                      | <span data-ttu-id="22537-168">ISWbemObject de IID \_</span><span class="sxs-lookup"><span data-stu-id="22537-168">IID\_ISWbemObject</span></span><br/>                                                            |



 

