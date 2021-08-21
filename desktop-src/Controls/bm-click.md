---
title: BM_CLICK mensagem (Winuser.h)
description: Simula o usuário clicando em um botão. Essa mensagem faz com que o botão receba as mensagens WM LBUTTONDOWN e WM LBUTTONUP e a janela pai do botão para receber um código de notificação \_ \_ BN \_ CLICKED.
ms.assetid: f76ca5eb-170c-43fc-a239-67af15497f08
keywords:
- BM_CLICK controles de Windows mensagem
topic_type:
- apiref
api_name:
- BM_CLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97fdf1e206546bcdb3fa0888276414bd44b927e96a8478be4ae8a5ce2d2a5169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674974"
---
# <a name="bm_click-message"></a>Mensagem BM \_ CLICK

Simula o usuário clicando em um botão. Essa mensagem faz com que o botão receba as mensagens [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) e [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) e a janela pai do botão para receber um código de notificação [BN \_ CLICKED.](bn-clicked.md)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Se o botão estiver em uma caixa de diálogo e a caixa de diálogo não estiver ativa, a **mensagem BM \_ CLICK** poderá falhar. Para garantir o sucesso nessa situação, chame a função [**SetActiveWindow**](/windows/desktop/api/winuser/nf-winuser-setactivewindow) para ativar a caixa de diálogo antes de enviar a **mensagem BM \_ CLICK** para o botão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



 

