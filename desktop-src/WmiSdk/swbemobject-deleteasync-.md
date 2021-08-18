---
description: O método DeleteAsync \_ de SWbemObject exclui de forma assíncrona a classe atual ou a instância atual.
ms.assetid: b8d67fa5-5217-422b-acbe-5eea6028deeb
ms.tgt_platform: multiple
title: SWbemObject.DeleteAsync_ método (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.DeleteAsync_
- ISWbemObject.DeleteAsync_
- ISWbemObject.DeleteAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 66b5b2492b73d880f356a3d581efb6ff75d9e3d811c25283ef481bc2e592ae93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732536"
---
# <a name="swbemobjectdeleteasync_-method"></a>Método SWbemObject.DeleteAsync \_

O **método DeleteAsync \_** de [**SWbemObject**](swbemobject.md) exclui de forma assíncrona a classe atual ou a instância atual. Se um provedor dinâmico fornece a classe ou a instância, às vezes não é possível excluir esse objeto, a menos que o provedor seja compatível com a exclusão de classe ou instância.

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
SWbemObject.DeleteAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*objWbemSink* \[ Em\]
</dt> <dd>

O sink do objeto que retorna o resultado da operação de exclusão.

</dd> <dt>

*iFlags* \[ in, opcional\]
</dt> <dd>

Inteiro que determina o comportamento da chamada. Esse parâmetro pode aceitar os valores a seguir.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus*** (128 (0x80))


</dt> <dd>

Faz com que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**SWbemSink.OnProgress**](swbemsink-onprogress.md) para o sink do objeto.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus*** ( 0 (0x0))


</dt> <dd>

Impede que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o sink do objeto.

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ in, opcional\]
</dt> <dd>

Esse parâmetro normalmente é indefinido. Caso contrário, esse é [**um objeto SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação. Um provedor que dá suporte ou requer essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.

</dd> <dt>

*objWbemAsyncContext* \[ in, opcional\]
</dt> <dd>

Este é um [**objeto SWbemNamedValueSet**](swbemnamedvalueset.md) que retorna ao sink do objeto para identificar a origem da chamada assíncrona original. Use esse parâmetro se você estiver fazendo várias chamadas assíncronas usando o mesmo sink de objeto. Para usar esse parâmetro, crie um objeto **SWbemNamedValueSet** e use o método [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo. Esse **objeto SWbemNamedValueSet** é retornado ao sink do objeto e a origem da chamada pode ser extraída usando o [**método SWbemNamedValueSet.Item.**](swbemnamedvalueset-item.md) Para obter mais informações, consulte [Chamando um método](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor. Se essa chamada for bem-sucedida, o resultado da operação de exclusão será fornecido por meio do sink de objeto fornecido.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do **método \_ DeleteAsync,** o [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrAccessDenied** – 2147749891 (0x80041003)
</dt> <dd>

O contexto atual não tem direitos de segurança adequados para excluir o objeto.

</dd> <dt>

**wbemErrFailed** – 2147749890 (0x80041002)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrInvalidClass** – 2147749904 (0x80041010)
</dt> <dd>

A classe especificada não existe.

</dd> <dt>

**wbemErrInvalidOperation** – 2147749910 (0x80041016)
</dt> <dd>

O objeto não pode ser excluído.

</dd> <dt>

**wbemErrNotFound** – 2147749890 (0x80041002)
</dt> <dd>

O objeto não existia.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa chamada retorna imediatamente. O status é retornado ao chamador por meio de um retorno de chamada entregue ao sink especificado em *objWbemSink.*

Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o sink. Isso representa riscos de segurança para seus scripts e aplicativos. Para eliminar os riscos, use comunicação síncrona ou comunicação síncrona. Para obter mais informações, consulte [Chamando um método](calling-a-method.md).

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



 

