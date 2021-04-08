---
title: Mensagem de DTM_CLOSEMONTHCAL (commctrl. h)
description: Fecha um controle do seletor de data e hora (DTP). Envie essa mensagem explicitamente ou usando a macro DateTime \_ CloseMonthCal.
ms.assetid: f60af77f-ec34-4f3d-9427-cda7ac6083bf
keywords:
- Controles de DTM_CLOSEMONTHCAL de mensagens do Windows
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
ms.openlocfilehash: bd79f33576490196bf29fd51316f8ce3daf4ad4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008946"
---
# <a name="dtm_closemonthcal-message"></a>\_Mensagem DTM CLOSEMONTHCAL

Fecha um controle do seletor de data e hora (DTP). Envie essa mensagem explicitamente ou usando a macro [**DateTime \_ CloseMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna zero.

## <a name="remarks"></a>Comentários

Destrói o controle e envia uma notificação [DTN \_ closeup](dtn-closeup.md) de que o controle está fechando, ao contrário do controle, é aberto (descartando como na notificação [ \_ suspensa DTN](dtn-dropdown.md) ) para o pai do controle.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[\_lista suspensa DTN](dtn-dropdown.md)
</dt> <dt>

[DTN \_ closeup](dtn-closeup.md)
</dt> </dl>

 

 





