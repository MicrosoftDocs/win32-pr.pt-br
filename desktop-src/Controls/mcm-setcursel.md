---
title: Mensagem de MCM_SETCURSEL (commctrl. h)
description: Define a data atualmente selecionada para um controle de calendário mensal. Se a data especificada não estiver na exibição, o controle atualizará a exibição para colocá-la no modo de exibição. Você pode enviar essa mensagem explicitamente ou usando a \_ macro Setcurseal calendário mensal.
ms.assetid: 2a9f82a1-66d9-44dd-b60f-b588b4688316
keywords:
- Controles de MCM_SETCURSEL de mensagens do Windows
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
ms.openlocfilehash: cceff48fbc4ffdb7446277d506c369e1bd89c92b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755657"
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

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro. Essa mensagem falhará se for aplicada a um controle de calendário de mês que usa o estilo de [**\_ multiseleção MCS**](month-calendar-control-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Vezes no controle de calendário mensal](month-calendar-controls.md)
</dt> </dl>

 

