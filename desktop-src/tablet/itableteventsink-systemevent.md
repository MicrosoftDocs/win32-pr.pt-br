---
description: Ocorre quando um evento do sistema está disponível.
ms.assetid: 3d9e98f0-b11e-4a65-a544-9e1998a80d5f
title: 'Método ITabletEventSink:: SystemEvent'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.SystemEvent
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 71b5882fd9e19df43581e00cce55c2af5faa432b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751575"
---
# <a name="itableteventsinksystemevent-method"></a>Método ITabletEventSink:: SystemEvent

Ocorre quando um evento do sistema está disponível.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SystemEvent(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] SYSTEM_EVENT      event,
  [in] SYSTEM_EVENT_DATA eventdata
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TCID* \[ no\]
</dt> <dd>

O identificador do Tablet.

</dd> <dt>

*CID* \[ em\]
</dt> <dd>

O identificador da caneta.

</dd> <dt>

*evento* \[ de no\]
</dt> <dd>

O código do evento do sistema.

</dd> <dt>

*EVENTDATA* \[ no\]
</dt> <dd>

Os dados de evento do sistema.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                       |
| <dl> <dt>**E \_ falha**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="remarks"></a>Comentários

A lista a seguir contém os valores válidos para o parâmetro de evento.

-   \_toque em
-   \_toque duplo \_ se
-   toque com o \_ botão direito \_
-   \_arrastar para
-   arrastar para a \_ direita \_
-   \_ \_ Inserir
-   \_deixar de manter \_
-   \_inserir em foco \_ Enter
-   \_sair do foco de se \_
-   \_clique no meio \_
-   \_chave se
-   \_chave do modificador se \_
-   \_modo de gesto de se \_
-   \_cursor se

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 




