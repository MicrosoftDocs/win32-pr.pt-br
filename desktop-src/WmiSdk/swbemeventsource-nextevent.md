---
description: Se um evento estiver disponível, o método NextEvent do objeto SWbemEventSource recuperará o evento de uma consulta de evento.
ms.assetid: ff2d54d4-b8ee-4bb8-b6f7-081a1ca20489
ms.tgt_platform: multiple
title: Método SWbemEventSource.NextEvent (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemEventSource.NextEvent
- ISWbemEventSource.NextEvent
- ISWbemEventSource.NextEvent
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6ce39d442b48f32c2aafcd6e24c1c214dce82a19435b6b36bce65d5426161859
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050064"
---
# <a name="swbemeventsourcenextevent-method"></a>Método SWbemEventSource.NextEvent

Se um evento estiver disponível, o **método NextEvent** do objeto [**SWbemEventSource**](swbemeventsource.md) recuperará o evento de uma consulta de evento.

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objWbemObject = .NextEvent( _
  [ ByVal iTimeoutMs ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iTimeoutMs* \[ in, opcional\]
</dt> <dd>

Número de milissegundos que a chamada aguarda um evento antes de retornar um erro de tempo-out. O valor padrão para esse parâmetro é **wbemTimeoutInfinite** (-1), que direciona a chamada para aguardar indefinidamente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o **método NextEvent** for bem-sucedido, ele retornará um [**objeto SWbemObject**](swbemobject.md) que contém o evento solicitado. Se a chamada aumentar, o objeto retornado será **NULL** e um erro será gerado.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do **método NextEvent,** o **objeto Err** pode conter o código de erro na lista a seguir.

<dl> <dt>

**wbemErrTimedOut** – 0x80043001
</dt> <dd>

O evento solicitado não chegou na quantidade de tempo especificada em *iTimeoutMs.*

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemEventSource<br/>                                                      |
| IID<br/>                      | IID \_ ISWbemEventSource<br/>                                                       |



 

 




