---
title: DTM_GETMCFONT mensagem (Commctrl.h)
description: Obtém a fonte que o controle de calendário de mês filho do DTP (selador de data e hora) está usando no momento. Você pode enviar essa mensagem explicitamente ou usar a \_ macro DateTime GetMonthCalFont.
ms.assetid: 6687a1dc-6f6d-4684-80b2-f726b08d2f3a
keywords:
- DTM_GETMCFONT controles Windows mensagem
topic_type:
- apiref
api_name:
- DTM_GETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2bf60f226e7fe5d309324bc517a7fd215abe4591fd5141ff149b14e162ac9be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878126"
---
# <a name="dtm_getmcfont-message"></a>Mensagem \_ GETMCFONT DTM

Obtém a fonte que o controle de calendário de mês filho do DTP (selador de data e hora) está usando no momento. Você pode enviar essa mensagem explicitamente ou usar a macro [**\_ DateTime GetMonthCalFont.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor HFONT que é o alçador para a fonte atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





