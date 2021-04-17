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
# <a name="swbemservicesexecnotificationqueryasync-method"></a>SWbemServices.Exemétodo cNotificationQueryAsync

O método **ExecNotificationQueryAsync** do objeto [**SWbemServices**](swbemservices.md) executa uma consulta para receber eventos. Essa chamada retorna imediatamente e os resultados e o status são retornados para o chamador por meio de eventos entregues ao coletor especificado em *objWbemSink*.

Os eventos que são especificados na consulta podem ser eventos intrínsecos Instrumentação de gerenciamento do Windows (WMI), como [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)ou eventos extrínsecos, como [**Win32 \_ IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent) ou [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent). Para obter mais informações, consulte [determinando o tipo de evento a ser recebido](determining-the-type-of-event-to-receive.md).

O método é chamado no modo assíncrono. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


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



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*objWbemSink* 
</dt> <dd>

Obrigatórios. Coletor de objeto que recebe a notificação de eventos de forma assíncrona. Crie um objeto [**SWbemSink**](swbemsink.md) para receber os objetos.

</dd> <dt>

*strQuery* 
</dt> <dd>

Obrigatórios. Cadeia de caracteres que contém o texto da consulta relacionada ao evento. Este parâmetro não pode ficar em branco. Para obter mais informações sobre como criar cadeias de caracteres de consulta do WMI, consulte [consultando com WQL](querying-with-wql.md) e a referência [WQL](wql-sql-for-wmi.md) .

</dd> <dt>

*strQueryLanguage* \[ adicional\]
</dt> <dd>

Cadeia de caracteres que contém a linguagem de consulta a ser usada. Se especificado, esse valor deve ser "WQL".

</dd> <dt>

*iFlags* \[ adicional\]
</dt> <dd>

Inteiro que determina o comportamento da consulta. Esse parâmetro pode ser definido com os valores a seguir.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus * * * * (128 (0x80))


</dt> <dd>

Faz com que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus * * * * (0 (0x0))


</dt> <dd>

Impede que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ adicional\]
</dt> <dd>

Normalmente, isso é indefinido. Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que presta a solicitação. Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.

</dd> <dt>

*objWbemAsyncContext* \[ adicional\]
</dt> <dd>

Esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que retorna ao coletor de objeto para identificar a origem da chamada assíncrona original. Use esse parâmetro para fazer várias chamadas assíncronas usando o mesmo coletor de objeto. Para usar esse parâmetro, crie um objeto **SWbemNamedValueSet** e use o método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo. O objeto **SWbemNamedValueSet** é retornado para o coletor de objeto e a origem da chamada pode ser extraída usando o método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) . Para obter mais informações, consulte [chamando um método](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor. Se for bem-sucedido, o coletor receberá um evento [**OnObjectReady**](swbemsink-onobjectready.md) por instância. Após a última instância, o coletor de objeto recebe um evento [**OnCompleted**](swbemsink-oncompleted.md) .

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **ExecNotificationQueryAsync** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro identificados na lista a seguir.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

O usuário atual não está autorizado a exibir o conjunto de resultados.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Parâmetro inválido especificado.

</dd> <dt>

**wbemErrInvalidQuery** -2147749911 (0x80041017)
</dt> <dd>

Sintaxe de consulta inválida.

</dd> <dt>

**wbemErrInvalidQueryType** -2147749912 (0x80041018)
</dt> <dd>

Não há suporte para a linguagem de consulta solicitada.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> </dl>

## <a name="remarks"></a>Comentários

O método **ExecNotificationQueryAsync** retorna objetos de tipo de evento que geram eventos futuros. Os objetos de evento que **ExecNotificationQueryAsync** solicitações podem ser intrínsecos (por exemplo, [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)) ou extrínsecos (por exemplo, eventos de [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) ou SNMP). Para obter mais informações, consulte [determinando o tipo de evento a ser recebido](determining-the-type-of-event-to-receive.md).

A chamada para **ExecNotificationQueryAsync** retorna imediatamente. Os objetos e status solicitados são retornados ao chamador por meio de retornos de chamada entregues ao coletor especificado em *objWbemSink*. Para processar cada objeto quando ele for retornado, crie um *objWbemSink*. Sub-rotina de evento [**OnObjectReady**](swbemsink-onobjectready.md) . Depois que todos os objetos forem retornados, execute o processamento final para implementar o *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .

Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor. Isso representa riscos de segurança para seus scripts e aplicativos. Para eliminar os riscos, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).

Há limites para o número de palavras-chave **and** e **or** que podem ser usadas em consultas WQL. Grandes números de palavras-chave WQL usadas em uma consulta complexa podem fazer com que o WMI retorne o código de erro de **\_ \_ \_ violação E de cota** de Asan valor de **HRESULT** . O limite de palavras-chave WQL depende da complexidade da consulta.

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir mostra um script que está aguardando uma notificação de evento WMI que indica que um processo foi encerrado. Ele está aguardando um evento intrínseco do WMI, uma instância da classe de evento [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md). O **\_ \_ InstanceDeletionEvent** deve representar a exclusão de uma instância do [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process). Para obter mais informações sobre eventos intrínsecos do WMI, consulte [determinando o tipo de evento a ser recebido](determining-the-type-of-event-to-receive.md).

O script a seguir é executado indefinidamente até que o computador seja reinicializado, o WMI é interrompido ou o script é interrompido. Para interromper o script manualmente, use o Gerenciador de tarefas para interromper o processo. Para interrompê-lo programaticamente, use o método [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) na classe de processo do Win32 \_ .


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMSERVICES CLSID<br/>                                                         |
| IID<br/>                      | ISWbemServices de IID \_<br/>                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemServices.ExecQuery**](swbemservices-execquery.md)
</dt> <dt>

[**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md)
</dt> <dt>

[Registrando para eventos de registro do sistema](registering-for-system-registry-events.md)
</dt> <dt>

[Determinando o tipo de evento a ser recebido](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[Chamando um método](calling-a-method.md)
</dt> <dt>

[Definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md)
</dt> </dl>

 

