---
title: Mensagem de LB_SETHORIZONTALEXTENT (WinUser. h)
description: Define a largura, em pixels, pela qual uma caixa de listagem pode ser rolada horizontalmente (a largura rolável).
ms.assetid: 7d59b6de-2a22-4246-936b-4c669d285392
keywords:
- Controles de LB_SETHORIZONTALEXTENT de mensagens do Windows
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
ms.openlocfilehash: ded17b9ea2d78a77b030950877047256d0e2a1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824677"
---
# <a name="lb_sethorizontalextent-message"></a>SETHORIZONTALEXTENT de mensagens de LB \_

Define a largura, em pixels, pela qual uma caixa de listagem pode ser rolada horizontalmente (a largura rolável). Se a largura da caixa de listagem for menor que esse valor, a barra de rolagem horizontal rolará horizontalmente os itens na caixa de listagem. Se a largura da caixa de listagem for igual ou maior que esse valor, a barra de rolagem horizontal ficará oculta.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o número de pixels pelos quais a caixa de listagem pode ser rolada.

Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Para responder à mensagem **\_ SETHORIZONTALEXTENT de lb** , a caixa de listagem deve ter sido definida com o estilo [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) .

Observe que uma caixa de listagem não atualiza sua extensão horizontal dinamicamente.

Esta mensagem não tem nenhum efeito em uma caixa de listagem de várias colunas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_GETHORIZONTALEXTENT lb**](lb-gethorizontalextent.md)
</dt> </dl>

 

