---
description: O evento OnCompleted de um objeto SWbemSink é disparado quando uma chamada assíncrona é concluída. Esse evento indica ao aplicativo cliente, o resultado de uma operação assíncrona e fornece informações de erro quando a chamada assíncrona falha.
ms.assetid: 2723185d-5b8b-4cc7-ada3-51c3275272a9
ms.tgt_platform: multiple
title: 'Evento ISWbemSinkEvents:: OnCompleted (Wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnCompleted
- ISWbemSinkEvents.OnCompleted
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 16cb0362b5c1b1d432d72bb959103adbb7315069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091279"
---
# <a name="iswbemsinkeventsoncompleted-event"></a>Evento ISWbemSinkEvents:: OnCompleted

O evento **OnCompleted** de um objeto [**SWbemSink**](swbemsink.md) é disparado quando uma chamada assíncrona é concluída. Esse evento indica ao aplicativo cliente, o resultado de uma operação assíncrona e fornece informações de erro quando a chamada assíncrona falha.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
SWbemSink.OnCompleted( _
  ByVal iHResult, _
  ByVal objWbemErrorObject, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iHResult* 
</dt> <dd>

O HRESULT do método assíncrono concluído. O HRESULT é o mesmo que o valor retornado de uma [API com equivalente para chamada de método WMI](com-api-for-wmi.md) . Verifique esse valor para determinar se a chamada assíncrona foi bem-sucedida ou não. Se a chamada assíncrona for bem-sucedida, esse parâmetro conterá o WBEM \_ S \_ sem \_ erro (0). Se a chamada assíncrona falhar, esse parâmetro conterá um código de erro.

</dd> <dt>

*objWbemErrorObject* 
</dt> <dd>

Contém um objeto [**SWbemLastError**](swbemlasterror.md) quando o método assíncrono falha.

</dd> <dt>

*objWbemAsyncContext* 
</dt> <dd>

Esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que é passado para a chamada assíncrona original. Use esse parâmetro para identificar a origem da chamada assíncrona que dispara esse evento quando várias chamadas assíncronas são feitas usando esse coletor de objeto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do evento **OnCompleted** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro abaixo.

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

Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor. Isso representa riscos de segurança para seus scripts e aplicativos. Para eliminar os riscos, use semisynchronous ou comunicação síncrona. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

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



 

