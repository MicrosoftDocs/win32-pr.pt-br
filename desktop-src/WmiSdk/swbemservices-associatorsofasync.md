---
description: Método SWbemServices. AssociatorsOfAsync – retorna uma coleção de objetos (classes ou instâncias) chamadas de pontos de extremidade que estão associados a um objeto especificado.
ms.assetid: 3969d90f-d39c-40f1-9328-fc1afbaa53b1
ms.tgt_platform: multiple
title: Método SWbemServices. AssociatorsOfAsync (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.AssociatorsOfAsync
- ISWbemServices.AssociatorsOfAsync
- ISWbemServices.AssociatorsOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4b16eed97c891b4b4f5bd283496868d99f9e0fbc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103664"
---
# <a name="swbemservicesassociatorsofasync-method"></a>Método SWbemServices. AssociatorsOfAsync

O método **AssociatorsOfAsync** do objeto [**SWbemServices**](swbemservices.md) retorna uma coleção de objetos (classes ou instâncias) chamada pontos de extremidade que estão associados a um objeto especificado. A chamada para **AssociatorsOfAsync** retorna imediatamente, e os resultados e o status são retornados para o chamador por meio de eventos entregues ao coletor especificado em *objWbemSink*. Para lidar com cada objeto retornado, crie um *objWbemSink*. Manipulador de eventos [**OnObjectReady**](swbemsink-onobjectready.md) .

Depois que todos os objetos chegarem, o processamento será feito no *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) . Esse método executa a mesma função que os ASSOCIAdores da consulta WQL executam. Para obter mais informações sobre como criar um coletor, consulte [recebendo um evento WMI](receiving-a-wmi-event.md).

O método é chamado no modo assíncrono. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
SWbemServices.AssociatorsOfAsync( _
  ByVal objWbemSink, _
  ByVal strObjectPath, _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*objWbemSink* 
</dt> <dd>

Obrigatórios. Coletor de objeto que recebe os objetos de forma assíncrona. Crie um objeto [**SWbemSink**](swbemsink.md) para receber os objetos.

</dd> <dt>

*strObjectPath* 
</dt> <dd>

Obrigatórios. Cadeia de caracteres que contém o caminho do objeto da classe ou instância de origem. Para obter mais informações, consulte [descrevendo o local de um objeto WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*strAssocClass* \[ adicional\]
</dt> <dd>

Cadeia de caracteres que contém uma classe de associação. Quando especificado, esse parâmetro indica que os pontos de extremidade retornados devem ser associados à origem por meio da classe de associação especificada ou de uma classe derivada dessa classe de associação.

</dd> <dt>

*strResultClass* \[ adicional\]
</dt> <dd>

Cadeia de caracteres que contém um nome de classe. Se especificado, esse parâmetro opcional indica que os pontos de extremidade retornados devem pertencer ou ser derivados da classe especificada nesse parâmetro.

</dd> <dt>

*strResultRole* \[ adicional\]
</dt> <dd>

Cadeia de caracteres que contém um nome de propriedade. Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem reproduzir uma função específica em sua associação com o objeto de origem. A função é definida pelo nome de uma propriedade especificada (que deve ser uma propriedade de referência) de uma associação.

</dd> <dt>

*strRole* \[ adicional\]
</dt> <dd>

Cadeia de caracteres que contém um nome de propriedade. Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem participar de uma associação com o objeto de origem no qual o objeto de origem desempenha uma função específica. A função é definida pelo nome de uma propriedade especificada (que deve ser uma propriedade de referência) de uma associação.

</dd> <dt>

*bClassesOnly* \[ adicional\]
</dt> <dd>

Valor booliano que indica se uma lista de nomes de classe deve ser retornada em vez de instâncias reais das classes. Essas são as classes às quais as instâncias de ponto de extremidade pertencem. O valor padrão para esse parâmetro é **false**.

</dd> <dt>

*bSchemaOnly* \[ adicional\]
</dt> <dd>

Valor booliano que indica se a consulta se aplica ao esquema em vez dos dados. O valor padrão para esse parâmetro é **false**. Ele só poderá ser definido como **true** se o parâmetro *strObjectPath* especificar o caminho do objeto de uma classe. Quando definido como **true**, o conjunto de pontos de extremidade retornados representa classes que são adequadamente associadas à classe de origem no esquema.

</dd> <dt>

*strRequiredAssocQualifier* \[ adicional\]
</dt> <dd>

Cadeia de caracteres que contém um nome de qualificador. Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem ser associados ao objeto de origem por meio de uma classe de associação que inclui o qualificador especificado.

</dd> <dt>

*strRequiredQualifier* \[ adicional\]
</dt> <dd>

Cadeia de caracteres que contém um nome de qualificador. Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem incluir o qualificador especificado.

</dd> <dt>

*iFlags* \[ adicional\]
</dt> <dd>

Inteiro que especifica os sinalizadores adicionais para a operação. O padrão para esse parâmetro é **wbemFlagDontSendStatus**. Esse parâmetro pode aceitar os valores a seguir.

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

Faz com que o WMI retorne dados de alteração de classe junto com a definição de classe base. Para obter mais informações sobre qualificadores corrigidos, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ adicional\]
</dt> <dd>

Normalmente, isso é indefinido. Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação. Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.

</dd> <dt>

*objWbemAsyncContext* \[ adicional\]
</dt> <dd>

Um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que retorna ao coletor de objeto para identificar a origem da chamada assíncrona original. Use esse parâmetro se você estiver fazendo várias chamadas assíncronas usando o mesmo coletor de objetos. Para usar esse parâmetro, crie um objeto **SWbemNamedValueSet** e use o método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo. Esse objeto **SWbemNamedValueSet** é retornado para o coletor de objeto e a origem da chamada pode ser extraída usando o método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) . Para obter mais informações, consulte [chamando um método](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor. Se for bem-sucedido, o coletor receberá um evento [**OnObjectReady**](swbemsink-onobjectready.md) por instância. Após a última instância, o coletor de objeto recebe um evento [**OnCompleted**](swbemsink-oncompleted.md) .

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **AssociatorsOfAsync** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

O usuário atual não tem permissão para exibir uma ou mais das classes retornadas pela chamada.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Foi especificado um parâmetro inválido.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

O item solicitado não foi encontrado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa chamada retorna imediatamente. Os objetos e status solicitados são retornados ao chamador por meio de retornos de chamada entregues ao coletor especificado em *objWbemSink*. Para processar cada objeto quando ele retornar, crie um *objWbemSink*. Sub-rotina de evento [**OnObjectReady**](swbemsink-onobjectready.md) . Depois que todos os objetos forem retornados, você poderá executar o processamento final em sua implementação do *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .

Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor. Isso representa riscos de segurança para seus scripts e aplicativos. Para eliminar os riscos, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).

Use o parâmetro *objWbemAsyncContext* em scripts para verificar a origem de uma chamada.

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



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemObject. ASSOCIATORS\_**](swbemobject-associators-.md)
</dt> <dt>

[**SWbemObject. AssociatorsAsync\_**](swbemobject-associatorsasync-.md)
</dt> <dt>

[**SWbemObject. referências\_**](swbemobject-references-.md)
</dt> <dt>

[**SWbemObject. ReferencesAsync\_**](swbemobject-referencesasync-.md)
</dt> <dt>

[**SWbemServices. References**](swbemservices-referencesto.md)
</dt> <dt>

[**SWbemServices. ReferencesToAsync**](swbemservices-referencestoasync.md)
</dt> </dl>

 

