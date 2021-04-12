---
title: Mensagem de MCM_SETCALENDARBORDER (commctrl. h)
description: Define o tamanho da borda, em pixels. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ SetCalendarBorder.
ms.assetid: 2a64a08f-a1fb-47a8-8f09-725807e87a03
keywords:
- Controles de MCM_SETCALENDARBORDER de mensagens do Windows
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
ms.openlocfilehash: 09b870346e8d8b475833657dd83141ba1fe11715
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455116"
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

## <a name="return-value"></a>Retornar valor

Não usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





