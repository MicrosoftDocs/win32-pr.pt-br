---
description: O método Put de SWbemObject cria ou atualiza uma instância ou um objeto de classe para Windows \_ WMI (Instrumentação de Gerenciamento). Você pode usar esse método depois de modificar quaisquer propriedades ou métodos em um SWbemObject e suas alterações são escritas no WMI.
ms.assetid: c636ff95-9f3e-4ba9-adf3-30b981be02a4
ms.tgt_platform: multiple
title: SWbemObject.Put_ método (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Put_
- ISWbemObject.Put_
- ISWbemObject.Put_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9310f690ea9ffc153e88ee9b0cd5ed489beef107c048f7e00e6891a69800b957
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991966"
---
# <a name="swbemobjectput_-method"></a>Método SWbemObject.Put \_

O **\_ método Put** de [**SWbemObject**](swbemobject.md) cria ou atualiza uma instância ou um objeto de classe para Windows WMI (Instrumentação de Gerenciamento). Você pode usar esse método depois de modificar quaisquer propriedades ou métodos em um **SWbemObject** e suas alterações são escritas no WMI.

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objObjectPath = .Put_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iFlags* \[ in, opcional\]
</dt> <dd>

Esse parâmetro determina se a chamada cria ou atualiza a classe ou a instância e se a chamada retorna imediatamente. Esse parâmetro pode aceitar os valores a seguir.

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>wbemChangeFlagUpdateCompatible*** (0 (0x0))


</dt> <dd>

Permite que uma classe seja atualizada se não houver classes derivadas e não houver instâncias para essa classe. Ele também permitirá atualizações em todos os casos se a alteração for apenas para qualificadores sem importância (por exemplo, o qualificador **Descrição).** Esse é o comportamento padrão para essa chamada e é usado para compatibilidade com versões anteriores do WMI. Se a classe tiver instâncias, a atualização falhará.

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>wbemChangeFlagUpdateSafeMode*** (32 (0x20))


</dt> <dd>

Permite atualizações de classes mesmo se houver classes filho se a alteração não causar conflitos com classes filho. Você pode usar esse sinalizador ao adicionar uma nova propriedade a uma classe base que não foi mencionada anteriormente em nenhuma das classes filho. Se a classe tiver instâncias, a atualização falhará. Se a classe tiver instâncias, a atualização falhará.

</dd> <dt>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>WbemChangeFlagUpdateForceMode*** (64 (0x40))


</dt> <dd>

Esse sinalizador força as atualizações de classes quando existem classes filho conflitantes. Por exemplo, esse sinalizador força uma atualização se um qualificador de classe foi definido em uma classe filho e a classe base tenta adicionar o mesmo qualificador e entrar em conflito com o existente. No modo de força, esse conflito seria resolvido excluindo o qualificador conflitante na classe filho. Se a classe tiver instâncias, a atualização falhará.

Usar o modo de força para atualizar uma classe estática resulta na exclusão de todas as instâncias dessa classe. Uma atualização forçada em uma classe de provedor não exclui instâncias da classe .

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>wbemChangeFlagCreateOrUpdate*** (0 (0x0))


</dt> <dd>

Faz com que a classe ou a instância seja criada se ela não existir ou substituída se ela já existir.

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>wbemChangeFlagCreateOnly*** (2 (0x2))


</dt> <dd>

Usado apenas para criação. A chamada falhará se a classe ou a instância já existir.

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>wbemChangeFlagUpdateOnly*** (1 (0x1))


</dt> <dd>

Faz com que essa chamada seja atualizada. A classe ou a instância deve existir para que a chamada seja bem-sucedida.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately*** (16 (0x10))


</dt> <dd>

Faz com que a chamada retorne imediatamente.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete*** (0 (0x0))


</dt> <dd>

Faz com que essa chamada bloqueie até que a consulta seja concluída.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers*** (131072 (0x20000))


</dt> <dd>

Faz com que o WMI escreva dados de alteração de classe, bem como a definição de classe base. Para obter mais informações sobre qualificadores corrigidos, consulte [Localizando informações de classe WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ in, opcional\]
</dt> <dd>

Normalmente, isso é indefinido. Caso contrário, esse é um [**objeto SWbemObjectPath**](swbemobjectpath.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação. Um provedor que dá suporte ou requer essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a chamada for bem-sucedida, [**um objeto SWbemObjectPath**](swbemobjectpath.md) será retornado. Esse objeto contém o caminho do objeto da instância ou classe que foi comprometida com êxito no WMI.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **\_ Put,** o [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrAccessDenied** – 2147749891
</dt> <dd>

O usuário atual não tem permissão para atualizar uma instância da classe especificada.

</dd> <dt>

**wbemErrAlreadyExists** – 2147749913 (0x80041019)
</dt> <dd>

O **sinalizador wbemChangeFlagCreateOnly** foi especificado, mas a instância já existe.

</dd> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErr LtdgalNull** – 2147749898 (0x8004100A)
</dt> <dd>

Um valor de **Nothing** foi especificado para uma propriedade que pode não ser **Nothing.** Um exemplo dessa propriedade é aquele marcado por um qualificador **Chave,** **Indexado** ou **Não \_ Nulo.**

</dd> <dt>

**wbemErrInvalidObject** – 2147749908 (0x80041014)
</dt> <dd>

A instância especificada é inválida.

</dd> <dt>

**wbemErrInvalidParameter** – 0x80041008
</dt> <dd>

Um parâmetro especificado não é válido.

</dd> <dt>

**wbemErrNotFound** – 2147749890 (0x80041002)
</dt> <dd>

O **sinalizador wbemChangeFlagUpdateOnly** foi especificado, mas a instância ou a classe não existe.

</dd> <dt>

**wbemErrIncompleteClass** – 2147749920 (0x80041020)
</dt> <dd>

As propriedades necessárias para classes não foram definidas.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Swbemobject**](swbemobject.md)
</dt> <dt>

[**SWbemObjectPath.Class**](swbemobjectpath-class.md)
</dt> <dt>

[**SWbemProperty**](swbemproperty.md)
</dt> <dt>

[**SWbemQualifier**](swbemqualifier.md)
</dt> </dl>

 

