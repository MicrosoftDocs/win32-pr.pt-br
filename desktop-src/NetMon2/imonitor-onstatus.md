---
description: O método MCSVC chama o método OnStatus para notificar o monitor de que existe um evento de status NPP. Esse método deve ser implementado pelo monitor.
ms.assetid: 771852b1-77d8-4d7d-b3fb-03eb3ea593b8
title: 'Método IMonitor:: OnStatus (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStatus
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 2a82594400bebc8a529290e0e0e881603172aa45c111d2d4d83ebcbd5ebfbeb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779036"
---
# <a name="imonitoronstatus-method"></a>Método IMonitor:: OnStatus

O método MCSVC chama o método **OnStatus** para notificar o monitor de que existe um evento de status NPP. Esse método deve ser implementado pelo monitor.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnStatus(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Evento* \[ de no\]
</dt> <dd>

Uma estrutura de [ \_ eventos de atualização](update-event.md) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será S \_ OK (que é o mesmo que NOERROR) e o MCSVC passará o valor retornado de volta para o NPP para processamento.

Se o método não for bem-sucedido, retorne um código de erro. Se houver erro, o MCSVC passa o valor retornado de volta para o NPP para processamento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




