---
description: SWbemServices.Exemétodo cQueryAsync – executa uma consulta para recuperar objetos.
ms.assetid: 50c7f62b-dd83-4117-b10e-acee1690ce8c
ms.tgt_platform: multiple
title: SWbemServices.Exemétodo cQueryAsync (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecQueryAsync
- ISWbemServices.ExecQueryAsync
- ISWbemServices.ExecQueryAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5cd3fe778ca7338df6b2674a4930458ef9113a1d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118374"
---
# <a name="swbemservicesexecqueryasync-method"></a><span data-ttu-id="5e0cf-103">SWbemServices.Exemétodo cQueryAsync</span><span class="sxs-lookup"><span data-stu-id="5e0cf-103">SWbemServices.ExecQueryAsync method</span></span>

<span data-ttu-id="5e0cf-104">O método **ExecQueryAsync** do objeto [**SWbemServices**](swbemservices.md) executa uma consulta para recuperar objetos.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-104">The **ExecQueryAsync** method of the [**SWbemServices**](swbemservices.md) object executes a query to retrieve objects.</span></span> <span data-ttu-id="5e0cf-105">A chamada para esse método retorna imediatamente, e os resultados e o status são retornados para o chamador por meio de eventos entregues ao coletor especificado em *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-105">The call to this method returns immediately, and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="5e0cf-106">Para lidar com cada objeto retornado, crie um *objWbemSink*. Sub-rotina de evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="5e0cf-106">To handle each returned object, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span>

<span data-ttu-id="5e0cf-107">O método é chamado no modo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-107">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="5e0cf-108">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="5e0cf-108">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="5e0cf-109">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5e0cf-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5e0cf-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e0cf-110">Syntax</span></span>


```VB
objWbemObjectSet = .ExecQueryAsync( _
  [ ByVal objWbemSink ], _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="5e0cf-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e0cf-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e0cf-112">*objWbemSink* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="5e0cf-112">*objWbemSink* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5e0cf-113">Coletor de objeto que executa a consulta de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-113">Object sink that executes the query asynchronously.</span></span> <span data-ttu-id="5e0cf-114">Crie um objeto [**SWbemSink**](swbemsink.md) para receber os objetos.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-114">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="5e0cf-115">*strQuery*</span><span class="sxs-lookup"><span data-stu-id="5e0cf-115">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="5e0cf-116">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-116">Required.</span></span> <span data-ttu-id="5e0cf-117">Cadeia de caracteres que contém o texto da consulta.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-117">String that contains the text of the query.</span></span> <span data-ttu-id="5e0cf-118">Este parâmetro não pode ficar em branco.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-118">This parameter cannot be blank.</span></span> <span data-ttu-id="5e0cf-119">Para obter mais informações sobre como criar cadeias de caracteres de consulta do WMI, consulte [consultando com WQL](querying-with-wql.md) e a referência [WQL](wql-sql-for-wmi.md) .</span><span class="sxs-lookup"><span data-stu-id="5e0cf-119">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="5e0cf-120">*strQueryLanguage* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="5e0cf-120">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5e0cf-121">Cadeia de caracteres que contém a linguagem de consulta a ser usada.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-121">String that contains the query language to be used.</span></span> <span data-ttu-id="5e0cf-122">Se especificado, o valor deve ser "WQL".</span><span class="sxs-lookup"><span data-stu-id="5e0cf-122">If specified, the value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="5e0cf-123">*iFlags* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="5e0cf-123">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5e0cf-124">Inteiro que determina o comportamento da consulta.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-124">Integer that determines the behavior of the query.</span></span> <span data-ttu-id="5e0cf-125">Esse parâmetro pode aceitar os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-125">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="5e0cf-126"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="5e0cf-126"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="5e0cf-127">Faz com que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-127">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="5e0cf-128"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="5e0cf-128"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="5e0cf-129">Impede que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-129">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>

<span data-ttu-id="5e0cf-130"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>wbemQueryFlagPrototype \* \* \* \* (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="5e0cf-130"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>\*\*\*\*wbemQueryFlagPrototype\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="5e0cf-131">Usado para um protótipo.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-131">Used for a prototype.</span></span> <span data-ttu-id="5e0cf-132">Ele interrompe a consulta de acontecer e, em vez disso, retorna um objeto que se parece com um objeto de resultado típico.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-132">It stops the query from happening and instead, returns an object that looks like a typical result object.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="5e0cf-133"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="5e0cf-133"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="5e0cf-134">Faz com que o WMI retorne dados de alteração de classe com a definição de classe base.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-134">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="5e0cf-135">Para obter mais informações, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="5e0cf-135">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5e0cf-136">*objwbemNamedValueSet* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="5e0cf-136">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5e0cf-137">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-137">Typically, this is undefined.</span></span> <span data-ttu-id="5e0cf-138">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que presta a solicitação.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-138">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="5e0cf-139">Um provedor que dá suporte ou exige informações de contexto deve documentar os nomes de valores reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-139">A provider that supports or requires context information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="5e0cf-140">*objWbemAsyncContext* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="5e0cf-140">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5e0cf-141">Um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que retorna ao coletor de objeto para identificar a origem da chamada assíncrona original.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-141">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="5e0cf-142">Use esse parâmetro para fazer várias chamadas assíncronas usando o mesmo coletor de objeto.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-142">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="5e0cf-143">Para usar esse parâmetro, crie um objeto **SWbemNamedValueSet** e use o método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-143">To use this parameter, create an **SWbemNamedValueSet** object, and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="5e0cf-144">Esse objeto **SWbemNamedValueSet** é retornado para o coletor de objeto e a origem da chamada pode ser extraída usando o método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="5e0cf-144">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="5e0cf-145">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="5e0cf-145">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e0cf-146">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5e0cf-146">Return value</span></span>

<span data-ttu-id="5e0cf-147">Este método não tem valores de retorno.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-147">This method has no return values.</span></span> <span data-ttu-id="5e0cf-148">Se for bem-sucedido, o coletor receberá um evento [**OnObjectReady**](swbemsink-onobjectready.md) por instância.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-148">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="5e0cf-149">Após a última instância, o coletor de objeto recebe um evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="5e0cf-149">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5e0cf-150">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="5e0cf-150">Error codes</span></span>

<span data-ttu-id="5e0cf-151">Após a conclusão do método **ExecQueryAsync** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-151">After the completion of the **ExecQueryAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object can contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="5e0cf-152">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="5e0cf-152">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="5e0cf-153">O usuário atual não tem permissão para exibir o conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-153">Current user does not have the permission to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="5e0cf-154">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="5e0cf-154">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="5e0cf-155">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-155">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="5e0cf-156">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="5e0cf-156">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="5e0cf-157">Foi especificado um parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-157">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="5e0cf-158">**wbemErrInvalidQuery** -2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="5e0cf-158">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="5e0cf-159">Sintaxe de consulta inválida.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-159">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5e0cf-160">**wbemErrInvalidQueryType** -2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="5e0cf-160">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="5e0cf-161">Não há suporte para a linguagem de consulta solicitada.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-161">Requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5e0cf-162">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="5e0cf-162">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="5e0cf-163">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-163">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e0cf-164">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e0cf-164">Remarks</span></span>

<span data-ttu-id="5e0cf-165">Essa chamada retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-165">This call returns immediately.</span></span> <span data-ttu-id="5e0cf-166">Os objetos e status solicitados são retornados ao chamador por meio de retornos de chamada entregues ao coletor especificado em *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-166">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="5e0cf-167">Para processar cada objeto quando ele retornar, crie um *objWbemSink*. Sub-rotina de evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="5e0cf-167">To process each object when it returns, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="5e0cf-168">Depois que todos os objetos forem retornados, execute o processamento final em sua implementação do *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="5e0cf-168">After all the objects are returned, perform the final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="5e0cf-169">Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-169">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="5e0cf-170">Isso representa riscos de segurança para seus scripts e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-170">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="5e0cf-171">Para eliminar os riscos, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md)</span><span class="sxs-lookup"><span data-stu-id="5e0cf-171">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md)</span></span>

<span data-ttu-id="5e0cf-172">O método **ExecQueryAsync** retorna um conjunto de resultados vazio quando não há objetos para corresponder aos critérios na consulta.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-172">The **ExecQueryAsync** method returns an empty result set when there are no objects to match the criteria in the query.</span></span> <span data-ttu-id="5e0cf-173">Esse método retorna propriedades de chave se a propriedade de [**chave**](standard-qualifiers.md) é ou não solicitada no parâmetro *strQuery* .</span><span class="sxs-lookup"><span data-stu-id="5e0cf-173">This method returns key properties whether or not the [**Key**](standard-qualifiers.md) property is requested in the *strQuery* parameter.</span></span>

<span data-ttu-id="5e0cf-174">Há limites para o número de palavras-chave **and** e **or** que podem ser usadas em consultas WQL.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-174">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="5e0cf-175">Grandes números de palavras-chave WQL usadas em uma consulta complexa podem fazer com que o WMI retorne o \_ código de erro de violação E de cota de WBEM \_ \_ como um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5e0cf-175">Large numbers of WQL keywords used in a complex query can cause WMI to return the WBEM\_E\_QUOTA\_VIOLATION error code as an **HRESULT** value.</span></span> <span data-ttu-id="5e0cf-176">O limite de palavras-chave WQL depende da complexidade da consulta.</span><span class="sxs-lookup"><span data-stu-id="5e0cf-176">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e0cf-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e0cf-177">Requirements</span></span>



| <span data-ttu-id="5e0cf-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e0cf-178">Requirement</span></span> | <span data-ttu-id="5e0cf-179">Valor</span><span class="sxs-lookup"><span data-stu-id="5e0cf-179">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e0cf-180">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e0cf-180">Minimum supported client</span></span><br/> | <span data-ttu-id="5e0cf-181">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e0cf-181">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5e0cf-182">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e0cf-182">Minimum supported server</span></span><br/> | <span data-ttu-id="5e0cf-183">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5e0cf-183">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5e0cf-184">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5e0cf-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e0cf-185"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e0cf-185"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e0cf-186">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5e0cf-186">Type library</span></span><br/>             | <dl> <span data-ttu-id="5e0cf-187"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5e0cf-187"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5e0cf-188">DLL</span><span class="sxs-lookup"><span data-stu-id="5e0cf-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e0cf-189"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e0cf-189"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5e0cf-190">CLSID</span><span class="sxs-lookup"><span data-stu-id="5e0cf-190">CLSID</span></span><br/>                    | <span data-ttu-id="5e0cf-191">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="5e0cf-191">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="5e0cf-192">IID</span><span class="sxs-lookup"><span data-stu-id="5e0cf-192">IID</span></span><br/>                      | <span data-ttu-id="5e0cf-193">ISWbemServices de IID \_</span><span class="sxs-lookup"><span data-stu-id="5e0cf-193">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="5e0cf-194">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5e0cf-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e0cf-195">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="5e0cf-195">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="5e0cf-196">Chamando um método</span><span class="sxs-lookup"><span data-stu-id="5e0cf-196">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="5e0cf-197">**SWbemServices. Get**</span><span class="sxs-lookup"><span data-stu-id="5e0cf-197">**SWbemServices.Get**</span></span>](swbemservices-get.md)
</dt> </dl>

 

