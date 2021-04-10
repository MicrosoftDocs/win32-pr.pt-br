---
description: O evento OnObjectReady de um objeto SWbemSink é disparado quando uma operação assíncrona retorna um objeto.
ms.assetid: 14110ee7-a808-4786-b695-2ce54189d826
ms.tgt_platform: multiple
title: 'Evento ISWbemSinkEvents:: OnObjectReady (Wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnObjectReady
- ISWbemSinkEvents.OnObjectReady
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1fa803339e7007a030881c3d5b47d67f354b5661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091277"
---
# <a name="iswbemsinkeventsonobjectready-event"></a>Evento ISWbemSinkEvents:: OnObjectReady

O evento **OnObjectReady** de um objeto [**SWbemSink**](swbemsink.md) é disparado quando uma operação assíncrona retorna um objeto. Use esse evento para processar objetos de chamadas assíncronas, como [**SWbemObject \_ . InstancesAsync**](swbemobject-instancesasync-.md) ou [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md). **OnObjectReady** retorna um [**SWbemObject**](swbemobject.md) a cada vez até que a enumeração seja concluída.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
SWbemSink.OnObjectReady( _
  ByVal objWbemObject, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*objWbemObject* 
</dt> <dd>

Um objeto [**SWbemObject**](swbemobject.md) . Isso é semelhante ao que é retornado pelo equivalente síncrono da chamada assíncrona que dispara esse evento. Por exemplo, uma chamada para o método [**SWbemServices. getasync**](swbemservices-getasync.md) retorna um **SWbemObject** no parâmetro *objWbemObject* do evento **OnObjectReady** do objeto [**SWbemSink**](swbemsink.md) , que é passado como o parâmetro *objWbemObject* da chamada original. O mesmo objeto **SWbemObject** pode ser obtido usando uma chamada síncrona equivalente para [**SWbemServices. Get**](swbemservices-get.md).

</dd> <dt>

*objWbemAsyncContext* 
</dt> <dd>

Um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que é passado para a chamada assíncrona original. Use esse parâmetro para identificar a origem da chamada assíncrona que dispara esse evento quando várias chamadas assíncronas são feitas usando esse coletor de objeto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do evento **OnObjectReady** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro abaixo.

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

Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor. Isso representa riscos de segurança para seus scripts e aplicativos. Para eliminar os riscos, use a comunicação semi-síncrona ou a comunicação síncrona. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

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

 

