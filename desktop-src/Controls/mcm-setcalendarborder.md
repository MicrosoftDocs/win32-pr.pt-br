---
title: Mensagem de MCM_SETCALENDARBORDER (commctrl. h)
description: Define o tamanho da borda, em pixels. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ SetCalendarBorder.
ms.assetid: 2a64a08f-a1fb-47a8-8f09-725807e87a03
keywords:
- controles de Windows de mensagem de MCM_SETCALENDARBORDER
topic_type:
- apiref
api_name:
- MCM_SETCALENDARBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08e020ad282ce21555e6c3a74198a0034013ac1d7cfac8f4eb68e52137e5f684
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697196"
---
# <a name="mcm_setcalendarborder-message"></a>\_Mensagem MCM SETCALENDARBORDER

Define o tamanho da borda, em pixels. Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ SetCalendarBorder**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalendarborder) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Se for **true**, o tamanho da borda será definido como o número de pixels especificado por *lParam* . Se **for false**, o tamanho da borda será redefinido para o valor padrão especificado pelo tema ou zero se os temas não estiverem sendo usados.

</dd> <dt>

*lParam* 
</dt> <dd>

Número de pixels do tamanho da borda.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Não usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





