---
description: A \_ operação WPD \_ declara valores de enumeração que descrevem o estado atual de uma operação em andamento.
ms.assetid: a002f735-e385-4c7c-b734-e70a9c6842ca
title: Enumeração de WPD_OPERATION_STATES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_OPERATION_STATES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3c2bc25fdbc040bd849d60f1e16e5d86d1916ced17eb6670ceb3bc6a75108772
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118696479"
---
# <a name="wpd_operation_states-enumeration"></a>Enumeração de Estados de \_ operação WPD \_

A **\_ operação WPD \_ declara** valores de enumeração que descrevem o estado atual de uma operação em andamento.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWPD_OPERATION_STATES { 
  WPD_OPERATION_STATE_UNSPECIFIED  = 0,
  WPD_OPERATION_STATE_STARTED      = 1,
  WPD_OPERATION_STATE_RUNNING      = 2,
  WPD_OPERATION_STATE_PAUSED       = 3,
  WPD_OPERATION_STATE_CANCELLED    = 4,
  WPD_OPERATION_STATE_FINISHED     = 5,
  WPD_OPERATION_STATE_ABORTED      = 6
} WPD_OPERATION_STATES;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_OPERATION_STATE_UNSPECIFIED"></span><span id="wpd_operation_state_unspecified"></span>**\_estado da operação WPD \_ \_ não especificado**
</dt> <dd>

A operação atual está em um estado não especificado (não definido) e desconhecido.

</dd> <dt>

<span id="WPD_OPERATION_STATE_STARTED"></span><span id="wpd_operation_state_started"></span>**\_estado da operação WPD \_ \_ iniciado**
</dt> <dd>

A operação foi iniciada.

</dd> <dt>

<span id="WPD_OPERATION_STATE_RUNNING"></span><span id="wpd_operation_state_running"></span>**\_estado da operação WPD \_ \_ em execução**
</dt> <dd>

A operação está em execução.

</dd> <dt>

<span id="WPD_OPERATION_STATE_PAUSED"></span><span id="wpd_operation_state_paused"></span>**\_estado de operação WPD \_ \_ pausado**
</dt> <dd>

A operação está em pausa.

</dd> <dt>

<span id="WPD_OPERATION_STATE_CANCELLED"></span><span id="wpd_operation_state_cancelled"></span>**\_estado da operação WPD \_ \_ cancelado**
</dt> <dd>

A operação foi cancelada.

</dd> <dt>

<span id="WPD_OPERATION_STATE_FINISHED"></span><span id="wpd_operation_state_finished"></span>**\_estado da operação WPD \_ \_ concluído**
</dt> <dd>

A operação foi concluída.

</dd> <dt>

<span id="WPD_OPERATION_STATE_ABORTED"></span><span id="wpd_operation_state_aborted"></span>**\_estado da operação WPD \_ \_ anulado**
</dt> <dd>

A operação foi anulada.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esses valores são recebidos no retorno de chamada definido pelo aplicativo ([**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




