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
# <a name="swbemservicesexecnotificationquery-method"></a>SWbemServices.Exemétodo cNotificationQuery

O método **ExecNotificationQuery** do objeto [**SWbemServices**](swbemservices.md) executa uma consulta para receber eventos. A chamada retorna imediatamente. O usuário pode sondar o enumerador retornado em busca de eventos à medida que eles chegam.

O método é chamado no modo semisynchronous. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objwbemEventsource = .ExecNotificationQuery( _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

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

Este é um inteiro que determina o comportamento da consulta. O valor padrão é **wbemFlagReturnImmediately**  +  **wbemFlagForwardOnly**. Se você especificar esse parâmetro, esse parâmetro deverá ser definido como **wbemFlagReturnImmediately** e **wbemFlagForwardOnly** ou a chamada falhará. Esse parâmetro pode aceitar os valores a seguir.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly * * * * (32 (0x20))


</dt> <dd>

Faz com que um enumerador somente de encaminhamento seja retornado. Enumeradores de somente encaminhamento são geralmente muito mais rápidos e usam menos memória do que enumeradores convencionais, mas não permitem chamadas para [**SWbemObject. \_ clone**](swbemobject-clone-.md).

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately * * * * (16 (0x10))


</dt> <dd>

Faz com que a chamada retorne imediatamente.

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ adicional\]
</dt> <dd>

Normalmente, isso é indefinido. Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação. Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se nenhum erro ocorrer, esse método retornará um objeto [**SWbemEventSource**](swbemeventsource.md) . Você pode chamar o método [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md) para recuperar eventos à medida que eles chegam.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **ExecNotificationQuery** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.

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

Foi especificado um parâmetro inválido.

</dd> <dt>

**wbemErrInvalidQuery** -2147749911 (0x80041017)
</dt> <dd>

Sintaxe de consulta inválida.

</dd> <dt>

**wbemErrInvalidQueryType** -2147749912 (0x80041018)
</dt> <dd>

O idioma de consulta solicitado não tem suporte.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao contrário do método [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md) , **ExecNotificationQuery** retorna objetos de tipo de evento que são gerados por eventos futuros em vez de objetos existentes. Os objetos de evento que **ExecNotificationQuery** solicitações podem ser intrínsecos (como [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)) ou extrínsecos (como eventos de provedor do registro, como [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) ou eventos SNMP). Para obter mais informações, consulte [determinando o tipo de evento para receber](determining-the-type-of-event-to-receive.md) e [receber notificações de eventos](receiving-event-notifications.md).

Há limites para o número de palavras-chave **and** e **or** que podem ser usadas em consultas WQL. Grandes números de palavras-chave WQL usadas em uma consulta complexa podem fazer com que o WMI retorne o código de erro de **\_ \_ \_ violação E de cota de WBEM** como um valor **HRESULT** . O limite de palavras-chave WQL depende da complexidade da consulta.

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir monitora as alterações em volumes em um computador local. Observe que o [**Win32 \_ VolumeChangeEvent**](/windows/desktop/CIMWin32Prov/win32-volumechangeevent) é um evento extrínsecos que é definido por um provedor não é um evento INTRÍNSECO definido pelo WMI. Para obter mais informações, consulte [determinando o tipo de evento a ser recebido](determining-the-type-of-event-to-receive.md).


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



O exemplo de código VBScript a seguir monitora a exclusão do processo. Se você excluir um processo no Gerenciador de tarefas ou fechar um aplicativo, o script exibirá uma mensagem. Observe que esse script consulta um evento intrínseco que é definido por WMI- [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md).


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

[**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md)
</dt> <dt>

[**SWbemServices.ExecQuery**](swbemservices-execquery.md)
</dt> <dt>

[Recebendo um evento WMI](receiving-a-wmi-event.md)
</dt> <dt>

[Consultando com WQL](querying-with-wql.md)
</dt> <dt>

[WQL (SQL para WMI)](wql-sql-for-wmi.md)
</dt> <dt>

[Determinando o tipo de evento a ser recebido](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

