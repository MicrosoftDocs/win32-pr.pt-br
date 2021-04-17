---
description: Executa uma consulta para receber eventos.
ms.assetid: 0b0e8313-4ffd-4d4a-8965-d2c6743e7573
ms.tgt_platform: multiple
title: SWbemServices.Exemétodo cNotificationQueryAsync (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecNotificationQueryAsync
- ISWbemServices.ExecNotificationQueryAsync
- ISWbemServices.ExecNotificationQueryAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8e2ecddf290d83583b3108620b8b4bb23be7c957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791579"
---
# <a name="swbemservicesexecnotificationqueryasync-method"></a><span data-ttu-id="c8145-103">SWbemServices.Exemétodo cNotificationQueryAsync</span><span class="sxs-lookup"><span data-stu-id="c8145-103">SWbemServices.ExecNotificationQueryAsync method</span></span>

<span data-ttu-id="c8145-104">O método **ExecNotificationQueryAsync** do objeto [**SWbemServices**](swbemservices.md) executa uma consulta para receber eventos.</span><span class="sxs-lookup"><span data-stu-id="c8145-104">The **ExecNotificationQueryAsync** method of the [**SWbemServices**](swbemservices.md) object executes a query to receive events.</span></span> <span data-ttu-id="c8145-105">Essa chamada retorna imediatamente e os resultados e o status são retornados para o chamador por meio de eventos entregues ao coletor especificado em *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="c8145-105">This call returns immediately and the results and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span>

<span data-ttu-id="c8145-106">Os eventos que são especificados na consulta podem ser eventos intrínsecos Instrumentação de gerenciamento do Windows (WMI), como [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)ou eventos extrínsecos, como [**Win32 \_ IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent) ou [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span><span class="sxs-lookup"><span data-stu-id="c8145-106">The events that are specified in the query can be intrinsic Windows Management Instrumentation (WMI) events, such as [**\_\_InstanceCreationEvent**](--instancecreationevent.md), or extrinsic events, such as [**Win32\_IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent) or [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span></span> <span data-ttu-id="c8145-107">Para obter mais informações, consulte [determinando o tipo de evento a ser recebido](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="c8145-107">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="c8145-108">O método é chamado no modo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="c8145-108">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="c8145-109">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="c8145-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="c8145-110">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c8145-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c8145-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8145-111">Syntax</span></span>


```VB
SWbemServices.ExecNotificationQueryAsync( _
  ByVal objWbemSink, _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c8145-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8145-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8145-113">*objWbemSink*</span><span class="sxs-lookup"><span data-stu-id="c8145-113">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="c8145-114">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="c8145-114">Required.</span></span> <span data-ttu-id="c8145-115">Coletor de objeto que recebe a notificação de eventos de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="c8145-115">Object sink that receives the notification of events asynchronously.</span></span> <span data-ttu-id="c8145-116">Crie um objeto [**SWbemSink**](swbemsink.md) para receber os objetos.</span><span class="sxs-lookup"><span data-stu-id="c8145-116">Create a [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span>

</dd> <dt>

<span data-ttu-id="c8145-117">*strQuery*</span><span class="sxs-lookup"><span data-stu-id="c8145-117">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="c8145-118">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="c8145-118">Required.</span></span> <span data-ttu-id="c8145-119">Cadeia de caracteres que contém o texto da consulta relacionada ao evento.</span><span class="sxs-lookup"><span data-stu-id="c8145-119">String that contains the text of the event-related query.</span></span> <span data-ttu-id="c8145-120">Este parâmetro não pode ficar em branco.</span><span class="sxs-lookup"><span data-stu-id="c8145-120">This parameter cannot be blank.</span></span> <span data-ttu-id="c8145-121">Para obter mais informações sobre como criar cadeias de caracteres de consulta do WMI, consulte [consultando com WQL](querying-with-wql.md) e a referência [WQL](wql-sql-for-wmi.md) .</span><span class="sxs-lookup"><span data-stu-id="c8145-121">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="c8145-122">*strQueryLanguage* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="c8145-122">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c8145-123">Cadeia de caracteres que contém a linguagem de consulta a ser usada.</span><span class="sxs-lookup"><span data-stu-id="c8145-123">String that contains the query language to be used.</span></span> <span data-ttu-id="c8145-124">Se especificado, esse valor deve ser "WQL".</span><span class="sxs-lookup"><span data-stu-id="c8145-124">If specified, this value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="c8145-125">*iFlags* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="c8145-125">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c8145-126">Inteiro que determina o comportamento da consulta.</span><span class="sxs-lookup"><span data-stu-id="c8145-126">Integer that determines the behavior of the query.</span></span> <span data-ttu-id="c8145-127">Esse parâmetro pode ser definido com os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c8145-127">This parameter can be set to the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="c8145-128"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="c8145-128"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="c8145-129">Faz com que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="c8145-129">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="c8145-130"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="c8145-130"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="c8145-131">Impede que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="c8145-131">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c8145-132">*objwbemNamedValueSet* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="c8145-132">*objwbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c8145-133">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="c8145-133">Typically, this is undefined.</span></span> <span data-ttu-id="c8145-134">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que presta a solicitação.</span><span class="sxs-lookup"><span data-stu-id="c8145-134">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="c8145-135">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="c8145-135">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="c8145-136">*objWbemAsyncContext* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="c8145-136">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c8145-137">Esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que retorna ao coletor de objeto para identificar a origem da chamada assíncrona original.</span><span class="sxs-lookup"><span data-stu-id="c8145-137">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="c8145-138">Use esse parâmetro para fazer várias chamadas assíncronas usando o mesmo coletor de objeto.</span><span class="sxs-lookup"><span data-stu-id="c8145-138">Use this parameter to make multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="c8145-139">Para usar esse parâmetro, crie um objeto **SWbemNamedValueSet** e use o método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo.</span><span class="sxs-lookup"><span data-stu-id="c8145-139">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="c8145-140">O objeto **SWbemNamedValueSet** é retornado para o coletor de objeto e a origem da chamada pode ser extraída usando o método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="c8145-140">The **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="c8145-141">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="c8145-141">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8145-142">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c8145-142">Return value</span></span>

<span data-ttu-id="c8145-143">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c8145-143">This method does not return a value.</span></span> <span data-ttu-id="c8145-144">Se for bem-sucedido, o coletor receberá um evento [**OnObjectReady**](swbemsink-onobjectready.md) por instância.</span><span class="sxs-lookup"><span data-stu-id="c8145-144">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="c8145-145">Após a última instância, o coletor de objeto recebe um evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="c8145-145">After the last instance, the object sink receives an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c8145-146">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="c8145-146">Error codes</span></span>

<span data-ttu-id="c8145-147">Após a conclusão do método **ExecNotificationQueryAsync** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro identificados na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="c8145-147">After the completion of the **ExecNotificationQueryAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes identified in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="c8145-148">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="c8145-148">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="c8145-149">O usuário atual não está autorizado a exibir o conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="c8145-149">Current user is not authorized to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="c8145-150">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="c8145-150">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="c8145-151">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="c8145-151">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="c8145-152">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="c8145-152">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="c8145-153">Parâmetro inválido especificado.</span><span class="sxs-lookup"><span data-stu-id="c8145-153">Invalid parameter is specified.</span></span>

</dd> <dt>

<span data-ttu-id="c8145-154">**wbemErrInvalidQuery** -2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="c8145-154">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="c8145-155">Sintaxe de consulta inválida.</span><span class="sxs-lookup"><span data-stu-id="c8145-155">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c8145-156">**wbemErrInvalidQueryType** -2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="c8145-156">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="c8145-157">Não há suporte para a linguagem de consulta solicitada.</span><span class="sxs-lookup"><span data-stu-id="c8145-157">Requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c8145-158">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="c8145-158">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="c8145-159">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="c8145-159">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c8145-160">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8145-160">Remarks</span></span>

<span data-ttu-id="c8145-161">O método **ExecNotificationQueryAsync** retorna objetos de tipo de evento que geram eventos futuros.</span><span class="sxs-lookup"><span data-stu-id="c8145-161">The **ExecNotificationQueryAsync** method returns event type objects that future events generate.</span></span> <span data-ttu-id="c8145-162">Os objetos de evento que **ExecNotificationQueryAsync** solicitações podem ser intrínsecos (por exemplo, [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)) ou extrínsecos (por exemplo, eventos de [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) ou SNMP).</span><span class="sxs-lookup"><span data-stu-id="c8145-162">The event objects that **ExecNotificationQueryAsync** requests can be intrinsic (for example, [**\_\_InstanceCreationEvent**](--instancecreationevent.md)), or extrinsic (for example, [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) or SNMP events).</span></span> <span data-ttu-id="c8145-163">Para obter mais informações, consulte [determinando o tipo de evento a ser recebido](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="c8145-163">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="c8145-164">A chamada para **ExecNotificationQueryAsync** retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="c8145-164">The call to **ExecNotificationQueryAsync** returns immediately.</span></span> <span data-ttu-id="c8145-165">Os objetos e status solicitados são retornados ao chamador por meio de retornos de chamada entregues ao coletor especificado em *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="c8145-165">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="c8145-166">Para processar cada objeto quando ele for retornado, crie um *objWbemSink*. Sub-rotina de evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="c8145-166">To process each object when it is returned, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="c8145-167">Depois que todos os objetos forem retornados, execute o processamento final para implementar o *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="c8145-167">After all the objects are returned, perform the final processing to implement the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="c8145-168">Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor.</span><span class="sxs-lookup"><span data-stu-id="c8145-168">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="c8145-169">Isso representa riscos de segurança para seus scripts e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="c8145-169">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="c8145-170">Para eliminar os riscos, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="c8145-170">To eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="c8145-171">Há limites para o número de palavras-chave **and** e **or** que podem ser usadas em consultas WQL.</span><span class="sxs-lookup"><span data-stu-id="c8145-171">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="c8145-172">Grandes números de palavras-chave WQL usadas em uma consulta complexa podem fazer com que o WMI retorne o código de erro de **\_ \_ \_ violação E de cota** de Asan valor de **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c8145-172">Large numbers of WQL keywords used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code asan **HRESULT** value.</span></span> <span data-ttu-id="c8145-173">O limite de palavras-chave WQL depende da complexidade da consulta.</span><span class="sxs-lookup"><span data-stu-id="c8145-173">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="examples"></a><span data-ttu-id="c8145-174">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c8145-174">Examples</span></span>

<span data-ttu-id="c8145-175">O exemplo de código VBScript a seguir mostra um script que está aguardando uma notificação de evento WMI que indica que um processo foi encerrado.</span><span class="sxs-lookup"><span data-stu-id="c8145-175">The following VBScript code example shows a script that is waiting for a WMI event notification that indicates that a process has terminated.</span></span> <span data-ttu-id="c8145-176">Ele está aguardando um evento intrínseco do WMI, uma instância da classe de evento [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md).</span><span class="sxs-lookup"><span data-stu-id="c8145-176">It is waiting for a WMI intrinsic event, an instance of the event class [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md).</span></span> <span data-ttu-id="c8145-177">O **\_ \_ InstanceDeletionEvent** deve representar a exclusão de uma instância do [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="c8145-177">The **\_\_InstanceDeletionEvent** must represent the deletion of an instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span> <span data-ttu-id="c8145-178">Para obter mais informações sobre eventos intrínsecos do WMI, consulte [determinando o tipo de evento a ser recebido](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="c8145-178">For more information about WMI intrinsic events, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="c8145-179">O script a seguir é executado indefinidamente até que o computador seja reinicializado, o WMI é interrompido ou o script é interrompido.</span><span class="sxs-lookup"><span data-stu-id="c8145-179">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="c8145-180">Para interromper o script manualmente, use o Gerenciador de tarefas para interromper o processo.</span><span class="sxs-lookup"><span data-stu-id="c8145-180">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="c8145-181">Para interrompê-lo programaticamente, use o método [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) na classe de processo do Win32 \_ .</span><span class="sxs-lookup"><span data-stu-id="c8145-181">To stop it programmatically, use the [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) method in the Win32\_Process class.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & _strComputer & "\root\CIMV2") 
Set MySink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync MySink, "SELECT * FROM __InstanceCreationEvent WITHIN 1 " _
                                               & "WHERE TargetInstance ISA 'Win32_Process'"

WScript.Echo "Waiting for events..."

While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    WScript.Echo "Event occurred."
End Sub

Sub SINK_OnCompleted(objObject, objAsyncContext)
    WScript.Echo "Event call complete."
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c8145-182">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8145-182">Requirements</span></span>



| <span data-ttu-id="c8145-183">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8145-183">Requirement</span></span> | <span data-ttu-id="c8145-184">Valor</span><span class="sxs-lookup"><span data-stu-id="c8145-184">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8145-185">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8145-185">Minimum supported client</span></span><br/> | <span data-ttu-id="c8145-186">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8145-186">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c8145-187">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8145-187">Minimum supported server</span></span><br/> | <span data-ttu-id="c8145-188">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8145-188">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c8145-189">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c8145-189">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8145-190"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8145-190"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c8145-191">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c8145-191">Type library</span></span><br/>             | <dl> <span data-ttu-id="c8145-192"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c8145-192"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c8145-193">DLL</span><span class="sxs-lookup"><span data-stu-id="c8145-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8145-194"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8145-194"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c8145-195">CLSID</span><span class="sxs-lookup"><span data-stu-id="c8145-195">CLSID</span></span><br/>                    | <span data-ttu-id="c8145-196">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="c8145-196">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="c8145-197">IID</span><span class="sxs-lookup"><span data-stu-id="c8145-197">IID</span></span><br/>                      | <span data-ttu-id="c8145-198">ISWbemServices de IID \_</span><span class="sxs-lookup"><span data-stu-id="c8145-198">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="c8145-199">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8145-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8145-200">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="c8145-200">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="c8145-201">**SWbemServices.ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="c8145-201">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)
</dt> <dt>

[<span data-ttu-id="c8145-202">**SWbemServices.ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="c8145-202">**SWbemServices.ExecQueryAsync**</span></span>](swbemservices-execqueryasync.md)
</dt> <dt>

[<span data-ttu-id="c8145-203">Registrando para eventos de registro do sistema</span><span class="sxs-lookup"><span data-stu-id="c8145-203">Registering for System Registry Events</span></span>](registering-for-system-registry-events.md)
</dt> <dt>

[<span data-ttu-id="c8145-204">Determinando o tipo de evento a ser recebido</span><span class="sxs-lookup"><span data-stu-id="c8145-204">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[<span data-ttu-id="c8145-205">Chamando um método</span><span class="sxs-lookup"><span data-stu-id="c8145-205">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="c8145-206">Definindo a segurança em uma chamada assíncrona</span><span class="sxs-lookup"><span data-stu-id="c8145-206">Setting Security on an Asynchronous Call</span></span>](setting-security-on-an-asynchronous-call.md)
</dt> </dl>

 

