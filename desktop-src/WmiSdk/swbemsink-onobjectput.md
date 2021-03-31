---
description: O evento OnObjectPut de um objeto SWbemSink é disparado quando uma operação Put assíncrona é concluída. Esse evento retorna o caminho do objeto da instância ou da classe salva.
ms.assetid: 2046dd03-ac2c-49fa-b1ad-a458967709e5
ms.tgt_platform: multiple
title: 'Evento ISWbemSinkEvents:: OnObjectPut (Wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnObjectPut
- ISWbemSinkEvents.OnObjectPut
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c6ed42105efe407558d80cd108e657e396e88763
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171968"
---
# <a name="iswbemsinkeventsonobjectput-event"></a>Evento ISWbemSinkEvents:: OnObjectPut

O evento **OnObjectPut** de um objeto [**SWbemSink**](swbemsink.md) é disparado quando uma operação Put assíncrona é concluída. Esse evento retorna o caminho do objeto da instância ou da classe salva.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
SWbemSink.OnObjectPut( _
  ByVal objWbemObjectPath, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*objWbemObjectPath* 
</dt> <dd>

Um objeto [**SWbemObjectPath**](swbemobjectpath.md) , que contém o caminho do objeto da instância ou classe que a operação Put grava no WMI.

</dd> <dt>

*objWbemAsyncContext* 
</dt> <dd>

Um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que é passado para a chamada assíncrona original. Use esse parâmetro para identificar a origem da chamada assíncrona que dispara esse evento quando várias chamadas assíncronas são feitas usando esse coletor de objeto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do evento **OnObjectPut** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro abaixo.

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

> [!Note]  
> Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor. Isso representa riscos de segurança para seus scripts e aplicativos. Para eliminar os riscos, use a comunicação semi-síncrona ou a comunicação síncrona. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

 

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

 

