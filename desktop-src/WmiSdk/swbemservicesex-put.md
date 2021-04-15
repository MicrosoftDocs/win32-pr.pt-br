---
description: Retorna um objeto SWbemObjectPath que contém o caminho do objeto para o qual os dados foram gravados.
ms.assetid: 1a9a718d-875d-4102-9d9d-3d10be162f58
ms.tgt_platform: multiple
title: Método SWbemServicesEx. put (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx.Put
- ISWbemServicesEx.Put
- ISWbemServicesEx.Put
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e495a38262e6b6f7dd8b67424b74db74c025be62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761543"
---
# <a name="swbemservicesexput-method"></a>Método SWbemServicesEx. put

O método **Put** do objeto [**SWbemServicesEx**](swbemservicesex.md) salva o objeto no namespace associado ao objeto e retorna um objeto [**SWbemObjectPath**](swbemobjectpath.md) que contém o caminho do objeto no qual os dados foram gravados.

Esse método é chamado no modo semisynchronous. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objObjectPath = .Put( _
  ByVal objWbemObject, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*objWbemObject* 
</dt> <dd>

Obrigatórios. O novo objeto a ser colocado no namespace. Pode ser um objeto criado recentemente ou um objeto modificado.

</dd> <dt>

*iFlags* \[ adicional\]
</dt> <dd>

Esse parâmetro determina se a chamada cria ou atualiza o objeto e se a chamada retorna imediatamente. Esse parâmetro pode aceitar os valores a seguir.

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>**wbemChangeFlagUpdateCompatible** (0 (0x0))


</dt> <dd>

Permite que uma classe seja atualizada se não houver classes derivadas e não houver nenhuma instância para essa classe. Ele também permitirá atualizações em todos os casos se a alteração for apenas para qualificadores não importantes (por exemplo, o qualificador de **Descrição** ). Esse é o comportamento padrão para essa chamada e é usado para compatibilidade com as versões anteriores do WMI. Se a classe tiver instâncias, a atualização falhará.

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>**wbemChangeFlagUpdateSafeMode** (32 (0x20))


</dt> <dd>

Permite atualizações de classes, mesmo se houver classes filhas, quando a alteração não causar conflitos com classes filhas. Você pode usar esse sinalizador ao adicionar uma nova propriedade a uma classe base que não foi mencionada anteriormente em nenhuma das classes filhas. Se a classe tiver instâncias, a atualização falhará.

</dd> <dt>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span id="wbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>**wbemChangeFlagUpdateForceMode** (64 (0x40))


</dt> <dd>

Esse sinalizador força as atualizações de classes quando existem classes filhas conflitantes. Por exemplo, esse sinalizador força uma atualização se um qualificador de classe foi definido em uma classe filho e a classe base tenta adicionar o mesmo qualificador em conflito com o existente. No modo de força, esse conflito é resolvido com a exclusão do qualificador conflitante na classe filho. Se a classe tiver instâncias, a atualização falhará.

O uso do modo Force para atualizar uma classe estática causa a exclusão de todas as instâncias dessa classe. Uma atualização forçada em uma classe de provedor não exclui instâncias da classe.

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>**wbemChangeFlagCreateOrUpdate** (0 (0x0))


</dt> <dd>

Faz com que a classe ou instância seja criada se não existir, ou substituída, se já existir.

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>**wbemChangeFlagCreateOnly** (2 (0x2))


</dt> <dd>

Usado somente para criação. A chamada falhará se a classe ou instância já existir.

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>**wbemChangeFlagUpdateOnly** (1 (0x1))


</dt> <dd>

Faz com que essa chamada faça apenas uma atualização. A classe ou instância deve existir para que a chamada seja bem-sucedida.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>**wbemFlagReturnImmediately** (16 (0x10))


</dt> <dd>

Faz com que a chamada retorne imediatamente.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>**wbemFlagReturnWhenComplete** (0 (0x0))


</dt> <dd>

Faz com que essa chamada seja bloqueada até que a operação seja concluída. Esse sinalizador chama o método no modo síncrono.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>**wbemFlagUseAmendedQualifiers** (131072 (0x20000))


</dt> <dd>

Faz com que o WMI grave dados de emenda de classe, bem como a definição de classe base. Para obter mais informações, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ adicional\]
</dt> <dd>

Normalmente, isso é indefinido. Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que presta a solicitação. Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a chamada for bem-sucedida, um objeto [**SWbemObjectPath**](swbemobjectpath.md) será retornado. Este objeto contém o caminho do objeto da instância ou classe que foi confirmada com êxito no WMI.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **Put** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

O usuário atual não tem a permissão para a operação.

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

Um valor **NULL** foi especificado para uma propriedade que não pode ser **nula**. Um exemplo de tal propriedade é um marcado por um qualificador de [**chave**](standard-qualifiers.md), **indexado** ou **não \_ nulo** .

</dd> <dt>

**wbemErrInvalidObject** -2147749908 (0x80041014)
</dt> <dd>

O objeto especificado não é válido.

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

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_ISWBEMSERVICESEX CLSID<br/>                                                      |
| IID<br/>                      | ISWbemServicesEx de IID \_<br/>                                                        |



 

 




