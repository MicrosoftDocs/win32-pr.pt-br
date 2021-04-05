---
title: Mensagem de MCM_GETCALID (commctrl. h)
description: Obtém a ID do calendário para o controle de calendário fornecido. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ GetCALID.
ms.assetid: ecfab4f3-a5af-445d-8b90-243b646524a6
keywords:
- Controles de MCM_GETCALID de mensagens do Windows
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
ms.openlocfilehash: cb4a780d5107a7761d7dcac9b27a7cb01f3de744
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085675"
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

## <a name="return-value"></a>Retornar valor

ID do calendário atual. Uma das constantes de [identificadores de calendário](/windows/desktop/Intl/calendar-identifiers) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

