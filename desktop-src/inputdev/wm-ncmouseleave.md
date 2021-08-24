---
title: Mensagem de WM_NCMOUSELEAVE (WinUser. h)
description: Postado em uma janela quando o cursor sai da área não cliente da janela especificada em uma chamada anterior para TrackMouseEvent.
ms.assetid: b3ada6db-93ce-45d7-b408-d08692328aeb
keywords:
- Entrada de mouse e teclado de mensagem WM_NCMOUSELEAVE
topic_type:
- apiref
api_name:
- WM_NCMOUSELEAVE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 141c4f1f2483e1cbd725a70454b1df1be12c46ec1970c052938181fb511ed248
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778446"
---
# <a name="wm_ncmouseleave-message"></a>Mensagem do WM \_ NCMOUSELEAVE

Postado em uma janela quando o cursor sai da área não cliente da janela especificada em uma chamada anterior para [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCMOUSELEAVE                 0x02A2
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado e deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro não é usado e deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

Todo o controle solicitado por [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) é cancelado quando esta mensagem é gerada. O aplicativo deve chamar **TrackMouseEvent** quando o mouse reinserir sua janela se precisar de mais controle sobre o comportamento de focalização do mouse.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[**SYSCOMMAND do WM \_**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[**MOUSELEAVE do WM \_**](wm-mouseleave.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Entrada do mouse](mouse-input.md)
</dt> </dl>

 

