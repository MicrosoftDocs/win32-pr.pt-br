---
description: O método SendNMEvent envia eventos para Instrumentação de Gerenciamento do Windows (WMI).
ms.assetid: 85c33a71-72aa-4b0a-8e8b-3a220a080bb2
title: 'Método IMonitorEventer:: SendNMEvent (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.SendNMEvent
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 3286fca4d5b852d4562c13446699c1a6b40f3efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754316"
---
# <a name="imonitoreventersendnmevent-method"></a>Método IMonitorEventer:: SendNMEvent

O método **SendNMEvent** envia eventos para instrumentação de gerenciamento do Windows (WMI).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SendNMEvent(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pNMEventData* \[ no\]
</dt> <dd>

Ponteiro para o evento enviado ao WMI.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem-sucedido, o valor de retorno será S \_ OK.

Se o método não for bem-sucedido, o valor de retorno será NMERR \_ memória insuficiente \_ \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




