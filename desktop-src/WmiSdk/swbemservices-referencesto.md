---
description: Retorna uma coleção de todas as classes ou instâncias de associação que se referem a uma classe ou instância de origem específica.
ms.assetid: 33425b1c-13f5-4c3d-8f8a-2922f3e95264
ms.tgt_platform: multiple
title: Método SWbemServices.ReferencesTo (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ReferencesTo
- ISWbemServices.ReferencesTo
- ISWbemServices.ReferencesTo
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b703ab1384286ecfc3a797f88ec18cafe8b6142acf586c7f96e4ae9b4085f7cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312495"
---
# <a name="swbemservicesreferencesto-method"></a>Método SWbemServices.ReferencesTo

O **método ReferencesTo** do objeto [**SWbemServices**](swbemservices.md) retorna uma coleção de todas as classes de associação ou instâncias que se referem a uma classe ou instância de origem específica. Esse método executa a mesma função que a [consulta REFERENCES OF](references-of-statement.md) WQL executa.

Esse método é chamado no modo semissíncrono. Para obter mais informações, consulte [Chamando um método](calling-a-method.md).

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objWbemObjectSet = .ReferencesTo( _
  ByVal strObjectPath, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strObjectPath* 
</dt> <dd>

Obrigatórios. Cadeia de caracteres que contém o caminho do objeto da origem para esse método. Para obter mais informações, [consulte Descrevendo o local de um objeto WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*strResultClass* \[ Opcional\]
</dt> <dd>

Cadeia de caracteres que contém um nome de classe. Se especificado, esse parâmetro indica que os objetos de associação retornados devem pertencer ou ser derivados da classe especificada nesse parâmetro.

</dd> <dt>

*strRole* \[ Opcional\]
</dt> <dd>

Cadeia de caracteres que contém um nome de propriedade. Se especificado, esse parâmetro indica que os objetos de associação retornados devem ser limitados àqueles em que o objeto de origem desempenha uma função específica. A função é definida pelo nome de uma propriedade especificada (que deve ser uma propriedade de referência) de uma associação.

</dd> <dt>

*bClassesOnly* \[ Opcional\]
</dt> <dd>

Valor booliana que indica se uma lista de nomes de classe deve ou não ser retornada em vez de instâncias reais das classes. Essas são as classes às quais os objetos de associação pertencem. O valor padrão para esse parâmetro é **FALSE.**

</dd> <dt>

*bSchemaOnly* \[ Opcional\]
</dt> <dd>

Valor booliana que indica se a consulta se aplica ou não ao esquema em vez dos dados. O valor padrão para esse parâmetro é **FALSE.** Ele só poderá ser definido como **TRUE se** o *parâmetro strObjectPath* especificar o caminho do objeto de uma classe. Quando definido como **TRUE**, o conjunto de pontos de extremidade retornados representa classes que são associadas de maneira adequada à classe de origem no esquema.

</dd> <dt>

*strRequiredQualifier* \[ Opcional\]
</dt> <dd>

Cadeia de caracteres que contém um nome de qualificador. Se especificado, esse parâmetro indica que os objetos de associação retornados devem incluir o qualificador especificado.

</dd> <dt>

*iFlags* \[ Opcional\]
</dt> <dd>

Inteiro que especifica sinalizadores adicionais para a operação. O padrão para esse parâmetro é **wbemFlagReturnImmediately**, que direciona a chamada a retornar imediatamente em vez de aguardar até que a consulta seja concluída. Esse parâmetro pode aceitar os valores a seguir.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly*** (32 (0x20))


</dt> <dd>

Faz com que um enumerador somente de avanço seja retornado. Enumeradores somente avanço geralmente são muito mais rápidos e usam menos memória do que enumeradores convencionais, mas não permitem chamadas para [**SWbemObject.Clone \_**](swbemobject-clone-.md).

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional*** (0 (0x0))


</dt> <dd>

Faz Windows WMI (Instrumentação de Gerenciamento) manter ponteiros para objetos da enumeração até que o cliente libere o enumerador.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately*** (16 (0x10))


</dt> <dd>

Faz com que a chamada retorne imediatamente.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete*** (0 (0x0))


</dt> <dd>

Faz com que essa chamada bloqueie até que a consulta seja concluída. Esse sinalizador chama o método no modo síncrono.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers*** (131072 (0x20000))


</dt> <dd>

Faz com que o WMI retorne dados de alteração de classe junto com a definição de classe base. Para obter mais informações, consulte [Localizando informações de classe WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ Opcional\]
</dt> <dd>

Normalmente, isso é indefinido. Caso contrário, esse é [**um objeto SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação. Um provedor que dá suporte ou requer essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o método retornará [**um objeto SWbemObjectSet.**](swbemobjectset.md)

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do **método ReferencesTo,** o **objeto Err** pode conter um dos códigos de erro na lista a seguir.

> [!Note]  
> Uma coleção retornada com zero elementos não é um erro.

 

<dl> <dt>

**wbemErrAccessDenied** – 2147749891 (0x80041003)
</dt> <dd>

O usuário atual não tem permissão para exibir uma ou mais das classes retornadas pela chamada.

</dd> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Parâmetro inválido foi especificado.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> <dt>

**wbemFlagUseAmendedQualifiers** – 131072 (0x20000)
</dt> <dd>

Faz com que o WMI retorne dados de alteração de classe com a definição de classe base.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para obter mais informações sobre a consulta REFERENCES OF associada do WQL, instâncias de origem e objetos de associação, consulte [instrução ASSOCIATORS OF](associators-of-statement.md).

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

[**SWbemObject.Associators\_**](swbemobject-associators-.md)
</dt> <dt>

[**SWbemObject.References\_**](swbemobject-references-.md)
</dt> <dt>

[**SWbemServices.AssociatorsOf**](swbemservices-associatorsof.md)
</dt> </dl>

 

 




