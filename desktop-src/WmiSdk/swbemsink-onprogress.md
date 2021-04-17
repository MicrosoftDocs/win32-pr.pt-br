---
description: O evento OnProgress de SWbemSink é disparado quando uma chamada assíncrona retorna o status de uma chamada em andamento.
ms.assetid: abb43916-f952-41fe-a5ba-0428864c0685
ms.tgt_platform: multiple
title: 'Evento ISWbemSinkEvents:: OnProgress (Wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnProgress
- ISWbemSinkEvents.OnProgress
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0d322309adcfad33b1c303d7efd6af28db1cac80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787656"
---
# <a name="iswbemsinkeventsonprogress-event"></a>Evento ISWbemSinkEvents:: OnProgress

O evento **OnProgress** de [**SWbemSink**](swbemsink.md) é disparado quando uma chamada assíncrona retorna o status de uma chamada em andamento. Se os eventos, instâncias ou classes forem produzidos de um provedor que dá suporte a atualizações de status, você poderá posicionar o código nesse evento para fornecer aos usuários comentários sobre o status de uma operação assíncrona. Você deve definir o parâmetro *iFlags* da chamada assíncrona para **wbemFlagSendStatus** (128/0x80) se quiser receber atualizações de status, caso contrário, esse evento não será disparado.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
SWbemSink.OnProgress( _
  ByVal iUpperBound, _
  ByVal iCurrent, _
  ByVal strMessage, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iUpperBound* 
</dt> <dd>

Inteiro que descreve o número total de tarefas a serem concluídas.

</dd> <dt>

*iCurrent* 
</dt> <dd>

Item atual que está sendo processado.

</dd> <dt>

*strMessage* 
</dt> <dd>

Mensagem que descreve o status da tarefa atual.

</dd> <dt>

*objWbemAsyncContext* 
</dt> <dd>

Um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que é passado para a chamada assíncrona original. Use esse parâmetro para identificar a origem da chamada assíncrona que dispara esse evento quando várias chamadas assíncronas são feitas usando esse coletor de objeto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do evento **OnProgress** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro abaixo.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> <dt>

**wbemErrTransportFailure** -2147749909 (0x80041015)
</dt> <dd>

Ocorreu um erro de rede, impedindo a operação normal.

</dd> </dl>

## <a name="remarks"></a>Comentários

O evento **OnProgress** é disparado quando uma chamada assíncrona retorna o status de uma chamada em andamento. Se os eventos, instâncias ou classes forem produzidos de um provedor que dá suporte a atualizações de status, você poderá colocar o código nesse evento para fornecer comentários aos usuários sobre o status de uma operação assíncrona.

> [!Note]  
> Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor. Isso representa riscos de segurança para seus scripts e aplicativos. Para eliminar os riscos, use a comunicação semi-síncrona ou síncrona. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Wbemdisp. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMSINK CLSID<br/>                                                             |
| IID<br/>                      | ISWbemSinkEvents de IID \_<br/>                                                        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemSink**](swbemsink.md)
</dt> </dl>

 

