---
description: Retorna todas as classes de associação ou instâncias que se referem a uma classe ou instância de origem específica.
ms.assetid: 2ad66ea1-b8f0-4b6b-b68f-29496afbe4bf
ms.tgt_platform: multiple
title: Método SWbemServices. ReferencesToAsync (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ReferencesToAsync
- ISWbemServices.ReferencesToAsync
- ISWbemServices.ReferencesToAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 64a8b9b336a1e7aa6007b17d2e878f1ace5e6163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785125"
---
# <a name="swbemservicesreferencestoasync-method"></a>Método SWbemServices. ReferencesToAsync

O método **ReferencesToAsync** do objeto [**SWbemServices**](swbemservices.md) retorna todas as classes ou instâncias de associação que se referem a uma classe ou instância de origem específica. Esse método executa a mesma função que as [referências da](references-of-statement.md) consulta WQL executa.

Para obter mais informações sobre o modo assíncrono, consulte [chamando um método](calling-a-method.md).

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
SWbemServices.ReferencesToAsync( _
  ByVal ObjWbemSink, _
  ByVal strObjectPath, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ObjWbemSink* 
</dt> <dd>

Obrigatórios. Coletor de objeto que recebe os objetos de forma assíncrona. Crie um objeto [**SWbemSink**](swbemsink.md) para receber os objetos.

</dd> <dt>

*strObjectPath* 
</dt> <dd>

Obrigatórios. Cadeia de caracteres que contém o caminho do objeto da origem para esse método. Para obter mais informações, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).

</dd> <dt>

*strResultClass* \[ adicional\]
</dt> <dd>

Cadeia de caracteres que contém um nome de classe. Se especificado, esse parâmetro indica que os objetos de associação retornados devem pertencer ou ser derivados da classe especificada nesse parâmetro.

</dd> <dt>

*strRole* \[ adicional\]
</dt> <dd>

Cadeia de caracteres que contém um nome de propriedade. Se especificado, esse parâmetro indica que os objetos de associação retornados devem ser limitados àqueles nos quais o objeto de origem desempenha uma função específica. A função é definida pelo nome de uma propriedade de referência especificada de uma associação.

</dd> <dt>

*bClassesOnly* \[ adicional\]
</dt> <dd>

Valor booliano que indica se uma lista de nomes de classe deve ser retornada em vez de instâncias reais das classes. Essas são as classes às quais os objetos de associação pertencem. O valor padrão para esse parâmetro é **false**.

</dd> <dt>

*bSchemaOnly* \[ adicional\]
</dt> <dd>

Valor booliano que indica se a consulta se aplica ou não ao esquema, e não aos dados. O valor padrão para esse parâmetro é **false**. Ele só poderá ser definido como **true** se o parâmetro *strObjectPath* especificar o caminho do objeto de uma classe. Quando definido como **true**, o conjunto de pontos de extremidade retornados representa as classes associadas à classe de origem no esquema.

</dd> <dt>

*strRequiredQualifier* \[ adicional\]
</dt> <dd>

Cadeia de caracteres que contém um nome de qualificador. Se especificado, esse parâmetro indica que os objetos de associação retornados devem incluir o qualificador especificado.

</dd> <dt>

*iFlags* \[ adicional\]
</dt> <dd>

Inteiro que especifica sinalizadores adicionais para a operação. O padrão para esse parâmetro é **wbemFlagBidirectional**. Esse parâmetro pode aceitar os valores a seguir.

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

Faz com que Instrumentação de Gerenciamento do Windows (WMI) retorne dados de alteração de classe junto com a definição de classe base. Para obter mais informações, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ adicional\]
</dt> <dd>

Normalmente, isso é indefinido. Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação. Um provedor que dá suporte ou exige informações de contexto deve documentar os nomes de valores reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.

</dd> <dt>

*objWbemAsyncContext* \[ adicional\]
</dt> <dd>

Esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que retorna ao coletor de objeto para identificar a origem da chamada assíncrona original. Use esse parâmetro para fazer várias chamadas assíncronas usando o mesmo coletor de objeto. Para usar esse parâmetro, crie um objeto **SWbemNamedValueSet** e use o método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo. Esse objeto **SWbemNamedValueSet** é retornado para o coletor de objeto e a origem da chamada pode ser extraída usando o método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) . Para obter mais informações, consulte [chamando um método](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor. Se for bem-sucedido, o coletor receberá um evento [**OnObjectReady**](swbemsink-onobjectready.md) por instância. Após a última instância, o coletor de objeto recebe um evento [**OnCompleted**](swbemsink-oncompleted.md) .

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **ReferencesToAsync** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.

> [!Note]  
> Uma coleção retornada com zero elementos não é um erro.

 

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

Essa chamada retorna imediatamente. Os objetos e status solicitados são retornados ao chamador por meio de retornos de chamada entregues ao coletor especificado em *objWbemSink*. Para processar cada objeto quando ele retornar, crie um *objWbemSink*. Sub-rotina de evento [**OnObjectReady**](swbemsink-onobjectready.md) . Depois que todos os objetos forem retornados, você poderá executar o processamento final em sua implementação do *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .

Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor. Isso representa riscos de segurança para seus scripts e aplicativos. Para eliminar os riscos, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).

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

[**SWbemObject. ASSOCIATORS\_**](swbemobject-associators-.md)
</dt> <dt>

[**SWbemObject. referências\_**](swbemobject-references-.md)
</dt> <dt>

[**SWbemServices. AssociatorsOf**](swbemservices-referencesto.md)
</dt> </dl>

 

