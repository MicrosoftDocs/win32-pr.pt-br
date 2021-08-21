---
title: MCM_SETCALID mensagem (Commctrl.h)
description: Define a ID do calendário para o controle de calendário determinado. Você pode enviar essa mensagem explicitamente ou usando a \_ macro MonthCal SetCALID.
ms.assetid: 4b9d06f5-0784-4a17-b401-982206d4be67
keywords:
- MCM_SETCALID controles Windows mensagem
topic_type:
- apiref
api_name:
- MCM_SETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40e7f4577382aa0e003165e38e4557b8dc234592f747a579e5a071ce2440a37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575576"
---
# <a name="mcm_setcalid-message"></a>Mensagem MCM \_ SETCALID

Define a ID do calendário para o controle de calendário determinado. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ MonthCal SetCALID.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalid)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A ID do calendário. Uma das [constantes de Identificadores de](/windows/desktop/Intl/calendar-identifiers) Calendário.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Não utilizado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

