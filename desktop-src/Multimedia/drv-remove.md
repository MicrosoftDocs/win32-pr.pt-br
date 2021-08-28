---
title: DRV_REMOVE mensagem (Mmsystem.h)
description: Notifica o driver de que ele está prestes a ser removido do sistema. Quando um driver recebe essa mensagem, ele deve remover todas as seções criadas no Registro.
ms.assetid: e4f6ce7c-29e5-4256-b08a-13571256207c
keywords:
- DRV_REMOVE mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- DRV_REMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c08302d69e934ec77908b247f3c8f6368de8de4eab36809b6102b74858adde5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496416"
---
# <a name="drv_remove-message"></a>Mensagem DRV \_ REMOVE

Notifica o driver de que ele está prestes a ser removido do sistema. Quando um driver recebe essa mensagem, ele deve remover todas as seções criadas no Registro.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*
</dt> <dd>

Identificador do driver instalável. Esse é o mesmo valor retornado anteriormente pelo driver da [**mensagem DRV \_ OPEN.**](drv-open.md)

</dd> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Lidar com a instância do driver instanciada.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Os *parâmetros lParam1* *e lParam2* não são usados.

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

 

 





