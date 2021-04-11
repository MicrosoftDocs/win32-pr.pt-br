---
description: O \_ método PutAsync de SWbemObject cria ou atualiza de forma assíncrona uma instância ou um objeto de classe para instrumentação de gerenciamento do Windows (WMI).
ms.assetid: ff738412-fcca-4e4a-a178-0d1d391ec99b
ms.tgt_platform: multiple
title: Método de SWbemObject.PutAsync_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.PutAsync_
- ISWbemObject.PutAsync_
- ISWbemObject.PutAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3530c3883763773f53bec81aeee8b0d199170133
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171792"
---
# <a name="swbemobjectputasync_-method"></a>Método SWbemObject. PutAsync \_

O **método \_ PutAsync** de [**SWbemObject**](swbemobject.md) cria ou atualiza de forma assíncrona uma instância ou um objeto de classe para instrumentação de gerenciamento do Windows (WMI). Você pode usar esse método depois de modificar qualquer propriedade ou método em **SWbemObject** e suas alterações são gravadas no WMI.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
SWbemObject.PutAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*objWbemSink* \[ no\]
</dt> <dd>

Obrigatórios. Coletor de objeto que recebe de forma assíncrona o resultado da operação **Put** .

</dd> <dt>

*iFlags* \[ em, opcional\]
</dt> <dd>

Determina se a chamada cria ou atualiza a classe ou instância e se a chamada retorna imediatamente. Esse parâmetro pode aceitar os valores a seguir.

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>wbemChangeFlagUpdateCompatible * * * * (0 (0x0))


</dt> <dd>

Permite que uma classe seja atualizada se não houver classes derivadas e não houver nenhuma instância para essa classe. Ele também permite atualizações em todos os casos se a alteração for apenas para qualificadores não importantes (por exemplo, o qualificador de **Descrição** ). Esse é o comportamento padrão para essa chamada e é usado para compatibilidade com as versões anteriores do WMI. Se a classe tiver instâncias, a atualização falhará.

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>wbemChangeFlagUpdateSafeMode * * * * (32 (0x20))


</dt> <dd>

Permite atualizações de classes, mesmo se houver classes filhas, se a alteração não causar conflitos com classes filhas. Você pode usar esse sinalizador ao adicionar uma nova propriedade a uma classe base que não foi mencionada anteriormente em nenhuma das classes filhas. Se a classe tiver instâncias, a atualização falhará.

</dd> <dt>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>WbemChangeFlagUpdateForceMode * * * * (64 (0x40))


</dt> <dd>

Força atualizações de classes quando existem classes filhas conflitantes. Por exemplo, esse sinalizador força uma atualização se um qualificador de classe foi definido em uma classe filho e a classe base tenta adicionar o mesmo qualificador em conflito com o existente. Em forçar modo, esse conflito é resolvido com a exclusão do qualificador conflitante na classe filho. Se a classe tiver instâncias, a atualização falhará.

O uso do modo Force para atualizar uma classe estática resulta na exclusão de todas as instâncias dessa classe. Uma atualização forçada em uma classe de provedor não exclui instâncias da classe.

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>wbemChangeFlagCreateOrUpdate * * * * (0 (0x0))


</dt> <dd>

Faz com que a classe ou instância seja criada se ela não existir ou substituída se já existir.

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>wbemChangeFlagCreateOnly * * * * (2 (0x2))


</dt> <dd>

Usado somente para criação. A chamada falhará se a classe ou instância já existir.

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>wbemChangeFlagUpdateOnly * * * * (1 (0x1))


</dt> <dd>

Faz com que essa chamada seja atualizada. A classe ou instância deve existir para que a chamada seja bem-sucedida.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately * * * * (16 (0x10))


</dt> <dd>

Faz com que a chamada retorne imediatamente.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete * * * * (0 (0x0))


</dt> <dd>

Faz com que essa chamada seja bloqueada até que a consulta seja concluída.

</dd> <dt>

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

Faz com que o WMI grave dados de alteração de classe junto com a definição de classe base. Para obter mais informações sobre qualificadores corrigidos, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ em, opcional\]
</dt> <dd>

Normalmente, isso é indefinido. Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação. Um provedor que dá suporte ou requer essas informações deve documentar os nomes de valores reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.

</dd> <dt>

*objWbemAsyncContext* \[ em, opcional\]
</dt> <dd>

Esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que retorna ao coletor de objeto para identificar a origem da chamada assíncrona original. Use esse parâmetro se você estiver fazendo várias chamadas assíncronas usando o mesmo coletor de objetos. Para usar esse parâmetro, crie um objeto **SWbemNamedValueSet** e use o método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo. Esse objeto **SWbemNamedValueSet** é retornado para o coletor de objeto e a origem da chamada pode ser extraída usando o método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) . Para obter mais informações, consulte [chamando um método](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor. Se a chamada for bem-sucedida, o evento [**OnObjectPut**](swbemsink-onobjectput.md) do coletor de objeto fornecido receberá um objeto [**SWbemObjectPath**](swbemobjectpath.md) , contendo o caminho do objeto da instância ou classe que está confirmada com êxito no WMI.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **PutAsync \_** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

O usuário atual não tem permissão para atualizar uma instância da classe especificada.

</dd> <dt>

**wbemErrAlreadyExists** -2147749913 (0x80041019)
</dt> <dd>

O sinalizador **wbemChangeFlagCreateOnly** foi especificado, mas a instância já existe.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrIllegalNull** -2147749898 (0x8004100A)
</dt> <dd>

Um valor de **nada** foi especificado para uma propriedade que pode não ser **nada**. Um exemplo de tal propriedade é um que é marcado por um qualificador de **chave**, **indexado** ou **não \_ nulo** .

</dd> <dt>

**wbemErrInvalidObject** -2147749908 (0x80041014)
</dt> <dd>

A instância especificada é inválida.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Um parâmetro especificado não é válido.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

O sinalizador **wbemChangeFlagUpdateOnly** foi especificado, mas a instância ou classe não existe.

</dd> <dt>

**wbemErrIncompleteClass** -2147749920 (0x80041020)
</dt> <dd>

As propriedades obrigatórias para classes não foram definidas.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa chamada retorna imediatamente, e o resultado da operação **Put** é retornado para o chamador por meio de retornos de chamada entregues ao coletor especificado em *objWbemSink*. Implemente o *objWbemSink*. Método [**OnObjectPut**](swbemsink-onobjectput.md) para obter o caminho do objeto da instância ou da classe que é gravada no repositório WMI. Para obter mais informações sobre métodos de coletor, consulte [chamando um método](calling-a-method.md).

Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor. Isso representa riscos de segurança para seus scripts e aplicativos. Para eliminar os riscos, use semisynchronous ou comunicação síncrona. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

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

[**SWbemObjectPath. Class**](swbemobjectpath-class.md)
</dt> <dt>

[**SWbemProperty**](swbemproperty.md)
</dt> <dt>

[**SWbemQualifier**](swbemqualifier.md)
</dt> </dl>

 

