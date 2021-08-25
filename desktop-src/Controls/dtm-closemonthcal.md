---
title: DTM_CLOSEMONTHCAL mensagem (Commctrl.h)
description: Fecha um controle DTP (selador de data e hora). Envie essa mensagem explicitamente ou usando a macro DateTime \_ CloseMonthCal.
ms.assetid: f60af77f-ec34-4f3d-9427-cda7ac6083bf
keywords:
- DTM_CLOSEMONTHCAL controles Windows mensagem
topic_type:
- apiref
api_name:
- DTM_CLOSEMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f458592d2842625b9826eda5963c66cbd182e3f052a2b2a70ff5219a054e8cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878236"
---
# <a name="dtm_closemonthcal-message"></a>Mensagem DTM \_ CLOSEMONTHCAL

Fecha um controle DTP (selador de data e hora). Envie essa mensagem explicitamente ou usando a [**macro DateTime \_ CloseMonthCal.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna zero.

## <a name="remarks"></a>Comentários

Destrói o controle e envia uma notificação [ \_ CLOSEUP de DTN](dtn-closeup.md) de que o controle está sendo fechado em vez de o controle estar sendo aberto (soltando como na notificação [DE \_ DROPDOWN de DTN)](dtn-dropdown.md) para o pai do controle.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[LISTA DE \_ DTN](dtn-dropdown.md)
</dt> <dt>

[CLOSEUP de \_ DTN](dtn-closeup.md)
</dt> </dl>

 

 





