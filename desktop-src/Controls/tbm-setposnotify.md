---
title: TBM_SETPOSNOTIFY mensagem (Commctrl.h)
description: TBM_SETPOSNOTIFY mensagem - define a posição lógica atual do controle deslizante em uma barra de faixa.
ms.assetid: 02f8899a-55b0-46ae-8642-9e534ab4abf5
keywords:
- TBM_SETPOSNOTIFY controles Windows mensagem
topic_type:
- apiref
api_name:
- TBM_SETPOSNOTIFY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 677ab818524614f89d16ae851376d8776a4ccca3ef7798d4ac90aa6d36962ca2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046076"
---
# <a name="tbm_setposnotify-message"></a>Mensagem TBM \_ SETPOSNOTIFY

Define a posição lógica atual do controle deslizante em uma barra de faixa.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

wParam não éusado.

</dd> <dt>

*lParam* 
</dt> <dd>

Nova posição lógica do controle deslizante. As posições lógicas válidas são os valores inteiros no intervalo da barra de faixa de posições mínimas a máximas do controle deslizante. Se esse valor estiver fora do intervalo máximo e mínimo do controle, a posição será definida como o valor máximo ou mínimo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Chamar **TBM \_ SETPOSNOTIFY** definirá o local do controle deslizante da barra de faixa, como [**faria TBM \_ SETPOS,**](tbm-setpos.md) mas também fará com que a barra de faixa notifique seu pai de uma movimentação por meio de uma mensagem [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL.**](wm-vscroll.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





