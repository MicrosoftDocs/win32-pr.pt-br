---
title: Mensagem de WM_MOUSEWHEEL (WinUser. h)
description: Enviado para a janela de foco quando a roda do mouse é girada.
ms.assetid: 9831cceb-bbf3-42a0-a0f9-c2d6ad4573eb
keywords:
- Entrada de mouse e teclado de mensagem WM_MOUSEWHEEL
topic_type:
- apiref
api_name:
- WM_MOUSEWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae3e750a8544c050e735671b7fd2df6980d53b1200e2f67493b46ad7a2e0b017
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888726"
---
# <a name="wm_mousewheel-message"></a>Mensagem do WM \_ MOUSEWHEEL

Enviado para a janela de foco quando a roda do mouse é girada. A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) propaga a mensagem para o pai da janela. Não deve haver nenhum encaminhamento interno da mensagem, pois **DefWindowProc** propaga a cadeia pai até encontrar uma janela que a processa.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_MOUSEWHEEL                   0x020A
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A palavra de ordem superior indica a distância em que a roda é girada, expressa em múltiplos ou divisões do **Wheel \_ Delta**, que é 120. Um valor positivo indica que a roda foi girada para frente, afastando-a do usuário; um valor negativo indica que a roda foi girada para trás, em direção ao usuário.

A palavra de ordem inferior indica se várias chaves virtuais estão inativas. Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                               | Significado                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_**</dt> <dt>0X0008</dt> de controle </dl>    | A tecla CTRL está inoperante.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt> </dl>    | O botão esquerdo do mouse está inativo.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt> </dl>    | O botão do meio do mouse está inativo.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt> </dl>    | O botão direito do mouse está inativo.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt> </dl>          | A tecla SHIFT está inoperante.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt> </dl> | O primeiro botão X está inoperante.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt> </dl> | O segundo botão X está inoperante.<br/>     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem inferior Especifica a coordenada x do ponteiro, em relação ao canto superior esquerdo da tela.

A palavra de ordem superior especifica a coordenada y do ponteiro, em relação ao canto superior esquerdo da tela.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

Use o código a seguir para obter as informações no parâmetro *wParam* :


```
fwKeys = GET_KEYSTATE_WPARAM(wParam);
zDelta = GET_WHEEL_DELTA_WPARAM(wParam);
```



Use o código a seguir para obter a posição horizontal e vertical:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Conforme observado acima, a coordenada x está **na ordem inferior** do valor de retorno; a coordenada y está no **intervalo** de ordem superior (ambos representam valores *assinados* porque podem receber valores negativos em sistemas com vários monitores). Se o valor de retorno for atribuído a uma variável, você poderá usar a macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obter uma estrutura de [**pontos**](/previous-versions//dd162808(v=vs.85)) do valor de retorno. Você também pode usar a macro [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extrair a coordenada x ou Y.

> [!IMPORTANT]
> Não use as macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extrair as coordenadas x e y da posição do cursor, pois essas macros retornam resultados incorretos em sistemas com vários monitores. Sistemas com vários monitores podem ter coordenadas x e y negativas e **LOWORD** e **HIWORD** tratam as coordenadas como quantidades não assinadas.

 

A rotação da roda será um múltiplo do **Wheel \_ Delta**, que é definido em 120. Esse é o limite para a ação a ser tomada e uma ação desse tipo (por exemplo, rolagem de um incremento) deve ocorrer para cada Delta.

O Delta foi definido como 120 para permitir que a Microsoft ou outros fornecedores criem rodas de resolução mais fina (uma roda de rotação livre sem entalhes) para enviar mais mensagens por rotação, mas com um valor menor em cada mensagem. Para usar esse recurso, você pode adicionar os valores Delta de entrada até que o **Wheel \_ Delta** seja atingido (para que uma rotação Delta obtenha a mesma resposta) ou role as linhas parciais em resposta às mensagens mais frequentes. Você também pode escolher a granularidade da rolagem e acumular deltas até que ele seja atingido.

Observe que não há nenhum *fwKeys* para **MSH \_ MOUSEWHEEL**. Caso contrário, os parâmetros são exatamente iguais aos do **WM \_ MOUSEWHEEL**.

Cabe ao aplicativo encaminhar **MSH \_ MOUSEWHEEL** a quaisquer objetos ou controles inseridos. O aplicativo é necessário para enviar a mensagem a um aplicativo OLE incorporado ativo. É opcional que o aplicativo o envia para um controle habilitado para roda com foco. Se o aplicativo enviar a mensagem a um controle, ele poderá verificar o valor de retorno para ver se a mensagem foi processada. Os controles são necessários para retornar um valor **true** se eles processarem a mensagem.

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

[**OBTER \_ \_ wParam KeyState**](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[**OBTER \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**OBTER \_ \_ lParam Y**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**OBTER \_ \_ wParam Delta do volante \_**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**evento do mouse \_**](/windows/win32/api/winuser/nf-winuser-mouse_event)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Entrada do mouse](mouse-input.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> <dt>

[**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**FAIXAS**](/previous-versions//dd162808(v=vs.85))
</dt> <dt>

[**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

