---
title: Mensagem de WM_DPICHANGED_AFTERPARENT (WinUser. h)
description: Para as janelas de nível superior de cada monitor v2, essa mensagem é enviada a todos os HWNDs na árvore HWDN filho da janela que está passando por uma alteração de DPI. | Mensagem de WM_DPICHANGED_AFTERPARENT (WinUser. h)
ms.assetid: FEA1BF07-55B6-4584-ABD3-340515831E0A
keywords:
- DPI alta de mensagem de WM_DPICHANGED_AFTERPARENT
topic_type:
- apiref
api_name:
- WM_DPICHANGED_AFTERPARENT
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cc76602662cefba42f62bd3ed85913ade40f15
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105761920"
---
# <a name="wm_dpichanged_afterparent-message"></a>Mensagem de AFTERPARENT do WM \_ DPICHANGED \_

Para as janelas de nível superior de [cada monitor v2](dpi-awareness-context.md) , essa mensagem é enviada a todos os HWNDs na árvore HWDN filho da janela que está passando por uma alteração de DPI. Essa mensagem ocorre depois que a janela de nível superior recebe o [**WM \_ DPICHANGED**](wm-dpichanged.md)e percorre a árvore filho de cima para baixo.


```C++
#define WM_DPICHANGED_AFTERPARENT       0x02E3
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse valor não é usado e será zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Esse valor não é usado e será zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse valor não é usado e ignorado pelo sistema.

## <a name="remarks"></a>Comentários

Não há nenhum tratamento padrão dessa mensagem no [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).

Essa mensagem é enviada somente quando a janela de nível superior tem um contexto de reconhecimento de DPI de PMv2.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]<br/>                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>WinUser. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DPICHANGED do WM \_**](wm-dpichanged.md)
</dt> <dt>

[**BEFOREPARENT do WM \_ DPICHANGED \_**](wm-dpichanged-beforeparent.md)
</dt> </dl>

 

