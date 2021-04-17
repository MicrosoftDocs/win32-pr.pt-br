---
description: Retorna uma coleção de objetos (classes ou instâncias) chamadas de pontos de extremidade que estão associados a um objeto especificado.
ms.assetid: a78e6701-6779-4a02-b811-23b2da4f4167
ms.tgt_platform: multiple
title: Método SWbemServices. AssociatorsOf (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.AssociatorsOf
- ISWbemServices.AssociatorsOf
- ISWbemServices.AssociatorsOf
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0208ef23158d71a5174fcb6759acba1d64bd09a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770314"
---
# <a name="swbemservicesassociatorsof-method"></a>Método SWbemServices. AssociatorsOf

O método **AssociatorsOf** do objeto [**SWbemServices**](swbemservices.md) retorna uma coleção de objetos (classes ou instâncias) chamada pontos de extremidade que estão associados a um objeto especificado. Esse método executa a mesma função que os ASSOCIAdores da consulta WQL executam.

Esse método é chamado no modo semisynchronous por padrão. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objWbemObjectSet = .AssociatorsOf( _
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
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strObjectPath* 
</dt> <dd>

Obrigatórios. Cadeia de caracteres que contém o caminho do objeto da classe ou instância de origem. Para obter mais informações, consulte [descrevendo o local de um objeto WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*strAssocClass* \[ adicional\]
</dt> <dd>

Cadeia de caracteres que contém uma classe de associação. Se especificado, esse parâmetro indica que os pontos de extremidade retornados devem ser associados à origem por meio da classe de associação especificada ou de uma classe derivada dessa classe de associação.

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

Inteiro que especifica sinalizadores adicionais para a operação. O valor padrão para esse parâmetro é **wbemFlagReturnImmediately**, que chama o método no modo semisynchronous. Esse parâmetro pode aceitar os valores a seguir.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly * * * * (32 (0x20))


</dt> <dd>

Faz com que um enumerador somente de encaminhamento seja retornado. Enumeradores de somente encaminhamento são geralmente muito mais rápidos e usam menos memória do que enumeradores convencionais, mas não permitem chamadas para [**SWbemObject. \_ clone**](swbemobject-clone-.md).

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional * * * * (0 (0x0))


</dt> <dd>

Faz com que o WMI retenha ponteiros para objetos da enumeração até que o cliente libere o enumerador.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately * * * * (16 (0x10))


</dt> <dd>

Faz com que a chamada retorne imediatamente.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete * * * * (0 (0x0))


</dt> <dd>

Faz com que essa chamada seja bloqueada até que a consulta seja concluída. Esse sinalizador chama o método no modo síncrono.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers * * * * (131072 (0x20000))


</dt> <dd>

Faz com que o WMI retorne dados de alteração de classe junto com a definição de classe base. Para obter mais informações, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ adicional\]
</dt> <dd>

Normalmente, isso é indefinido. Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação. Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a chamada for bem-sucedida, um objeto [**SWbemObjectSet**](swbemobjectset.md) será retornado.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **AssociatorsOf** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.

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

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

O item solicitado não foi encontrado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O método recupera as instâncias de recursos gerenciados que estão associados a um recurso especificado por meio de uma ou mais classes de associação. Você fornece o caminho do objeto para o ponto de extremidade de origem e AssociatorsOf retorna os recursos gerenciados no ponto de extremidade oposto. O método AssociatorsOf executa a mesma função que os ASSOCIAdores da consulta WQL executam.

Para obter mais informações sobre os ASSOCIAdores de consulta WQL, instâncias de origem e pontos de extremidade, consulte [ASSOCIATORS of Statement](associators-of-statement.md).

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

[**SWbemObject. AssociatorsAsync\_**](swbemobject-associatorsasync-.md)
</dt> <dt>

[**SWbemServices. AssociatorsOfAsync**](swbemservices-associatorsofasync.md)
</dt> <dt>

[**SWbemObject. referências\_**](swbemobject-references-.md)
</dt> <dt>

[**SWbemServices. References**](swbemservices-referencesto.md)
</dt> </dl>

 

 




