---
description: Executa uma consulta para receber eventos. A chamada retorna imediatamente.
ms.assetid: 3e1bb428-5395-4e90-9713-6d96242fef4e
ms.tgt_platform: multiple
title: SWbemServices.Exemétodo cNotificationQuery (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecNotificationQuery
- ISWbemServices.ExecNotificationQuery
- ISWbemServices.ExecNotificationQuery
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 44279d16e180d776dc4433c6d5246eab2419fca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807945"
---
# <a name="swbemservicesexecnotificationquery-method"></a><span data-ttu-id="720bc-104">SWbemServices.Exemétodo cNotificationQuery</span><span class="sxs-lookup"><span data-stu-id="720bc-104">SWbemServices.ExecNotificationQuery method</span></span>

<span data-ttu-id="720bc-105">O método **ExecNotificationQuery** do objeto [**SWbemServices**](swbemservices.md) executa uma consulta para receber eventos.</span><span class="sxs-lookup"><span data-stu-id="720bc-105">The **ExecNotificationQuery** method of the [**SWbemServices**](swbemservices.md) object executes a query to receive events.</span></span> <span data-ttu-id="720bc-106">A chamada retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="720bc-106">The call returns immediately.</span></span> <span data-ttu-id="720bc-107">O usuário pode sondar o enumerador retornado em busca de eventos à medida que eles chegam.</span><span class="sxs-lookup"><span data-stu-id="720bc-107">The user can poll the returned enumerator for events as they arrive.</span></span>

<span data-ttu-id="720bc-108">O método é chamado no modo semisynchronous.</span><span class="sxs-lookup"><span data-stu-id="720bc-108">The method is called in the semisynchronous mode.</span></span> <span data-ttu-id="720bc-109">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="720bc-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="720bc-110">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="720bc-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="720bc-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="720bc-111">Syntax</span></span>


```VB
objwbemEventsource = .ExecNotificationQuery( _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="720bc-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="720bc-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="720bc-113">*strQuery*</span><span class="sxs-lookup"><span data-stu-id="720bc-113">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="720bc-114">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="720bc-114">Required.</span></span> <span data-ttu-id="720bc-115">Cadeia de caracteres que contém o texto da consulta relacionada ao evento.</span><span class="sxs-lookup"><span data-stu-id="720bc-115">String that contains the text of the event-related query.</span></span> <span data-ttu-id="720bc-116">Este parâmetro não pode ficar em branco.</span><span class="sxs-lookup"><span data-stu-id="720bc-116">This parameter cannot be blank.</span></span> <span data-ttu-id="720bc-117">Para obter mais informações sobre como criar cadeias de caracteres de consulta do WMI, consulte [consultando com WQL](querying-with-wql.md) e a referência [WQL](wql-sql-for-wmi.md) .</span><span class="sxs-lookup"><span data-stu-id="720bc-117">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="720bc-118">*strQueryLanguage* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="720bc-118">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="720bc-119">Cadeia de caracteres que contém a linguagem de consulta a ser usada.</span><span class="sxs-lookup"><span data-stu-id="720bc-119">String that contains the query language to be used.</span></span> <span data-ttu-id="720bc-120">Se especificado, esse valor deve ser "WQL".</span><span class="sxs-lookup"><span data-stu-id="720bc-120">If specified, this value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="720bc-121">*iFlags* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="720bc-121">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="720bc-122">Este é um inteiro que determina o comportamento da consulta.</span><span class="sxs-lookup"><span data-stu-id="720bc-122">This is an integer that determines the behavior of the query.</span></span> <span data-ttu-id="720bc-123">O valor padrão é **wbemFlagReturnImmediately**  +  **wbemFlagForwardOnly**.</span><span class="sxs-lookup"><span data-stu-id="720bc-123">The default value is **wbemFlagReturnImmediately** + **wbemFlagForwardOnly**.</span></span> <span data-ttu-id="720bc-124">Se você especificar esse parâmetro, esse parâmetro deverá ser definido como **wbemFlagReturnImmediately** e **wbemFlagForwardOnly** ou a chamada falhará.</span><span class="sxs-lookup"><span data-stu-id="720bc-124">If you specify this parameter, this parameter must be set to both **wbemFlagReturnImmediately** and **wbemFlagForwardOnly** or the call fails.</span></span> <span data-ttu-id="720bc-125">Esse parâmetro pode aceitar os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="720bc-125">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="720bc-126"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="720bc-126"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="720bc-127">Faz com que um enumerador somente de encaminhamento seja retornado.</span><span class="sxs-lookup"><span data-stu-id="720bc-127">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="720bc-128">Enumeradores de somente encaminhamento são geralmente muito mais rápidos e usam menos memória do que enumeradores convencionais, mas não permitem chamadas para [**SWbemObject. \_ clone**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="720bc-128">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="720bc-129"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="720bc-129"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="720bc-130">Faz com que a chamada retorne imediatamente.</span><span class="sxs-lookup"><span data-stu-id="720bc-130">Causes the call to return immediately.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="720bc-131">*objWbemNamedValueSet* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="720bc-131">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="720bc-132">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="720bc-132">Typically, this is undefined.</span></span> <span data-ttu-id="720bc-133">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="720bc-133">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="720bc-134">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="720bc-134">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="720bc-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="720bc-135">Return value</span></span>

<span data-ttu-id="720bc-136">Se nenhum erro ocorrer, esse método retornará um objeto [**SWbemEventSource**](swbemeventsource.md) .</span><span class="sxs-lookup"><span data-stu-id="720bc-136">If no error occurs, this method returns an [**SWbemEventSource**](swbemeventsource.md) object.</span></span> <span data-ttu-id="720bc-137">Você pode chamar o método [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md) para recuperar eventos à medida que eles chegam.</span><span class="sxs-lookup"><span data-stu-id="720bc-137">You can call the [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md) method to retrieve events as they arrive.</span></span>

## <a name="error-codes"></a><span data-ttu-id="720bc-138">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="720bc-138">Error codes</span></span>

<span data-ttu-id="720bc-139">Após a conclusão do método **ExecNotificationQuery** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="720bc-139">After the completion of the **ExecNotificationQuery** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="720bc-140">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="720bc-140">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="720bc-141">O usuário atual não está autorizado a exibir o conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="720bc-141">Current user is not authorized to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="720bc-142">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="720bc-142">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="720bc-143">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="720bc-143">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="720bc-144">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="720bc-144">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="720bc-145">Foi especificado um parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="720bc-145">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="720bc-146">**wbemErrInvalidQuery** -2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="720bc-146">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="720bc-147">Sintaxe de consulta inválida.</span><span class="sxs-lookup"><span data-stu-id="720bc-147">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="720bc-148">**wbemErrInvalidQueryType** -2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="720bc-148">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="720bc-149">O idioma de consulta solicitado não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="720bc-149">The requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="720bc-150">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="720bc-150">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="720bc-151">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="720bc-151">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="720bc-152">Comentários</span><span class="sxs-lookup"><span data-stu-id="720bc-152">Remarks</span></span>

<span data-ttu-id="720bc-153">Ao contrário do método [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md) , **ExecNotificationQuery** retorna objetos de tipo de evento que são gerados por eventos futuros em vez de objetos existentes.</span><span class="sxs-lookup"><span data-stu-id="720bc-153">Unlike the [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md) method, **ExecNotificationQuery** returns event type objects that are generated by future events rather than existing objects.</span></span> <span data-ttu-id="720bc-154">Os objetos de evento que **ExecNotificationQuery** solicitações podem ser intrínsecos (como [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)) ou extrínsecos (como eventos de provedor do registro, como [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) ou eventos SNMP).</span><span class="sxs-lookup"><span data-stu-id="720bc-154">The event objects that **ExecNotificationQuery** requests can either be intrinsic (such as [**\_\_InstanceCreationEvent**](--instancecreationevent.md)) or extrinsic (such as registry provider events like [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) or SNMP events).</span></span> <span data-ttu-id="720bc-155">Para obter mais informações, consulte [determinando o tipo de evento para receber](determining-the-type-of-event-to-receive.md) e [receber notificações de eventos](receiving-event-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="720bc-155">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md) and [Receiving Event Notifications](receiving-event-notifications.md).</span></span>

<span data-ttu-id="720bc-156">Há limites para o número de palavras-chave **and** e **or** que podem ser usadas em consultas WQL.</span><span class="sxs-lookup"><span data-stu-id="720bc-156">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="720bc-157">Grandes números de palavras-chave WQL usadas em uma consulta complexa podem fazer com que o WMI retorne o código de erro de **\_ \_ \_ violação E de cota de WBEM** como um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="720bc-157">Large numbers of WQL keywords used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code as an **HRESULT** value.</span></span> <span data-ttu-id="720bc-158">O limite de palavras-chave WQL depende da complexidade da consulta.</span><span class="sxs-lookup"><span data-stu-id="720bc-158">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="examples"></a><span data-ttu-id="720bc-159">Exemplos</span><span class="sxs-lookup"><span data-stu-id="720bc-159">Examples</span></span>

<span data-ttu-id="720bc-160">O exemplo de código VBScript a seguir monitora as alterações em volumes em um computador local.</span><span class="sxs-lookup"><span data-stu-id="720bc-160">The following VBScript code example monitors changes to volumes on a local computer.</span></span> <span data-ttu-id="720bc-161">Observe que o [**Win32 \_ VolumeChangeEvent**](/windows/desktop/CIMWin32Prov/win32-volumechangeevent) é um evento extrínsecos que é definido por um provedor não é um evento INTRÍNSECO definido pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="720bc-161">Note that [**Win32\_VolumeChangeEvent**](/windows/desktop/CIMWin32Prov/win32-volumechangeevent) is an extrinsic event that is defined by a provider not an intrinsic WMI-defined event.</span></span> <span data-ttu-id="720bc-162">Para obter mais informações, consulte [determinando o tipo de evento a ser recebido](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="720bc-162">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>


```VB
Set colMonitoredEvents = _
   GetObject("Winmgmts:").ExecNotificationQuery_
      ("Select * from Win32_VolumeChangeEvent")

Do While i = 0
   Set strLatestEvent = colMonitoredEvents.NextEvent
   Wscript.Echo strLatestEvent.DriveName & "Time Created = " _
      & strLatestEvent.Time_Created

    Select Case strLatestEvent.EventType 
       Case 1        
            WScript.Echo "EventType = Configuration Changed"
       Case 2
            WScript.Echo "EventType = Device Arrival"
       Case 3
            WScript.Echo "EventType = Device Removal"
       Case 4
            WScript.Echo "EventType = Docking"

       Case Else
            WScript.Echo "Unrecognized EventType"
       End Select
Loop
```



<span data-ttu-id="720bc-163">O exemplo de código VBScript a seguir monitora a exclusão do processo.</span><span class="sxs-lookup"><span data-stu-id="720bc-163">The following VBScript code example monitors process deletion.</span></span> <span data-ttu-id="720bc-164">Se você excluir um processo no Gerenciador de tarefas ou fechar um aplicativo, o script exibirá uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="720bc-164">If you delete a process in Task Manager or close an application, then the script displays a message.</span></span> <span data-ttu-id="720bc-165">Observe que esse script consulta um evento intrínseco que é definido por WMI- [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md).</span><span class="sxs-lookup"><span data-stu-id="720bc-165">Note that this script queries an intrinsic event that is defined by WMI - [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md).</span></span>


```VB
Set objWMIService = GetObject( _
    "Winmgmts:{impersonationLevel=impersonate}" )
Set colMonitoredProcesses = _
    objWMIService.ExecNotificationQuery( _
    "SELECT * FROM __InstanceDeletionEvent WITHIN 10 WHERE " _
    & "TargetInstance ISA 'Win32_Process'")
i = 0
Do While i < 11
    Set strLatestProcess = colMonitoredProcesses.NextEvent
    WScript.Echo strLatestProcess.TargetInstance.Name
    WScript.Sleep 10000
    i= i + 1
Loop
```



## <a name="requirements"></a><span data-ttu-id="720bc-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="720bc-166">Requirements</span></span>



| <span data-ttu-id="720bc-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="720bc-167">Requirement</span></span> | <span data-ttu-id="720bc-168">Valor</span><span class="sxs-lookup"><span data-stu-id="720bc-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="720bc-169">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="720bc-169">Minimum supported client</span></span><br/> | <span data-ttu-id="720bc-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="720bc-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="720bc-171">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="720bc-171">Minimum supported server</span></span><br/> | <span data-ttu-id="720bc-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="720bc-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="720bc-173">parâmetro</span><span class="sxs-lookup"><span data-stu-id="720bc-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="720bc-174"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="720bc-174"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="720bc-175">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="720bc-175">Type library</span></span><br/>             | <dl> <span data-ttu-id="720bc-176"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="720bc-176"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="720bc-177">DLL</span><span class="sxs-lookup"><span data-stu-id="720bc-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="720bc-178"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="720bc-178"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="720bc-179">CLSID</span><span class="sxs-lookup"><span data-stu-id="720bc-179">CLSID</span></span><br/>                    | <span data-ttu-id="720bc-180">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="720bc-180">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="720bc-181">IID</span><span class="sxs-lookup"><span data-stu-id="720bc-181">IID</span></span><br/>                      | <span data-ttu-id="720bc-182">ISWbemServices de IID \_</span><span class="sxs-lookup"><span data-stu-id="720bc-182">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="720bc-183">Confira também</span><span class="sxs-lookup"><span data-stu-id="720bc-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="720bc-184">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="720bc-184">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="720bc-185">**SWbemEventSource.NextEvent**</span><span class="sxs-lookup"><span data-stu-id="720bc-185">**SWbemEventSource.NextEvent**</span></span>](swbemeventsource-nextevent.md)
</dt> <dt>

[<span data-ttu-id="720bc-186">**SWbemServices.ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="720bc-186">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)
</dt> <dt>

[<span data-ttu-id="720bc-187">Recebendo um evento WMI</span><span class="sxs-lookup"><span data-stu-id="720bc-187">Receiving a WMI Event</span></span>](receiving-a-wmi-event.md)
</dt> <dt>

[<span data-ttu-id="720bc-188">Consultando com WQL</span><span class="sxs-lookup"><span data-stu-id="720bc-188">Querying with WQL</span></span>](querying-with-wql.md)
</dt> <dt>

[<span data-ttu-id="720bc-189">WQL (SQL para WMI)</span><span class="sxs-lookup"><span data-stu-id="720bc-189">WQL (SQL for WMI)</span></span>](wql-sql-for-wmi.md)
</dt> <dt>

[<span data-ttu-id="720bc-190">Determinando o tipo de evento a ser recebido</span><span class="sxs-lookup"><span data-stu-id="720bc-190">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

