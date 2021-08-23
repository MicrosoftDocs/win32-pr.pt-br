---
title: WM_MOUSEHOVER mensagem (Winuser.h)
description: Postado em uma janela quando o cursor passar o mouse sobre a área do cliente da janela pelo período de tempo especificado em uma chamada anterior para TrackMouseEvent.
ms.assetid: efba7f04-2d26-44f1-89df-a565c03ad944
keywords:
- WM_MOUSEHOVER entrada do mouse e teclado da mensagem
topic_type:
- apiref
api_name:
- WM_MOUSEHOVER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52a8fb4aef4d363b87b0093316d264dddb212aa11d42e10b6ae97a4a93ee46a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451496"
---
# <a name="wm_mousehover-message"></a>Mensagem \_ WM MOUSEHOVER

Postado em uma janela quando o cursor passar o mouse sobre a área do cliente da janela pelo período de tempo especificado em uma chamada anterior para [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_MOUSEHOVER                   0x02A1
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Indica se várias chaves virtuais estão inoadas. Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                               | Significado                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_ CONTROLE**</dt> <dt>0x0008</dt> </dl>    | A tecla CTRL está desaixado.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt> </dl>    | O botão esquerdo do mouse está pressionado.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt> </dl>    | O botão do meio do mouse é pressionado.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt> </dl>    | O botão direito do mouse está pressionado.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt> </dl>          | A tecla SHIFT é desaixado.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt> </dl> | O primeiro botão X está ino mouse.<br/>           |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt> </dl> | O segundo botão X está ino mouse.<br/>          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem baixa especifica a coordenada X do cursor. A coordenada é relativa ao canto superior esquerdo da área do cliente.

A palavra de ordem alta especifica a coordenada y do cursor. A coordenada é relativa ao canto superior esquerdo da área do cliente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processa essa mensagem, ele deve retornar zero.

## <a name="remarks"></a>Comentários

O acompanhamento de foco para **quando WM \_ MOUSEHOVER** é gerado. O aplicativo deverá chamar [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) novamente se exigir um acompanhamento posterior do comportamento de foco do mouse.

Use o código a seguir para obter a posição horizontal e vertical:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Conforme mencionado acima, a coordenada x está na ordem baixa **a menos** que o valor de retorno; a coordenada y está em ordem alta  curta **(ambas** representam valores assinados porque podem receber valores negativos em sistemas com vários monitores). Se o valor de retorno for atribuído a uma variável, você poderá usar a macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obter uma estrutura [**POINTS**](/previous-versions//dd162808(v=vs.85)) do valor de retorno. Você também pode usar a [**macro GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) ou [**GET Y \_ \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extrair a coordenada x ou y.

> [!IMPORTANT]
> Não use as macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extrair as coordenadas x e y da posição do cursor porque essas macros retornam resultados incorretos em sistemas com vários monitores. Sistemas com vários monitores podem ter coordenadas x e y negativas, e **LOWORD** e **HIWORD** tratam as coordenadas como quantidades sem sinal.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (inclua Windowsx.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[**Setcapture**](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[**Trackmouseevent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[**Trackmouseevent**](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Entrada do mouse](mouse-input.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**Pontos**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

