---
description: Recupera um objeto, que é uma definição de classe ou uma instância, com base no caminho do objeto.
ms.assetid: 8da46851-52b8-4b5a-8c9d-1d492f57f4b6
ms.tgt_platform: multiple
title: Método SWbemServices. getasync (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.GetAsync
- ISWbemServices.GetAsync
- ISWbemServices.GetAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d507779493563556d250823cc1be0228731c55ced66911b4f530936b75afdf70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071476"
---
# <a name="swbemservicesgetasync-method"></a>Método SWbemServices. getasync

O método **getasync** do objeto [**SWbemServices**](swbemservices.md) recupera um objeto, que é uma definição de classe ou uma instância, com base no caminho do objeto.

Esse método recupera somente objetos do namespace que está associado ao objeto [**SWbemServices**](swbemservices.md) atual.

Esse método é chamado no modo assíncrono. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
SWbemServices.GetAsync( _
  ByVal objWbemSink, _
  [ ByVal strObjectPath ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*objWbemSink* 
</dt> <dd>

Obrigatórios. Coletor de objeto que obtém objetos de forma assíncrona. Crie um objeto [**SWbemSink**](swbemsink.md) para receber os objetos.

</dd> <dt>

*strObjectPath* \[ adicional\]
</dt> <dd>

Caminho do objeto que você deseja recuperar. Se esse valor estiver vazio, o objeto vazio retornado poderá se tornar uma nova classe. Para obter mais informações, consulte [descrevendo o local de um objeto WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*iFlags* \[ adicional\]
</dt> <dd>

Inteiro que determina o comportamento da chamada. Esse parâmetro pode aceitar os valores a seguir.

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

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers * * * * (131072 (0x20000))


</dt> <dd>

Faz com que o WMI retorne dados de alteração de classe com a definição de classe base. Para obter mais informações, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ adicional\]
</dt> <dd>

Normalmente, esse valor é indefinido. Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação. Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.

</dd> <dt>

*objWbemAsyncContext* \[ adicional\]
</dt> <dd>

Um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que retorna ao coletor de objeto para identificar a origem da chamada assíncrona original. Use esse parâmetro se você estiver fazendo várias chamadas assíncronas usando o mesmo coletor de objetos. Para usar esse parâmetro, crie um objeto **SWbemNamedValueSet** e use o método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo. Esse objeto **SWbemNamedValueSet** é retornado para o coletor de objeto e a origem da chamada pode ser extraída usando o método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) . Para obter mais informações, consulte [chamando um método](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor. Se for bem-sucedido, o coletor receberá um evento [**OnObjectReady**](swbemsink-onobjectready.md) quando o objeto estiver disponível.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **getasync** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

O usuário atual não tem permissão para acessar o objeto.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Um parâmetro especificado não é válido.

</dd> <dt>

**wbemErrInvalidObjectPath** -2147749946 (0x8004103A)
</dt> <dd>

O caminho especificado não era válido.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

O objeto solicitado não foi encontrado.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa chamada retorna imediatamente. O objeto solicitado e o status são retornados para o chamador por meio de um retorno de chamada entregue ao coletor especificado em *objWbemSink*. Para processar o objeto quando ele retornar, crie um *objWbemSink*. [**OnObjectReady**](swbemsink-onobjectready.md), ou um *objWbemSink*. Sub-rotina de evento [**OnCompleted**](swbemsink-oncompleted.md) .

Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor. Isso representa riscos de segurança para seus scripts e aplicativos. Para eliminar os riscos, use semisynchronous ou comunicação síncrona. Para obter mais informações, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMSERVICES CLSID<br/>                                                         |
| IID<br/>                      | ISWbemServices de IID \_<br/>                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemObject**](swbemobject.md)
</dt> </dl>

 

