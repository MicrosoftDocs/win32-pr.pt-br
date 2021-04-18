---
description: Se um evento estiver disponível, o método NextEvent do objeto SWbemEventSource recuperará o evento de uma consulta de evento.
ms.assetid: ff2d54d4-b8ee-4bb8-b6f7-081a1ca20489
ms.tgt_platform: multiple
title: Método SWbemEventSource. NextEvent (Wbemdisp. h)
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
ms.openlocfilehash: 02fbc32557ab29c66849a4249d26cc2ca41564e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764439"
---
# <a name="swbemeventsourcenextevent-method"></a>Método SWbemEventSource. NextEvent

Se um evento estiver disponível, o método **NextEvent** do objeto [**SWbemEventSource**](swbemeventsource.md) recuperará o evento de uma consulta de evento.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objWbemObject = .NextEvent( _
  [ ByVal iTimeoutMs ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iTimeoutMs* \[ em, opcional\]
</dt> <dd>

Número de milissegundos durante os quais a chamada aguarda um evento antes de retornar um erro de tempo limite. O valor padrão para esse parâmetro é **wbemTimeoutInfinite** (-1), que direciona a chamada para aguardar indefinidamente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método **NextEvent** for bem-sucedido, ele retornará um objeto [**SWbemObject**](swbemobject.md) que contém o evento solicitado. Se a chamada atingir o tempo limite, o objeto retornado será **nulo** e um erro será gerado.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **NextEvent** , o objeto **Err** pode conter o código de erro na lista a seguir.

<dl> <dt>

**wbemErrTimedOut** -0x80043001
</dt> <dd>

O evento solicitado não chegou no período de tempo especificado em *iTimeoutMs.*

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMEVENTSOURCE CLSID<br/>                                                      |
| IID<br/>                      | ISWbemEventSource de IID \_<br/>                                                       |



 

 




