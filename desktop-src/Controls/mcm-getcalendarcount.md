---
title: Mensagem de MCM_GETCALENDARCOUNT (commctrl. h)
description: Obtém o número de calendários atualmente exibidos no controle de calendário. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ GetCalendarCount.
ms.assetid: b9463f02-d37b-49b0-8387-0938020c23ee
keywords:
- controles de Windows de mensagem de MCM_GETCALENDARCOUNT
topic_type:
- apiref
api_name:
- MCM_GETCALENDARCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9379aa8c273451ba53c2a13d6190712212765b46dc1052a08b6d03ae4ae32e61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019044"
---
# <a name="mcm_getcalendarcount-message"></a>\_Mensagem MCM GETCALENDARCOUNT

Obtém o número de calendários atualmente exibidos no controle de calendário. Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ GetCalendarCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalendarcount) .

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

Número de calendários atualmente exibidos no controle de calendário. O número máximo de calendários permitidos é 12.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





