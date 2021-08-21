---
title: Mensagem de WM_DRAWITEM (WinUser. h)
description: Enviado para a janela pai de um botão, caixa de combinação, caixa de listagem ou menu de desenho de proprietário quando um aspecto visual do botão, caixa de combinação, caixa de listagem ou menu foi alterado.
ms.assetid: e54bae5e-10d6-43b0-a766-1b270c8873a9
keywords:
- controles de Windows de mensagem de WM_DRAWITEM
topic_type:
- apiref
api_name:
- WM_DRAWITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f5d4b2addfa2de5f8c76ded636ca29a96fb3af7e0ab4157d25ac26a78c462c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957515"
---
# <a name="wm_drawitem-message"></a>Mensagem do WM \_ DRAWITEM

Enviado para a janela pai de um botão, caixa de combinação, caixa de listagem ou menu de desenho de proprietário quando um aspecto visual do botão, caixa de combinação, caixa de listagem ou menu foi alterado.

Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
WM_DRAWITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o identificador do controle que enviou a mensagem **de \_ DRAWITEM do WM** . Se a mensagem foi enviada por um menu, esse parâmetro será zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) que contém informações sobre o item a ser desenhado e o tipo de desenho necessário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processar essa mensagem, ele deverá retornar **true**.

## <a name="remarks"></a>Comentários

Por padrão, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) desenha o retângulo de foco para um item da caixa de listagem desenhada pelo proprietário.

O membro de *ação* da estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) especifica a operação de desenho que um aplicativo deve executar.

Antes de retornar do processamento dessa mensagem, um aplicativo deve garantir que o contexto do dispositivo identificado pelo membro *HDC* da estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) esteja no estado padrão.

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

[**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

