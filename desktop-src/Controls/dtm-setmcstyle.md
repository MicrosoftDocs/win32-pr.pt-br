---
title: Mensagem de DTM_SETMCSTYLE (commctrl. h)
description: Define o estilo de um controle do seletor de data e hora (DTP). Envie essa mensagem explicitamente ou usando a macro DateTime \_ SetMonthCalStyle.
ms.assetid: 6b480a1e-c76e-4026-ab2a-5ec53df6fa28
keywords:
- controles de Windows de mensagem de DTM_SETMCSTYLE
topic_type:
- apiref
api_name:
- DTM_SETMCSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2805f2213bcbb1fa91a10ea80005b8b23bbc7447973bba6930bfdcb1e52a9e91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877796"
---
# <a name="dtm_setmcstyle-message"></a>\_Mensagem DTM SETMCSTYLE

Define o estilo de um controle do seletor de data e hora (DTP). Envie essa mensagem explicitamente ou usando a macro [**DateTime \_ SetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* \[ no\]
</dt> <dd>Um valor de estilo. Para obter mais informações, consulte <a href="month-calendar-control-styles.md">estilos de controle de calendário mensal</a>.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o valor do estilo anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





