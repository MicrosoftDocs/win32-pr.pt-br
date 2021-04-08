---
description: Retorna uma coleção de subclasses para uma classe especificada.
ms.assetid: a9d16ee9-992e-4ce5-9c03-0a2c9958588c
ms.tgt_platform: multiple
title: Método SWbemServices. SubclassesOfAsync (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.SubclassesOfAsync
- ISWbemServices.SubclassesOfAsync
- ISWbemServices.SubclassesOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d8d325c96ea1a292d8ac3afc76bfea619fe5a143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922078"
---
# <a name="swbemservicessubclassesofasync-method"></a><span data-ttu-id="3cdfd-103">Método SWbemServices. SubclassesOfAsync</span><span class="sxs-lookup"><span data-stu-id="3cdfd-103">SWbemServices.SubclassesOfAsync method</span></span>

<span data-ttu-id="3cdfd-104">O método **SubclassesOfAsync** do objeto [**SWbemServices**](swbemservices.md) retorna uma coleção de subclasses para uma classe especificada.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-104">The **SubclassesOfAsync** method of the [**SWbemServices**](swbemservices.md) object returns a collection of subclasses for a specified class.</span></span> <span data-ttu-id="3cdfd-105">Use este método somente para objetos de classe.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-105">Only use this method for class objects.</span></span>

<span data-ttu-id="3cdfd-106">Esse método é chamado no modo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-106">This method is called in the asynchronous mode.</span></span> <span data-ttu-id="3cdfd-107">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="3cdfd-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="3cdfd-108">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="3cdfd-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3cdfd-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3cdfd-109">Syntax</span></span>


```VB
SWbemServices.SubclassesOfAsync( _
  ByVal ObjWbemSink, _
  [ ByVal strSuperclass ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="3cdfd-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3cdfd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cdfd-111">*ObjWbemSink*</span><span class="sxs-lookup"><span data-stu-id="3cdfd-111">*ObjWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="3cdfd-112">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-112">Required.</span></span> <span data-ttu-id="3cdfd-113">Coletor de objeto que recebe as subclasses de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-113">Object sink that receives the subclasses asynchronously.</span></span> <span data-ttu-id="3cdfd-114">Crie um objeto [**SWbemSink**](swbemsink.md) para receber os objetos.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-114">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="3cdfd-115">*strSuperclass* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="3cdfd-115">*strSuperclass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3cdfd-116">Especifica um nome de classe pai.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-116">Specifies a parent class name.</span></span> <span data-ttu-id="3cdfd-117">Somente as classes que são subclasses dessa classe são retornadas no enumerador.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-117">Only the classes that are subclasses of this class are returned in the enumerator.</span></span> <span data-ttu-id="3cdfd-118">Se esse parâmetro estiver em branco e se *iFlags* for **wbemQueryFlagShallow**, somente as classes de nível superior serão retornadas (ou seja, classes que não têm nenhuma classe pai).</span><span class="sxs-lookup"><span data-stu-id="3cdfd-118">If this parameter is blank, and if *iFlags* is **wbemQueryFlagShallow**, only the top-level classes are returned (that is, classes that have no parent class).</span></span> <span data-ttu-id="3cdfd-119">Se esse parâmetro estiver em branco e se *iFlags* for **wbemQueryFlagDeep**, todas as classes dentro do namespace serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-119">If this parameter is blank, and if *iFlags* is **wbemQueryFlagDeep**, all classes within the namespace are returned.</span></span>

</dd> <dt>

<span data-ttu-id="3cdfd-120">*iFlags* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="3cdfd-120">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3cdfd-121">Determina a profundidade da enumeração de chamada.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-121">Determines the depth of the call enumeration.</span></span> <span data-ttu-id="3cdfd-122">O valor padrão para esse parâmetro é **wbemQueryFlagDeep**.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-122">The default value for this parameter is **wbemQueryFlagDeep**.</span></span> <span data-ttu-id="3cdfd-123">Esse parâmetro pode aceitar os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-123">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="3cdfd-124"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="3cdfd-124"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="3cdfd-125">Força a enumeração a incluir apenas subclasses imediatas da classe pai especificada.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-125">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="3cdfd-126"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="3cdfd-126"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="3cdfd-127">Padrão para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-127">Default for this parameter.</span></span> <span data-ttu-id="3cdfd-128">Esse valor força a enumeração recursiva em todas as subclasses derivadas da classe pai especificada.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-128">This value forces recursive enumeration into all subclasses that are derived from the specified parent class.</span></span> <span data-ttu-id="3cdfd-129">A classe pai não é retornada na enumeração.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-129">The parent class is not returned in the enumeration.</span></span>

</dd> <dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="3cdfd-130"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="3cdfd-130"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="3cdfd-131">Faz com que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-131">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="3cdfd-132"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="3cdfd-132"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="3cdfd-133">Impede que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-133">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="3cdfd-134"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="3cdfd-134"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="3cdfd-135">Faz com que o WMI retorne dados de alteração de classe com a definição de classe base.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-135">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="3cdfd-136">Para obter mais informações, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="3cdfd-136">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3cdfd-137">*objwbemNamedValueSet* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="3cdfd-137">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3cdfd-138">Normalmente, esse parâmetro é indefinido.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-138">Typically, this parameter is undefined.</span></span> <span data-ttu-id="3cdfd-139">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-139">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="3cdfd-140">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-140">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="3cdfd-141">*objWbemAsyncContext* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="3cdfd-141">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3cdfd-142">Um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que retorna ao coletor de objeto para identificar a origem da chamada assíncrona original.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-142">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="3cdfd-143">Use esse parâmetro para fazer várias chamadas assíncronas usando o mesmo coletor de objeto.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-143">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="3cdfd-144">Para usar esse parâmetro, crie um objeto **SWbemNamedValueSet** e use o método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-144">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="3cdfd-145">Esse objeto **SWbemNamedValueSet** é retornado para o coletor de objeto e a origem da chamada pode ser extraída usando o método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="3cdfd-145">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="3cdfd-146">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="3cdfd-146">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cdfd-147">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3cdfd-147">Return value</span></span>

<span data-ttu-id="3cdfd-148">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-148">This method does not return a value.</span></span> <span data-ttu-id="3cdfd-149">Se for bem-sucedido, o coletor receberá um evento [**OnObjectReady**](swbemsink-onobjectready.md) por instância.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-149">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="3cdfd-150">Após a última instância, o coletor de objeto recebe um evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="3cdfd-150">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3cdfd-151">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="3cdfd-151">Error codes</span></span>

<span data-ttu-id="3cdfd-152">Após a conclusão do método **SubclassesOfAsync** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-152">After the completion of the **SubclassesOfAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="3cdfd-153">Uma coleção retornada com zero elementos não é um erro.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-153">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="3cdfd-154">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="3cdfd-154">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="3cdfd-155">O usuário atual não tem permissão para exibir uma ou mais das classes retornadas pela chamada.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-155">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="3cdfd-156">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="3cdfd-156">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="3cdfd-157">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-157">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="3cdfd-158">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="3cdfd-158">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="3cdfd-159">A classe especificada não existe.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-159">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="3cdfd-160">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="3cdfd-160">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="3cdfd-161">Foi especificado um parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-161">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="3cdfd-162">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="3cdfd-162">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="3cdfd-163">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-163">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3cdfd-164">Comentários</span><span class="sxs-lookup"><span data-stu-id="3cdfd-164">Remarks</span></span>

<span data-ttu-id="3cdfd-165">Essa chamada retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-165">This call returns immediately.</span></span> <span data-ttu-id="3cdfd-166">Os objetos e status solicitados são retornados ao chamador por meio de retornos de chamada entregues ao coletor especificado em *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-166">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="3cdfd-167">Para processar cada objeto quando ele chegar, crie um *objWbemSink*. Sub-rotina de evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="3cdfd-167">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="3cdfd-168">Depois que todos os objetos forem retornados, você poderá executar o processamento final em sua implementação do *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="3cdfd-168">After all the objects are returned, you can perform the final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="3cdfd-169">Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-169">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="3cdfd-170">Isso representa riscos de segurança para seus scripts e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-170">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="3cdfd-171">Para eliminar os riscos, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="3cdfd-171">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3cdfd-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3cdfd-172">Requirements</span></span>



| <span data-ttu-id="3cdfd-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cdfd-173">Requirement</span></span> | <span data-ttu-id="3cdfd-174">Valor</span><span class="sxs-lookup"><span data-stu-id="3cdfd-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3cdfd-175">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3cdfd-175">Minimum supported client</span></span><br/> | <span data-ttu-id="3cdfd-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3cdfd-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3cdfd-177">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3cdfd-177">Minimum supported server</span></span><br/> | <span data-ttu-id="3cdfd-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3cdfd-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3cdfd-179">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3cdfd-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cdfd-180"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cdfd-180"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3cdfd-181">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3cdfd-181">Type library</span></span><br/>             | <dl> <span data-ttu-id="3cdfd-182"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3cdfd-182"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3cdfd-183">DLL</span><span class="sxs-lookup"><span data-stu-id="3cdfd-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cdfd-184"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cdfd-184"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3cdfd-185">CLSID</span><span class="sxs-lookup"><span data-stu-id="3cdfd-185">CLSID</span></span><br/>                    | <span data-ttu-id="3cdfd-186">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="3cdfd-186">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="3cdfd-187">IID</span><span class="sxs-lookup"><span data-stu-id="3cdfd-187">IID</span></span><br/>                      | <span data-ttu-id="3cdfd-188">ISWbemServices de IID \_</span><span class="sxs-lookup"><span data-stu-id="3cdfd-188">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="3cdfd-189">Confira também</span><span class="sxs-lookup"><span data-stu-id="3cdfd-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cdfd-190">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="3cdfd-190">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="3cdfd-191">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="3cdfd-191">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

