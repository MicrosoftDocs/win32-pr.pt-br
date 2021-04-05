---
description: O método onframes deve ser implementado pelo monitor. O MCSVC chama esse método quando o buffer de captura está cheio ou o tempo de atualização passou.
ms.assetid: 243bd35b-2527-463e-b3d2-4bd840fe9c3f
title: 'Método IMonitor:: onframes (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnFrames
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: c5b6ff3e9d5b97a228e6e1d865fe4d8f1b5bfc9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647046"
---
# <a name="imonitoronframes-method"></a>Método IMonitor:: onframes

O método **Onframes** deve ser implementado pelo monitor. O MCSVC chama esse método quando o buffer de captura está cheio ou o tempo de atualização passou.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnFrames(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Evento* \[ de no\]
</dt> <dd>

[Atualizar \_ o ](update-event.md) Estrutura de eventos que contém informações de quadro usadas para atualizar eventos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem-sucedido, o valor de retorno será S \_ OK (que é o mesmo que NOERROR). O MCSVC passa o valor retornado de volta para o NPP para processamento.

Se o método não for bem-sucedido, o valor de retorno será um código de erro. O MCSVC passa o valor retornado de volta para o NPP para processamento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




