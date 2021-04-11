---
title: Mensagem de LB_SELITEMRANGE (WinUser. h)
description: Seleciona ou anula a seleção de um ou mais itens consecutivos em uma caixa de listagem de seleção múltipla.
ms.assetid: 817d62df-98a3-40b3-8d62-86bf07ad797f
keywords:
- Controles de LB_SELITEMRANGE de mensagens do Windows
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
ms.openlocfilehash: a137b90a817519cf23c894dc19417dd2d9b6b7f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009656"
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

## <a name="return-value"></a>Retornar valor

Se ocorrer um erro, o valor de retorno será um erro de LB \_ .

## <a name="remarks"></a>Comentários

Use essa mensagem somente com caixas de listagem de seleção múltipla.

Esta mensagem pode selecionar um intervalo somente dentro dos primeiros 65.536 itens.

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

[**\_SELITEMRANGEEX lb**](lb-selitemrangeex.md)
</dt> <dt>

[**\_SETSEL lb**](lb-setsel.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

