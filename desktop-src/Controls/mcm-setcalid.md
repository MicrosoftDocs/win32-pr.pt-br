---
title: Mensagem de MCM_SETCALID (commctrl. h)
description: Define a ID do calendário para o controle de calendário fornecido. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ SetCALID.
ms.assetid: 4b9d06f5-0784-4a17-b401-982206d4be67
keywords:
- Controles de MCM_SETCALID de mensagens do Windows
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
ms.openlocfilehash: a661a685062fe737a1927c3a6ab455e8499c6ca9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009001"
---
# <a name="mcm_setcalid-message"></a>\_Mensagem MCM SETCALID

Define a ID do calendário para o controle de calendário fornecido. Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ SetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalid) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A ID do calendário. Uma das constantes de [identificadores de calendário](/windows/desktop/Intl/calendar-identifiers) .

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Não utilizado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

