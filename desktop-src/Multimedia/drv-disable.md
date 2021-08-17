---
title: DRV_DISABLE mensagem (Mmsystem.h)
description: Desabilita o driver. O driver deve colocar o dispositivo correspondente, se algum, em um estado inativo e encerrar quaisquer funções ou threads de retorno de chamada.
ms.assetid: 83e99397-6f0e-4174-9f96-e10c1f17ef0b
keywords:
- DRV_DISABLE mensagem Windows Multimídia
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
ms.openlocfilehash: 75d9c5a99414f0b755efbae005365d89665a2b2bc5a4673436101066ec740564
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144409"
---
# <a name="drv_disable-message"></a>Mensagem DRV \_ DISABLE

Desabilita o driver. O driver deve colocar o dispositivo correspondente, se algum, em um estado inativo e encerrar quaisquer funções ou threads de retorno de chamada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Lidar com a instância do driver instanciada.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Os *parâmetros dwDriverId,* *lParam1* e *lParam2* não são usados.

Depois de desabilitar o driver, o sistema normalmente envia ao driver uma mensagem [**DRV \_ FREE**](drv-free.md) antes de remover o driver da memória.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Drivers instaláveis](installable-drivers.md)
</dt> <dt>

[Mensagens de driver instaláveis](installable-driver-messages.md)
</dt> </dl>

 

 





