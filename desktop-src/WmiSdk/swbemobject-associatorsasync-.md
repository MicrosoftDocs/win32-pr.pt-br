---
description: O método AssociatorsAsync \_ de SWbemObject obtém objetos (classes ou instâncias) associados ao objeto atual. Esses objetos são chamados de pontos de extremidade. Esse método executa a mesma função que a consulta ASSOCIATORS OF WQL executa.
ms.assetid: c71e11cd-39a5-40d8-b279-f5ee9ff3ae04
ms.tgt_platform: multiple
title: SWbemObject.AssociatorsAsync_ método (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.AssociatorsAsync_
- ISWbemObject.AssociatorsAsync_
- ISWbemObject.AssociatorsAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b0a8cb6a3bf5099821e50e85699b1327462ee12ef6af10e3ebc3cc9fe0bf7f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314104"
---
# <a name="swbemobjectassociatorsasync_-method"></a>Método SWbemObject.AssociatorsAsync \_

O **método AssociatorsAsync \_** de [**SWbemObject**](swbemobject.md) obtém objetos (classes ou instâncias) associados ao objeto atual. Esses objetos são chamados de pontos de extremidade. Esse método executa a mesma função que a consulta ASSOCIATORS OF WQL executa.

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
SWbemObject.AssociatorsAsync_( _
  ByVal objWbemSink, _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*objWbemSink* \[ Em\]
</dt> <dd>

Obrigatórios. O sink do objeto que recebe os objetos de forma assíncrona como um retorno de chamada.

</dd> <dt>

*strAssocClass* \[ in, opcional\]
</dt> <dd>

Cadeia de caracteres que contém uma classe de associação. Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem ser associados à origem por meio da classe de associação especificada ou de uma classe derivada dessa classe de associação.

</dd> <dt>

*strResultClass* \[ in, opcional\]
</dt> <dd>

Cadeia de caracteres que contém um nome de classe. Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem pertencer ou ser derivados da classe especificada neste parâmetro.

</dd> <dt>

*strResultRole* \[ in, opcional\]
</dt> <dd>

Cadeia de caracteres que contém um nome de propriedade. Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem desempenhar uma função específica em sua associação com o objeto de origem. A função é definida pelo nome de uma propriedade especificada (que deve ser uma propriedade de referência) de uma associação.

</dd> <dt>

*strRole* \[ in, opcional\]
</dt> <dd>

Cadeia de caracteres que contém um nome de propriedade. Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem participar de uma associação com o objeto de origem no qual o objeto de origem desempenha uma função específica. A função é definida pelo nome de uma propriedade especificada (que deve ser uma propriedade de referência) de uma associação.

</dd> <dt>

*bClassesOnly* \[ in, opcional\]
</dt> <dd>

Valor booliana que indica se uma lista de nomes de classe deve ser retornada em vez de instâncias reais das classes. Essas são as classes às quais as instâncias de ponto de extremidade pertencem. O valor padrão para esse parâmetro é **FALSE.**

</dd> <dt>

*bSchemaOnly* \[ in, opcional\]
</dt> <dd>

Valor booliana que indica se a consulta se aplica ao esquema em vez dos dados. O valor padrão para esse parâmetro é **FALSE.** Ele só poderá ser definido como **TRUE** se o objeto no qual esse método é invocado for uma classe . Quando definido como **TRUE**, o conjunto de pontos de extremidade retornados representa classes que são associadas de maneira adequada à classe de origem no esquema.

</dd> <dt>

*strRequiredAssocQualifier* \[ in, opcional\]
</dt> <dd>

Cadeia de caracteres que contém um nome de qualificador. Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem ser associados ao objeto de origem por meio de uma classe de associação que inclui o qualificador especificado.

</dd> <dt>

*strRequiredQualifier* \[ in, opcional\]
</dt> <dd>

Cadeia de caracteres que contém um nome de qualificador. Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem incluir o qualificador especificado.

</dd> <dt>

*iFlags* \[ in, opcional\]
</dt> <dd>

Inteiro especificando sinalizadores adicionais para a operação. Esse parâmetro pode aceitar os valores a seguir.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus*** (128 (0x80))


</dt> <dd>

Faz com que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**SWbemSink.OnProgress**](swbemsink-onprogress.md) para o sink do objeto.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus*** (0 (0x0))


</dt> <dd>

Impede que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o sink do objeto.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers*** (131072 (0x20000))


</dt> <dd>

Faz com que o WMI retorne as descrições de classe e propriedade localizadas. Para obter mais informações, consulte [Localizando informações de classe WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ in, opcional\]
</dt> <dd>

Normalmente, isso é indefinido. Caso contrário, esse é [**um objeto SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação. Um provedor que dá suporte ou requer essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.

</dd> <dt>

*objWbemAsyncContext* \[ in, opcional\]
</dt> <dd>

Este é um [**objeto SWbemNamedValueSet**](swbemnamedvalueset.md) que retorna ao sink do objeto para identificar a origem da chamada assíncrona original. Use esse parâmetro se você estiver fazendo várias chamadas assíncronas usando o mesmo sink de objeto. Para usar esse parâmetro, crie um objeto **SWbemNamedValueSet** e use o método [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo. Esse **objeto SWbemNamedValueSet** é retornado ao sink do objeto e a origem da chamada pode ser extraída usando o [**método SWbemNamedValueSet.Item.**](swbemnamedvalueset-item.md) Para obter mais informações, consulte [Chamando um método](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor. Se for bem-sucedido, o sink receberá um [**evento OnObjectReady**](swbemsink-onobjectready.md) por instância. Após a última instância, o sink do objeto recebe [**um evento OnCompleted.**](swbemsink-oncompleted.md)

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do **método \_ AssociatorsAsync,** o [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrAccessDenied** – 2147749891 (0x80041003)
</dt> <dd>

O usuário atual não tem permissão para exibir uma ou mais das classes retornadas pela chamada.

</dd> <dt>

**wbemErrFailed** – 2147449889 (0x7FFF7C21)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Um parâmetro especificado não é válido.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa chamada retorna imediatamente. Os objetos e o status solicitados são retornados ao chamador por meio de retornos de chamada entregues ao sink especificado em *objWbemSink.* Para processar cada objeto quando ele chegar, crie um *objWbemSink.* Sub-rotina de evento [**OnObjectReady.**](swbemsink-onobjectready.md) Depois que todos os objetos são retornados, você pode executar o processamento final em sua implementação *do objWbemSink.* [**Evento OnCompleted.**](swbemsink-oncompleted.md)

Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o sink. Isso representa riscos de segurança para seus scripts e aplicativos. Para eliminar os riscos, use comunicação síncrona ou comunicação síncrona. Para obter mais informações, consulte [Chamando um método](calling-a-method.md).

Para obter mais informações sobre as consultas WQL associadas a ASSOCIATORS OF, instâncias de origem e pontos de extremidade, consulte [instrução ASSOCIATORS OF](associators-of-statement.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | ISWbemObject de IID \_<br/>                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[**SWbemServices. AssociatorsOfAsync**](swbemservices-associatorsofasync.md)
</dt> <dt>

[**SWbemObject. referências\_**](swbemobject-references-.md)
</dt> <dt>

[**SWbemServices. References**](swbemservices-referencesto.md)
</dt> </dl>

 

