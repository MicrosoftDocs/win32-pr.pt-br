---
title: Mensagem de MCM_SETCURSEL (commctrl. h)
description: Define a data atualmente selecionada para um controle de calendário mensal. Se a data especificada não estiver na exibição, o controle atualizará a exibição para colocá-la no modo de exibição. Você pode enviar essa mensagem explicitamente ou usando a \_ macro Setcurseal calendário mensal.
ms.assetid: 2a9f82a1-66d9-44dd-b60f-b588b4688316
keywords:
- controles de Windows de mensagem de MCM_SETCURSEL
topic_type:
- apiref
api_name:
- MCM_SETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e63238f11f93e56c18e1897fcdd3cb96977f23fe16bde19123b5c063f99c0ff0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061886"
---
# <a name="mcm_setcursel-message"></a>\_Mensagem MCM SETcurseal

Define a data atualmente selecionada para um controle de calendário mensal. Se a data especificada não estiver na exibição, o controle atualizará a exibição para colocá-la no modo de exibição. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ setcurseal calendário mensal**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcursel) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que contém a data a ser definida como a seleção atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará zero se for bem-sucedido ou nenhum outro. Essa mensagem falhará se for aplicada a um controle de calendário de mês que usa o estilo de [**\_ multiseleção MCS**](month-calendar-control-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Vezes no controle de calendário mensal](month-calendar-controls.md)
</dt> </dl>

 

