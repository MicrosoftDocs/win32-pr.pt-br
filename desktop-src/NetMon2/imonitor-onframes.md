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
ms.openlocfilehash: a4138c35384753c8df79728a61decf78bf302d0dc9c0a71ca9f787d76a70a620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779166"
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

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será S \_ OK (que é o mesmo que NOERROR). O MCSVC passa o valor retornado de volta para o NPP para processamento.

Se o método não for bem-sucedido, o valor de retorno será um código de erro. O MCSVC passa o valor retornado de volta para o NPP para processamento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




