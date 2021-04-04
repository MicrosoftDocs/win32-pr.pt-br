---
title: Mensagem de BM_CLICK (WinUser. h)
description: Simula o usuário clicando em um botão. Essa mensagem faz com que o botão receba as \_ mensagens do WM LBUTTONDOWN e do WM \_ LBUTTONUP, e a janela pai do botão receba um \_ código de notificação clicado em bilhão.
ms.assetid: f76ca5eb-170c-43fc-a239-67af15497f08
keywords:
- Controles de BM_CLICK de mensagens do Windows
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
ms.openlocfilehash: 7b86c4809ac1ded3a9b7c57d1b73b70ab1cebc3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009074"
---
# <a name="bm_click-message"></a>BM \_ clique em mensagem

Simula o usuário clicando em um botão. Essa mensagem faz com que o botão receba as mensagens do [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) e do [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) , e a janela pai do botão receba um código de notificação [ \_ clicado em bilhão](bn-clicked.md) .

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

## <a name="return-value"></a>Retornar valor

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Se o botão estiver em uma caixa de diálogo e a caixa de diálogo não estiver ativa, a mensagem de **\_ clique BM** poderá falhar. Para garantir o sucesso nessa situação, chame a função [**SetActiveWindow**](/windows/desktop/api/winuser/nf-winuser-setactivewindow) para ativar a caixa de diálogo antes de enviar a mensagem de **\_ clique BM** para o botão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



 

