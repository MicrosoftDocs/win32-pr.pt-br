---
title: RB_GETRECT mensagem (Commctrl.h)
description: Recupera o retângulo delimitado para uma determinada faixa em um controle de barra rebar.
ms.assetid: e272b090-1e4d-4cff-87f0-557ad8116e7e
keywords:
- RB_GETRECT controles Windows mensagem
topic_type:
- apiref
api_name:
- RB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d2f085fa7c6f413700156999f1325879f91affc2c8984fb33d08cb6cc90b66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169292"
---
# <a name="rb_getrect-message"></a>Mensagem \_ GETRECT do RB

Recupera o retângulo delimitado para uma determinada faixa em um controle de barra rebar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice baseado em zero de uma banda no controle de barra de rebar.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura RECT**](/previous-versions//dd162897(v=vs.85)) que receberá os limites da faixa de barra de rebar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará diferente de zero se for bem-sucedido ou zero caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

