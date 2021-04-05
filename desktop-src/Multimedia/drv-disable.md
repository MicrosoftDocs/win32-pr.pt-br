---
title: Mensagem de DRV_DISABLE (mmsystem. h)
description: Desabilita o driver. O driver deve posicionar o dispositivo correspondente, se houver, em um estado inativo e encerrar quaisquer funções ou threads de retorno de chamada.
ms.assetid: 83e99397-6f0e-4174-9f96-e10c1f17ef0b
keywords:
- Multimídia do Windows de mensagem DRV_DISABLE
topic_type:
- apiref
api_name:
- DRV_DISABLE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b512e90612a02681008474c7f1323f17304422d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919149"
---
# <a name="drv_disable-message"></a>\_Mensagem de desabilitação de drv

Desabilita o driver. O driver deve posicionar o dispositivo correspondente, se houver, em um estado inativo e encerrar quaisquer funções ou threads de retorno de chamada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Identificador da instância de driver instalável.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Os parâmetros *dwDriverId*, *lParam1* e *lParam2* não são usados.

Depois de desabilitar o driver, o sistema normalmente envia o driver a uma mensagem [**drv \_ Free**](drv-free.md) antes de remover o driver da memória.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Drivers instaláveis](installable-drivers.md)
</dt> <dt>

[Mensagens de driver instaláveis](installable-driver-messages.md)
</dt> </dl>

 

 





