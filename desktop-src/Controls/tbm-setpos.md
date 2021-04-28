---
title: Mensagem de TBM_SETPOS (commctrl. h)
description: TBM_SETPOS mensagem – define a posição lógica atual do controle deslizante em um TrackBar.
ms.assetid: df6c4e5d-2847-419d-82b5-334d53bb6ba1
keywords:
- Controles de TBM_SETPOS de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f10e05a677119f18489d0eb9eebc4528d3ad115
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085864"
---
# <a name="tbm_setpos-message"></a>\_Mensagem tbm SETPOS

Define a posição lógica atual do controle deslizante em um TrackBar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Sinalizador de redesenho. Se esse parâmetro for **true**, a mensagem redesenhará o controle com o controle deslizante na posição fornecida pelo *lParam*. Se esse parâmetro for **false**, a mensagem não redesenhará o controle deslizante na nova posição. Observe que a mensagem define o valor da posição do controle deslizante (como retornado pela mensagem [**tbm \_ GETPOS**](tbm-getpos.md) ), independentemente do parâmetro *wParam* .

</dd> <dt>

*lParam* 
</dt> <dd>

Nova posição lógica do controle deslizante. As posições lógicas válidas são os valores inteiros no intervalo de TrackBar de mínimo para o máximo de posições do controle deslizante. Se esse valor estiver fora do intervalo máximo e mínimo do controle, a posição será definida como o valor máximo ou mínimo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





