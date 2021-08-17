---
title: Mensagem de WM_CTLCOLORBTN (WinUser. h)
description: A mensagem do WM \_ CTLCOLORBTN é enviada para a janela pai de um botão antes de desenhar o botão. A janela pai pode alterar o texto do botão e as cores do plano de fundo. No entanto, somente botões desenhados pelo proprietário respondem à janela pai que processa essa mensagem.
ms.assetid: fd2ab917-ffd6-4f71-9b1c-0ecdfe53ae8b
keywords:
- controles de Windows de mensagem de WM_CTLCOLORBTN
topic_type:
- apiref
api_name:
- WM_CTLCOLORBTN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5689d7c76499f1ed180f76831af325c5e311bf06e052ea1446805c39ddf8642
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407635"
---
# <a name="wm_ctlcolorbtn-message"></a>Mensagem do WM \_ CTLCOLORBTN

A mensagem do **WM \_ CTLCOLORBTN** é enviada para a janela pai de um botão antes de desenhar o botão. A janela pai pode alterar o texto do botão e as cores do plano de fundo. No entanto, somente botões desenhados pelo proprietário respondem à janela pai que processa essa mensagem.


```C++
WM_CTLCOLORBTN

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um **HDC** que especifica o identificador para o contexto de exibição do botão.

</dd> <dt>

*lParam* 
</dt> <dd>

Um **HWND** que especifica o identificador para o botão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processar essa mensagem, ele deverá retornar um identificador para um pincel. O sistema usa o pincel para pintar o plano de fundo do botão.

## <a name="remarks"></a>Comentários

Se o aplicativo retornar um pincel que ele criou (por exemplo, usando a função [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) ou [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), o aplicativo deverá liberar o pincel. Se o aplicativo retornar um pincel do sistema (por exemplo, um que foi recuperado pela função [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) ou [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), o aplicativo não precisará liberar o pincel.

Por padrão, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleciona as cores padrão do sistema para o botão. Os botões com os estilos de botão de [**\_ pressão BS**](button-styles.md), [**BS \_ DEFPUSHBUTTON**](button-styles.md)ou [**BS \_ PUSHLIKE**](button-styles.md) não usam o pincel retornado. Os botões com esses estilos são sempre desenhados com as cores padrão do sistema. O desenho de botões de push requer vários pincéis diferentes: face, realce e sombra, mas a mensagem do **WM \_ CTLCOLORBTN** permite que apenas um pincel seja retornado. Para fornecer uma aparência personalizada para botões de push, use um botão de desenho proprietário. Para obter mais informações, consulte [criando controles de Owner-Drawn](user-controls-intro.md).

A mensagem do **WM \_ CTLCOLORBTN** nunca é enviada entre threads. Ele é enviado somente dentro de um thread.

A cor do texto de uma caixa de seleção ou botão de opção se aplica à caixa ou ao botão, à marca de seleção e ao texto. O retângulo de foco para esses botões permanece a cor padrão do sistema (normalmente preto). A cor do texto de uma caixa de grupo se aplica ao texto, mas não à linha que define a caixa. A cor do texto de um botão de ação é aplicável somente ao seu retângulo de foco; Ele não afeta a cor do texto.

Se um procedimento de caixa de diálogo tratar essa mensagem, ele deverá converter o valor de retorno desejado para um **int \_ PTR** e retornar o valor diretamente. Se o procedimento da caixa de diálogo retornar **false**, a manipulação de mensagens padrão será executada. O \_ valor de MSGRESULT DWL definido pela [**função SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Outros recursos**
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

