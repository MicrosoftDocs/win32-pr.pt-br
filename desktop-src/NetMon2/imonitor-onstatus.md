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
ms.openlocfilehash: fc2716a10673cc1178591b14a335b1d8559aa35a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090927"
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

## <a name="return-value"></a>Retornar valor

Se o método for bem-sucedido, o valor de retorno será S \_ OK (que é o mesmo que NOERROR) e o MCSVC passará o valor retornado de volta para o NPP para processamento.

Se o método não for bem-sucedido, retorne um código de erro. Se houver erro, o MCSVC passa o valor retornado de volta para o NPP para processamento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




