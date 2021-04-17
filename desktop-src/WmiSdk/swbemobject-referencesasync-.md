---
description: O \_ método ReferencesAsync de SWbemObject fornece uma coleção de todas as classes ou instâncias de associação que se referem ao objeto atual. Esse método executa a mesma função que as referências WQL de consulta executam.
ms.assetid: 44989726-3f68-453b-b9f5-e76fb0fbb152
ms.tgt_platform: multiple
title: Método de SWbemObject.ReferencesAsync_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ReferencesAsync_
- ISWbemObject.ReferencesAsync_
- ISWbemObject.ReferencesAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: aa4b85475a0dc9f736254c8f207469a52897b7ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761843"
---
# <a name="swbemobjectreferencesasync_-method"></a>Método SWbemObject. ReferencesAsync \_

O **método \_ ReferencesAsync** de [**SWbemObject**](swbemobject.md) fornece uma coleção de todas as classes ou instâncias de associação que se referem ao objeto atual. Esse método executa a mesma função que as [referências WQL de](references-of-statement.md) consulta executam.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
SWbemObject.ReferencesAsync_( _
  ByVal objWbemSink, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*objWbemSink* \[ no\]
</dt> <dd>

Obrigatórios. Coletor de objeto que recebe os objetos de forma assíncrona.

</dd> <dt>

*strResultClass* \[ em, opcional\]
</dt> <dd>

Cadeia de caracteres que contém um nome de classe. Se especificado, esse parâmetro indica que os objetos de associação retornados devem pertencer ou ser derivados da classe especificada nesse parâmetro.

</dd> <dt>

*strRole* \[ em, opcional\]
</dt> <dd>

Cadeia de caracteres que contém um nome de propriedade. Se especificado, esse parâmetro indica que os objetos de associação retornados devem ser limitados àqueles nos quais o objeto de origem desempenha uma função específica. O nome de uma propriedade de referência especificada define a função de uma associação.

</dd> <dt>

*bClassesOnly* \[ em, opcional\]
</dt> <dd>

Valor booliano que indica se uma lista de nomes de classe deve ser retornada em vez de instâncias reais das classes. Essas são as classes às quais os objetos de associação pertencem. O valor padrão para esse parâmetro é **false**.

</dd> <dt>

*bSchemaOnly* \[ em, opcional\]
</dt> <dd>

Valor booliano que indica se a consulta se aplica ou não ao esquema, e não aos dados. O valor padrão para esse parâmetro é **false**. Ele só poderá ser definido como **true** se o objeto no qual esse método for invocado for uma classe. Quando definido como **true**, o conjunto de pontos de extremidade retornados representa classes que são adequadamente associadas à classe de origem no esquema.

</dd> <dt>

*strRequiredQualifier* \[ em, opcional\]
</dt> <dd>

Cadeia de caracteres que contém um nome de qualificador. Se especificado, esse parâmetro indica que os objetos de associação retornados devem incluir o qualificador especificado.

</dd> <dt>

*iFlags* \[ em, opcional\]
</dt> <dd>

Inteiro que especifica sinalizadores adicionais para a operação. Esse parâmetro pode aceitar os valores a seguir.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus * * * * (128 (0x80))


</dt> <dd>

Faz com que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**SWbemSink. OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus * * * * (0 (0x0))


</dt> <dd>

Impede que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers * * * * (131072 (0x20000))


</dt> <dd>

Faz com que Instrumentação de Gerenciamento do Windows (WMI) retorne dados de alteração de classe com a definição de classe base. Para obter mais informações, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ em, opcional\]
</dt> <dd>

Normalmente, isso é indefinido. Caso contrário, esse é um objeto [SWbemNamedValueSet](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação. Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.

</dd> <dt>

*objWbemAsyncContext* \[ em, opcional\]
</dt> <dd>

Esse é um objeto [SWbemNamedValueSet](swbemnamedvalueset.md) que retorna ao coletor de objeto para identificar a origem da chamada assíncrona original. Use esse parâmetro se você estiver fazendo várias chamadas assíncronas usando o mesmo coletor de objetos. Para usar esse parâmetro, crie um objeto SWbemNamedValueSet e use o método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo. Esse objeto SWbemNamedValueSet é retornado para o coletor de objeto e a origem da chamada pode ser extraída usando o método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) . Para obter mais informações, consulte [chamando um método](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor. Se for bem-sucedido, o coletor receberá um evento [**OnObjectReady**](swbemsink-onobjectready.md) por instância. Após a última instância, o coletor de objeto recebe um evento [**OnCompleted**](swbemsink-oncompleted.md) .

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **ReferencesAsync \_** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.

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

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa chamada retorna imediatamente. Os objetos e status solicitados são retornados ao chamador por meio de retornos de chamada entregues ao coletor especificado em *objWbemSink*. Para processar cada objeto quando ele chegar, crie um *objWbemSink*. Sub-rotina de evento [**OnObjectReady**](swbemsink-onobjectready.md) . Depois que todos os objetos forem retornados, você poderá executar o processamento final em sua implementação do *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .

Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor. Isso representa riscos de segurança para seus scripts e aplicativos. Para eliminar os riscos, use a comunicação do semisynchronous ou a comunicação síncrona. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

Para obter mais informações sobre as referências de consulta WQL associada, instâncias de origem e objetos de associação, consulte [associars of Statement](associators-of-statement.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | ISWbemObject de IID \_<br/>                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[**SWbemObject. ASSOCIATORS\_**](swbemobject-associators-.md)
</dt> <dt>

[**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md)
</dt> <dt>

[**SWbemServices. References**](swbemservices-referencesto.md)
</dt> <dt>

[**SWbemServices. ReferencesToAsync**](swbemservices-referencestoasync.md)
</dt> </dl>

 

