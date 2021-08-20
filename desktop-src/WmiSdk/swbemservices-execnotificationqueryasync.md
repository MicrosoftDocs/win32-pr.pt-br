---
description: Executa uma consulta para receber eventos.
ms.assetid: 0b0e8313-4ffd-4d4a-8965-d2c6743e7573
ms.tgt_platform: multiple
title: SWbemServices.Exemétodo cNotificationQueryAsync (Wbemdisp.h)
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
ms.openlocfilehash: 0f6c02be1be258f84afcbc941dafdaae6b492f995c25d9718ddbf719c347ae27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118108030"
---
# <a name="swbemservicesexecnotificationqueryasync-method"></a>SWbemServices.Exemétodo cNotificationQueryAsync

O **método ExecNotificationQueryAsync** do objeto [**SWbemServices**](swbemservices.md) executa uma consulta para receber eventos. Essa chamada retorna imediatamente e os resultados e o status são retornados ao chamador por meio de eventos entregues ao sink especificado em *objWbemSink.*

Os eventos especificados na consulta podem ser eventos intrínsecos Windows WMI (Instrumentação de Gerenciamento), como [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)ou eventos extrínsecos, como [**Win32 \_ IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent) ou [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent). Para obter mais informações, [consulte Determinando o tipo de evento a ser recebido.](determining-the-type-of-event-to-receive.md)

O método é chamado no modo assíncrono. Para obter mais informações, consulte [Chamando um método](calling-a-method.md).

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

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

Obrigatórios. O sink do objeto que recebe a notificação de eventos de forma assíncrona. Crie um [**objeto SWbemSink**](swbemsink.md) para receber os objetos.

</dd> <dt>

*strQuery* 
</dt> <dd>

Obrigatórios. Cadeia de caracteres que contém o texto da consulta relacionada ao evento. Esse parâmetro não pode estar em branco. Para obter mais informações sobre como criar cadeias de caracteres de consulta WMI, consulte Consultando com [WQL](querying-with-wql.md) e a [referência WQL.](wql-sql-for-wmi.md)

</dd> <dt>

*strQueryLanguage* \[ Opcional\]
</dt> <dd>

Cadeia de caracteres que contém a linguagem de consulta a ser usada. Se especificado, esse valor deve ser "WQL".

</dd> <dt>

*iFlags* \[ Opcional\]
</dt> <dd>

Inteiro que determina o comportamento da consulta. Esse parâmetro pode ser definido com os valores a seguir.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus*** (128 (0x80))


</dt> <dd>

Faz com que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o sink do objeto.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus*** (0 (0x0))


</dt> <dd>

Impede que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o sink do objeto.

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ Opcional\]
</dt> <dd>

Normalmente, isso é indefinido. Caso contrário, esse é [**um objeto SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que serviços a solicitação. Um provedor que dá suporte ou requer essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.

</dd> <dt>

*objWbemAsyncContext* \[ Opcional\]
</dt> <dd>

Este é um [**objeto SWbemNamedValueSet**](swbemnamedvalueset.md) que retorna ao sink do objeto para identificar a origem da chamada assíncrona original. Use esse parâmetro para fazer várias chamadas assíncronas usando o mesmo sink de objeto. Para usar esse parâmetro, crie um objeto **SWbemNamedValueSet** e use o método [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo. O **objeto SWbemNamedValueSet** é retornado ao sink do objeto e a origem da chamada pode ser extraída usando o [**método SWbemNamedValueSet.Item.**](swbemnamedvalueset-item.md) Para obter mais informações, consulte [Chamando um método](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor. Se for bem-sucedido, o sink receberá um [**evento OnObjectReady**](swbemsink-onobjectready.md) por instância. Após a última instância, o sink do objeto recebe [**um evento OnCompleted.**](swbemsink-oncompleted.md)

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do **método ExecNotificationQueryAsync,** o [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro identificados na lista a seguir.

<dl> <dt>

**wbemErrAccessDenied** – 2147749891 (0x80041003)
</dt> <dd>

O usuário atual não está autorizado a exibir o conjunto de resultados.

</dd> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

O parâmetro inválido é especificado.

</dd> <dt>

**wbemErrInvalidQuery** – 2147749911 (0x80041017)
</dt> <dd>

A sintaxe de consulta não é válida.

</dd> <dt>

**wbemErrInvalidQueryType** – 2147749912 (0x80041018)
</dt> <dd>

Não há suporte para a linguagem de consulta solicitada.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> </dl>

## <a name="remarks"></a>Comentários

O **método ExecNotificationQueryAsync** retorna objetos de tipo de evento que eventos futuros geram. Os objetos de evento que **ExecNotificationQueryAsync** solicita podem ser intrínsecos (por exemplo, [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)) ou extrínsecos (por exemplo, [**eventos RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) ou SNMP). Para obter mais informações, [consulte Determinando o tipo de evento a ser recebido.](determining-the-type-of-event-to-receive.md)

A chamada para **ExecNotificationQueryAsync** retorna imediatamente. Os objetos e o status solicitados são retornados ao chamador por meio de retornos de chamada entregues ao sink especificado em *objWbemSink.* Para processar cada objeto quando ele for retornado, crie *um objWbemSink.* Sub-rotina de evento [**OnObjectReady.**](swbemsink-onobjectready.md) Depois que todos os objetos são retornados, execute o processamento final para implementar *o objWbemSink.* [**Evento OnCompleted.**](swbemsink-oncompleted.md)

Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o sink. Isso representa riscos de segurança para seus scripts e aplicativos. Para eliminar os riscos, consulte [Definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).

Há limites para o número de palavras-chave **AND** e **OR** que podem ser usadas em consultas WQL. Um grande número de palavras-chave WQL usadas em uma consulta complexa pode fazer com que o WMI retorne o código de erro **WBEM \_ E \_ QUOTA \_ VIOLATION** como um **valor HRESULT.** O limite de palavras-chave WQL depende de quão complexa a consulta é.

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir mostra um script que está aguardando uma notificação de evento WMI que indica que um processo foi encerrado. Ele está aguardando um evento intrínseco WMI, uma instância da classe de evento [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md). O **\_ \_ InstanceDeletionEvent** deve representar a exclusão de uma instância do [**Processo win32. \_**](/windows/desktop/CIMWin32Prov/win32-process) Para obter mais informações sobre eventos intrínsecos do WMI, consulte [Determinando o tipo de evento a ser recebido.](determining-the-type-of-event-to-receive.md)

O script a seguir é executado indefinidamente até que o computador seja reinicializado, o WMI seja interrompido ou o script seja interrompido. Para interromper o script manualmente, use Gerenciador de Tarefas para interromper o processo. Para interromper programaticamente, use o [**método Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) na classe Processo Win32. \_


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
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemServices<br/>                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemServices.ExecQuery**](swbemservices-execquery.md)
</dt> <dt>

[**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md)
</dt> <dt>

[Registrando-se para eventos do Registro do Sistema](registering-for-system-registry-events.md)
</dt> <dt>

[Determinando o tipo de evento a ser recebido](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[Chamando um método](calling-a-method.md)
</dt> <dt>

[Definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md)
</dt> </dl>

 

