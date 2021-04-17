---
description: Exclui a classe ou instância especificada no caminho do objeto.
ms.assetid: f5ed170e-d002-4dd9-b8b6-b764a7a41a27
ms.tgt_platform: multiple
title: Método SWbemServices. DeleteAsync (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.DeleteAsync
- ISWbemServices.DeleteAsync
- ISWbemServices.DeleteAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: adc8811c11f67b9fc92628740bd15df2086948d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761553"
---
# <a name="swbemservicesdeleteasync-method"></a><span data-ttu-id="6a26f-103">Método SWbemServices. DeleteAsync</span><span class="sxs-lookup"><span data-stu-id="6a26f-103">SWbemServices.DeleteAsync method</span></span>

<span data-ttu-id="6a26f-104">O método **DeleteAsync** do objeto [**SWbemServices**](swbemservices.md) exclui a classe ou a instância especificada no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="6a26f-104">The **DeleteAsync** method of the [**SWbemServices**](swbemservices.md) object deletes the class or instance specified in the object path.</span></span> <span data-ttu-id="6a26f-105">A chamada para **DeleteAsync** retorna imediatamente e os resultados e o status são retornados para o chamador por meio de eventos entregues ao coletor especificado em *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="6a26f-105">The call to **DeleteAsync** returns immediately and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="6a26f-106">Para obter mais informações sobre como criar um coletor, consulte [recebendo um evento WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="6a26f-106">For more information about creating a sink, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span> <span data-ttu-id="6a26f-107">Você só pode excluir objetos no namespace ao qual você está conectado.</span><span class="sxs-lookup"><span data-stu-id="6a26f-107">You can only delete objects in the namespace to which you are connected.</span></span>

<span data-ttu-id="6a26f-108">Se um provedor dinâmico fornecer a classe ou instância, às vezes não será possível excluir esse objeto, a menos que o provedor dê suporte à exclusão de classe ou instância.</span><span class="sxs-lookup"><span data-stu-id="6a26f-108">If a dynamic provider supplies the class or instance, sometimes it is not possible to delete this object unless the provider supports class or instance deletion.</span></span>

<span data-ttu-id="6a26f-109">O método é chamado no modo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="6a26f-109">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="6a26f-110">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="6a26f-110">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="6a26f-111">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="6a26f-111">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6a26f-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a26f-112">Syntax</span></span>


```VB
SWbemServices.DeleteAsync( _
  [ ByVal ObjWbemSink ], _
  ByVal strObjectPath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="6a26f-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a26f-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a26f-114">*ObjWbemSink* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="6a26f-114">*ObjWbemSink* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6a26f-115">Coletor de objeto que recebe os resultados da exclusão.</span><span class="sxs-lookup"><span data-stu-id="6a26f-115">Object sink that receives the results of the deletion.</span></span> <span data-ttu-id="6a26f-116">Crie um objeto [**SWbemSink**](swbemsink.md) para receber os objetos.</span><span class="sxs-lookup"><span data-stu-id="6a26f-116">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="6a26f-117">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="6a26f-117">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="6a26f-118">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="6a26f-118">Required.</span></span> <span data-ttu-id="6a26f-119">Cadeia de caracteres que contém o caminho do objeto para o objeto que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="6a26f-119">String that contains the object path to the object that you want to delete.</span></span> <span data-ttu-id="6a26f-120">Para obter mais informações, consulte [descrevendo o local de um objeto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="6a26f-120">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="6a26f-121">*iFlags* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="6a26f-121">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6a26f-122">Determina se as atualizações de status são retornadas.</span><span class="sxs-lookup"><span data-stu-id="6a26f-122">Determines if status updates are returned.</span></span> <span data-ttu-id="6a26f-123">Esse parâmetro pode aceitar os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="6a26f-123">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="6a26f-124"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="6a26f-124"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="6a26f-125">Faz com que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="6a26f-125">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="6a26f-126"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="6a26f-126"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="6a26f-127">Impede que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="6a26f-127">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6a26f-128">*objWbemNamedValueSet* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="6a26f-128">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6a26f-129">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="6a26f-129">Typically, this is undefined.</span></span> <span data-ttu-id="6a26f-130">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="6a26f-130">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="6a26f-131">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="6a26f-131">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="6a26f-132">*objWbemAsyncContext* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="6a26f-132">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6a26f-133">Um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que retorna ao coletor de objeto para identificar a origem da chamada assíncrona original.</span><span class="sxs-lookup"><span data-stu-id="6a26f-133">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="6a26f-134">Use esse parâmetro se você estiver fazendo várias chamadas assíncronas usando o mesmo coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="6a26f-134">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="6a26f-135">Para usar esse parâmetro, crie um objeto **SWbemNamedValueSet** e use o método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo.</span><span class="sxs-lookup"><span data-stu-id="6a26f-135">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="6a26f-136">Esse objeto **SWbemNamedValueSet** é retornado para o coletor de objeto e a origem da chamada pode ser extraída usando o método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="6a26f-136">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="6a26f-137">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="6a26f-137">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a26f-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6a26f-138">Return value</span></span>

<span data-ttu-id="6a26f-139">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6a26f-139">This method does not return a value.</span></span> <span data-ttu-id="6a26f-140">Se a chamada for bem-sucedida, o coletor de objeto receberá a notificação da exclusão.</span><span class="sxs-lookup"><span data-stu-id="6a26f-140">If the call is successful, the object sink receives notification of the deletion.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6a26f-141">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="6a26f-141">Error codes</span></span>

<span data-ttu-id="6a26f-142">Após a conclusão do método **DeleteAsync** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="6a26f-142">After the completion of the **DeleteAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="6a26f-143">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="6a26f-143">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="6a26f-144">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="6a26f-144">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="6a26f-145">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="6a26f-145">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="6a26f-146">Foi especificado um parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="6a26f-146">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="6a26f-147">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="6a26f-147">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="6a26f-148">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="6a26f-148">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6a26f-149">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="6a26f-149">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="6a26f-150">Ocorreu um erro de rede, impedindo a operação normal.</span><span class="sxs-lookup"><span data-stu-id="6a26f-150">Networking error occurred, preventing normal operation.</span></span>

</dd> <dt>

<span data-ttu-id="6a26f-151">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="6a26f-151">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="6a26f-152">O nome de usuário e a senha atuais ou especificados não são válidos ou autorizados a estabelecer a conexão.</span><span class="sxs-lookup"><span data-stu-id="6a26f-152">Current or specified user name and password are not valid or authorized to make the connection.</span></span>

</dd> <dt>

<span data-ttu-id="6a26f-153">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="6a26f-153">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="6a26f-154">O item solicitado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="6a26f-154">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a26f-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a26f-155">Remarks</span></span>

<span data-ttu-id="6a26f-156">Essa chamada retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="6a26f-156">This call returns immediately.</span></span> <span data-ttu-id="6a26f-157">O status da operação de exclusão é retornado para o chamador por meio de um retorno de chamada entregue ao coletor especificado em *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="6a26f-157">The status of the delete operation is returned to the caller through a callback delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="6a26f-158">Você pode executar o processamento final em sua implementação do *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="6a26f-158">You can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="6a26f-159">Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor.</span><span class="sxs-lookup"><span data-stu-id="6a26f-159">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="6a26f-160">Isso representa riscos de segurança para seus scripts e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6a26f-160">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="6a26f-161">Para eliminar os riscos, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="6a26f-161">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a26f-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a26f-162">Requirements</span></span>



| <span data-ttu-id="6a26f-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a26f-163">Requirement</span></span> | <span data-ttu-id="6a26f-164">Valor</span><span class="sxs-lookup"><span data-stu-id="6a26f-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a26f-165">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a26f-165">Minimum supported client</span></span><br/> | <span data-ttu-id="6a26f-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a26f-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6a26f-167">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a26f-167">Minimum supported server</span></span><br/> | <span data-ttu-id="6a26f-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a26f-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6a26f-169">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6a26f-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a26f-170"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a26f-170"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6a26f-171">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6a26f-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="6a26f-172"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6a26f-172"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6a26f-173">DLL</span><span class="sxs-lookup"><span data-stu-id="6a26f-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a26f-174"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a26f-174"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6a26f-175">CLSID</span><span class="sxs-lookup"><span data-stu-id="6a26f-175">CLSID</span></span><br/>                    | <span data-ttu-id="6a26f-176">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="6a26f-176">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="6a26f-177">IID</span><span class="sxs-lookup"><span data-stu-id="6a26f-177">IID</span></span><br/>                      | <span data-ttu-id="6a26f-178">ISWbemServices de IID \_</span><span class="sxs-lookup"><span data-stu-id="6a26f-178">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="6a26f-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a26f-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a26f-180">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="6a26f-180">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="6a26f-181">**SWbemObjectPath**</span><span class="sxs-lookup"><span data-stu-id="6a26f-181">**SWbemObjectPath**</span></span>](swbemobjectpath.md)
</dt> </dl>

 

