---
title: LB_GETITEMRECT mensagem (Winuser.h)
description: Obtém as dimensões do retângulo que delimita um item de caixa de listagem como ele é exibido atualmente na caixa de listagem.
ms.assetid: 84f94bc9-f7a4-4c2d-8c35-1bd291082af9
keywords:
- LB_GETITEMRECT controles Windows mensagem
topic_type:
- apiref
api_name:
- LB_GETITEMRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94e6fa6ed15f4d3a186800fd66e7c917e8620effa775c76f85b144e49207f12f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799476"
---
# <a name="lb_getitemrect-message"></a>Mensagem \_ LB GETITEMRECT

Obtém as dimensões do retângulo que delimita um item de caixa de listagem como ele é exibido atualmente na caixa de listagem.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice de base zero do item.

Windows 95/Windows 98/Windows Edition DaNium (Windows Me) : o parâmetro *wParam* é limitado a valores de 16 bits. Isso significa que as caixas de listagem não podem conter mais de 32.767 itens. Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura RECT**](/previous-versions//dd162897(v=vs.85)) que receberá as coordenadas do cliente para o item na caixa de listagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se ocorrer um erro, o valor de retorno será LB \_ ERR.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Rect**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

