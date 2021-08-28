---
title: Mensagem de MCM_GETCALID (commctrl. h)
description: Obtém a ID do calendário para o controle de calendário fornecido. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ GetCALID.
ms.assetid: ecfab4f3-a5af-445d-8b90-243b646524a6
keywords:
- controles de Windows de mensagem de MCM_GETCALID
topic_type:
- apiref
api_name:
- MCM_GETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 148db880fe941c3b7df045c0ecdd4fbc9303203eace2b3be3ab38831aa4e3644
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170183"
---
# <a name="mcm_getcalid-message"></a>\_Mensagem MCM GETCALID

Obtém a ID do calendário para o controle de calendário fornecido. Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ GetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalid) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

ID do calendário atual. Uma das constantes de [identificadores de calendário](/windows/desktop/Intl/calendar-identifiers) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

