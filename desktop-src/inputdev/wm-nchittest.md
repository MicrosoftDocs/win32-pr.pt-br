---
title: Mensagem de WM_NCHITTEST (WinUser. h)
description: Enviado para uma janela a fim de determinar qual parte da janela corresponde a uma coordenada de tela específica.
ms.assetid: 4c860466-a9f8-4af8-96b9-cee005481875
keywords:
- Entrada de mouse e teclado de mensagem WM_NCHITTEST
topic_type:
- apiref
api_name:
- WM_NCHITTEST
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf14e817831c099988e9fb3fee57ae0731ef621
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105813580"
---
# <a name="wm_nchittest-message"></a>Mensagem do WM \_ NCHITTEST

Enviado para uma janela a fim de determinar qual parte da janela corresponde a uma coordenada de tela específica. Isso pode acontecer, por exemplo, quando o cursor se move, quando um botão do mouse é pressionado ou liberado, ou em resposta a uma chamada para uma função como [**WindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-windowfrompoint). Se o mouse não for capturado, a mensagem será enviada para a janela abaixo do cursor. Caso contrário, a mensagem será enviada para a janela que capturou o mouse.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCHITTEST                    0x0084
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem inferior Especifica a coordenada x do cursor. A coordenada é relativa ao canto superior esquerdo da tela.

A palavra de ordem superior especifica a coordenada y do cursor. A coordenada é relativa ao canto superior esquerdo da tela.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno da função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) é um dos valores a seguir, indicando a posição do ponto de acesso do cursor.



| Código/valor de retorno                                                                                                                                    | Descrição                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**HTBORDER**</dt> <dt>18</dt> </dl>      | Na borda de uma janela que não tem uma borda de dimensionamento.<br/>                                                                                                                                           |
| <dl> <dt>**HTBOTTOM**</dt> <dt>15</dt> </dl>      | Na borda inferior horizontal de uma janela redimensionável (o usuário pode clicar no mouse para redimensionar a janela verticalmente).<br/>                                                                                    |
| <dl> <dt>**HTBOTTOMLEFT**</dt> <dt>16</dt> </dl>  | No canto inferior esquerdo de uma borda de uma janela redimensionável (o usuário pode clicar no mouse para redimensionar a janela diagonalmente).<br/>                                                                              |
| <dl> <dt>**HTBOTTOMRIGHT**</dt> <dt>17</dt> </dl> | No canto inferior direito de uma borda de uma janela redimensionável (o usuário pode clicar no mouse para redimensionar a janela diagonalmente).<br/>                                                                             |
| <dl> <dt>**HTCAPTION**</dt> <dt>2</dt> </dl>      | Em uma barra de título.<br/>                                                                                                                                                                                         |
| <dl> <dt>**HTCLIENT**</dt> <dt>1</dt> </dl>       | Em uma área de cliente.<br/>                                                                                                                                                                                       |
| <dl> <dt>**HTCLOSE**</dt> <dt>20</dt> </dl>       | Em um botão **fechar** .<br/>                                                                                                                                                                                  |
| <dl> <dt>**HTERROR**</dt> <dt>-2</dt> </dl>       | Na tela de fundo ou em uma linha divisória entre janelas (o mesmo que **HTNOWHERE**, exceto que a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) produz um aviso sonoro do sistema para indicar um erro).<br/> |
| <dl> <dt>**HTGROWBOX**</dt> <dt>4</dt> </dl>      | Em uma caixa de tamanho (igual a **HTSIZE**).<br/>                                                                                                                                                                     |
| <dl> <dt>**HTHELP**</dt> <dt>21</dt> </dl>        | Em um botão de **ajuda** .<br/>                                                                                                                                                                                   |
| <dl> <dt>**HTHSCROLL**</dt> <dt>6</dt> </dl>      | Em uma barra de rolagem horizontal.<br/>                                                                                                                                                                             |
| <dl> <dt>**HTLEFT**</dt> <dt>10</dt> </dl>        | Na borda esquerda de uma janela redimensionável (o usuário pode clicar no mouse para redimensionar a janela horizontalmente).<br/>                                                                                              |
| <dl> <dt>**HTMENU**</dt> <dt>5</dt> </dl>         | Em um menu.<br/>                                                                                                                                                                                              |
| <dl> <dt>**HTMAXBUTTON**</dt> <dt>9</dt> </dl>    | Em um botão **maximizar** .<br/>                                                                                                                                                                               |
| <dl> <dt>**HTMINBUTTON**</dt> <dt>8</dt> </dl>    | Em um botão **minimizar** .<br/>                                                                                                                                                                               |
| <dl> <dt>**HTNOWHERE**</dt> <dt>0</dt> </dl>      | Na tela de fundo ou em uma linha divisória entre janelas.<br/>                                                                                                                                         |
| <dl> <dt>**HTREDUCE**</dt> <dt>8</dt> </dl>       | Em um botão **minimizar** .<br/>                                                                                                                                                                               |
| <dl> <dt>**HTRIGHT**</dt> <dt>11</dt> </dl>       | Na borda direita de uma janela redimensionável (o usuário pode clicar no mouse para redimensionar a janela horizontalmente).<br/>                                                                                             |
| <dl> <dt>**HTSIZE**</dt> <dt>4</dt> </dl>         | Em uma caixa de tamanho (igual a **HTGROWBOX**).<br/>                                                                                                                                                                  |
| <dl> <dt>**HTSYSMENU**</dt> <dt>3</dt> </dl>      | Em um menu de janela ou em um botão **fechar** em uma janela filho.<br/>                                                                                                                                            |
| <dl> <dt>**HTTOP**</dt> <dt>12</dt> </dl>         | Na borda superior horizontal de uma janela.<br/>                                                                                                                                                             |
| <dl> <dt>**HTTOPLEFT**</dt> <dt>13</dt> </dl>     | No canto superior esquerdo de uma borda de janela.<br/>                                                                                                                                                            |
| <dl> <dt>**HTTOPRIGHT**</dt> <dt>14</dt> </dl>    | No canto superior direito de uma borda de janela.<br/>                                                                                                                                                           |
| <dl> <dt>**HTTRANSPARENT**</dt> <dt>-1</dt> </dl> | Em uma janela atualmente coberta por outra janela no mesmo thread (a mensagem será enviada para janelas subjacentes no mesmo thread até que um deles retorne um código que não seja **HTTRANSPARENT**).<br/>  |
| <dl> <dt>**HTVSCROLL**</dt> <dt>7</dt> </dl>      | Na barra de rolagem vertical.<br/>                                                                                                                                                                             |
| <dl> <dt>**HTZOOM**</dt> <dt>9</dt> </dl>         | Em um botão **maximizar** .<br/>                                                                                                                                                                               |



 

## <a name="remarks"></a>Comentários

Use o código a seguir para obter a posição horizontal e vertical:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



Conforme observado acima, a coordenada x está **na ordem inferior** do valor de retorno; a coordenada y está no **intervalo** de ordem superior (ambos representam valores *assinados* porque podem receber valores negativos em sistemas com vários monitores). Se o valor de retorno for atribuído a uma variável, você poderá usar a macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obter uma estrutura de [**pontos**](/previous-versions//dd162808(v=vs.85)) do valor de retorno. Você também pode usar a macro [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extrair a coordenada x ou Y.

> [!IMPORTANT]
> Não use as macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extrair as coordenadas x e y da posição do cursor, pois essas macros retornam resultados incorretos em sistemas com vários monitores. Sistemas com vários monitores podem ter coordenadas x e y negativas e **LOWORD** e **HIWORD** tratam as coordenadas como quantidades não assinadas.

 

**Windows Vista:** Ao criar quadros personalizados que incluem os botões de legenda padrão, essa mensagem deve ser passada primeiro para a função [**DwmDefWindowProc**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmdefwindowproc) . Isso permite que o Gerenciador de Janelas da Área de Trabalho (DWM) forneça testes de colisão para os botões de legendas. Se **DwmDefWindowProc** não tratar a mensagem, o processamento adicional do **WM \_ NCHITTEST** poderá ser necessário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windowsx. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**OBTER \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**OBTER \_ \_ lParam Y**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Entrada do mouse](mouse-input.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**FAIXAS**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

