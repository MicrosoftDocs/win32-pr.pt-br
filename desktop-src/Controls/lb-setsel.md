---
title: LB_SETSEL mensagem (Winuser.h)
description: Seleciona um item em uma caixa de listagem de seleção múltipla e, se necessário, rola o item para a exibição.
ms.assetid: 643783f2-0e00-4b79-b957-47938bb9f8da
keywords:
- LB_SETSEL controles Windows mensagem
topic_type:
- apiref
api_name:
- LB_SETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4830dc83a2b62fa87a222be276cdd9db55720014adeaa03362f4965bc0ecf246
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958525"
---
# <a name="lb_setsel-message"></a>Mensagem LB \_ SETSEL

Seleciona um item em uma caixa de listagem de seleção múltipla e, se necessário, rola o item para a exibição.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica como definir a seleção. Se esse parâmetro for **TRUE,** o item será selecionado e realçado; se for **FALSE**, o realçando será removido e o item não será mais selecionado.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica o índice baseado em zero do item a ser definido. Se esse parâmetro for -1, a seleção será adicionada ou removida de todos os itens, dependendo do valor *de wParam* e nenhuma rolagem ocorrerá.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se ocorrer um erro, o valor de retorno será LB \_ ERR.

## <a name="remarks"></a>Comentários

Use essa mensagem somente com caixas de listagem de seleção múltipla.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**LB \_ GETSEL**](lb-getsel.md)
</dt> <dt>

[**LB \_ SELITEMRANGE**](lb-selitemrange.md)
</dt> </dl>

 

 





