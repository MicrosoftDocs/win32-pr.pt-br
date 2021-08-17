---
title: Mensagem de LB_SELITEMRANGE (WinUser. h)
description: Seleciona ou anula a seleção de um ou mais itens consecutivos em uma caixa de listagem de seleção múltipla.
ms.assetid: 817d62df-98a3-40b3-8d62-86bf07ad797f
keywords:
- controles de Windows de mensagem de LB_SELITEMRANGE
topic_type:
- apiref
api_name:
- LB_SELITEMRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87a08019f3d60e6c9bfe841067b48220b8fcfe75891c9bcc8db64bf28d219b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958595"
---
# <a name="lb_selitemrange-message"></a>SELITEMRANGE de mensagens de LB \_

Seleciona ou anula a seleção de um ou mais itens consecutivos em uma caixa de listagem de seleção múltipla.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

**True** para selecionar o intervalo de itens ou **false** para desselecioná-lo.

</dd> <dt>

*lParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o índice de base zero do primeiro item a ser selecionado. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o índice de base zero do último item a ser selecionado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se ocorrer um erro, o valor de retorno será um erro de LB \_ .

## <a name="remarks"></a>Comentários

Use essa mensagem somente com caixas de listagem de seleção múltipla.

Esta mensagem pode selecionar um intervalo somente dentro dos primeiros 65.536 itens.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**\_SELITEMRANGEEX lb**](lb-selitemrangeex.md)
</dt> <dt>

[**\_SETSEL lb**](lb-setsel.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

