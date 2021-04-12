---
title: Mensagem de LB_SETSEL (WinUser. h)
description: Seleciona um item em uma caixa de listagem de seleção múltipla e, se necessário, rola o item para a exibição.
ms.assetid: 643783f2-0e00-4b79-b957-47938bb9f8da
keywords:
- Controles de LB_SETSEL de mensagens do Windows
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
ms.openlocfilehash: cd50f12c4190ba9ecafad11b167c1ac60adf691d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455753"
---
# <a name="lb_setsel-message"></a>SETSEL de mensagens de LB \_

Seleciona um item em uma caixa de listagem de seleção múltipla e, se necessário, rola o item para a exibição.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica como definir a seleção. Se esse parâmetro for **true**, o item será selecionado e realçado; Se for **false**, o realce será removido e o item não será mais selecionado.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica o índice de base zero do item a ser definido. Se esse parâmetro for-1, a seleção será adicionada ou removida de todos os itens, dependendo do valor de *wParam*, e não ocorrerá nenhuma rolagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se ocorrer um erro, o valor de retorno será um erro de LB \_ .

## <a name="remarks"></a>Comentários

Use essa mensagem somente com caixas de listagem de seleção múltipla.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**\_GETSEL lb**](lb-getsel.md)
</dt> <dt>

[**\_SELITEMRANGE lb**](lb-selitemrange.md)
</dt> </dl>

 

 





