---
title: LB_SETHORIZONTALEXTENT mensagem (Winuser.h)
description: Define a largura, em pixels, pela qual uma caixa de listagem pode ser rolada horizontalmente (a largura rolável).
ms.assetid: 7d59b6de-2a22-4246-936b-4c669d285392
keywords:
- LB_SETHORIZONTALEXTENT controles de Windows mensagem
topic_type:
- apiref
api_name:
- LB_SETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce248354b853dd3be15e76646958ed25068648182970d748da35fb5c596ca49e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119433875"
---
# <a name="lb_sethorizontalextent-message"></a>Mensagem \_ LBORIZONTALEXTENT

Define a largura, em pixels, pela qual uma caixa de listagem pode ser rolada horizontalmente (a largura rolável). Se a largura da caixa de listagem for menor que esse valor, a barra de rolagem horizontal rolará os itens horizontalmente na caixa de listagem. Se a largura da caixa de listagem for igual ou maior que esse valor, a barra de rolagem horizontal será oculta.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o número de pixels pelos quais a caixa de listagem pode ser rolada.

Windows 95/Windows 98/Windows Edition DaNium (Windows Me) : o parâmetro *wParam* é limitado a valores de 16 bits.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Para responder à mensagem **LB \_ LBORIZONTALEXTENT,** a caixa de listagem deve ter sido definida com o [**estilo \_ HSCROLL do WS.**](/windows/desktop/winmsg/window-styles)

Observe que uma caixa de listagem não atualiza sua extensão horizontal dinamicamente.

Essa mensagem não tem nenhum efeito em uma caixa de listagem de várias colunas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LB \_ GETHORIZONTALEXTENT**](lb-gethorizontalextent.md)
</dt> </dl>

 

