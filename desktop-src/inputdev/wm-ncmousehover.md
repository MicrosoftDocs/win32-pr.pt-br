---
title: Mensagem de WM_NCMOUSEHOVER (WinUser. h)
description: Postado em uma janela quando o cursor passa sobre a área não cliente da janela pelo período de tempo especificado em uma chamada anterior para TrackMouseEvent.
ms.assetid: ca1afdc2-7884-445e-b9b7-4d7dd5dcea38
keywords:
- Entrada de mouse e teclado de mensagem WM_NCMOUSEHOVER
topic_type:
- apiref
api_name:
- WM_NCMOUSEHOVER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 323464d32a2529475823003e51d5bbf0b15c616e32edb0622efe5be7f94dfb4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611456"
---
# <a name="wm_ncmousehover-message"></a>Mensagem do WM \_ NCMOUSEHOVER

Postado em uma janela quando o cursor passa sobre a área não cliente da janela pelo período de tempo especificado em uma chamada anterior para [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCMOUSEHOVER                 0x02A0
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O valor de teste de clique retornado pela função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) como resultado do processamento da mensagem [**\_ NCHITTEST do WM**](wm-nchittest.md) . Para obter uma lista de valores de teste de clique, consulte **WM \_ NCHITTEST**.

</dd> <dt>

*lParam* 
</dt> <dd>

Uma estrutura de [**pontos**](/previous-versions//dd162808(v=vs.85)) que contém as coordenadas x e y do cursor. As coordenadas são relativas ao canto superior esquerdo da tela.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

O controle de foco para quando essa mensagem é gerada. O aplicativo deve chamar [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) novamente se precisar de mais controle sobre o comportamento de focalização do mouse.

Você também pode usar as macros [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) e [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extrair os valores das coordenadas X e y do *lParam*.


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> Não use as macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extrair as coordenadas x e y da posição do cursor, pois essas macros retornam resultados incorretos em sistemas com vários monitores. Sistemas com vários monitores podem ter coordenadas x e y negativas e **LOWORD** e **HIWORD** tratam as coordenadas como quantidades não assinadas.

 

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

[**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[**NCHITTEST do WM \_**](wm-nchittest.md)
</dt> <dt>

[**MOUSEHOVER do WM \_**](wm-mousehover.md)
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

 

