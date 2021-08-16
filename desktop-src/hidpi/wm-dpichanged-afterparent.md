---
title: WM_DPICHANGED_AFTERPARENT mensagem (Winuser.h)
description: Para janelas de nível superior por monitor v2, essa mensagem é enviada a todos os HWNDs na árvore HWDN filho da janela que está passando por uma alteração de DPI. | WM_DPICHANGED_AFTERPARENT mensagem (Winuser.h)
ms.assetid: FEA1BF07-55B6-4584-ABD3-340515831E0A
keywords:
- WM_DPICHANGED_AFTERPARENT DPI alto da mensagem
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
ms.openlocfilehash: d47f303db19438f1e7e2cd77df60ddace76bec791bb1789bed47e3f09d8a197c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118759359"
---
# <a name="wm_dpichanged_afterparent-message"></a>Mensagem WM \_ DPICHANGED \_ AFTERPARENT

Para janelas de nível superior por monitor [v2,](dpi-awareness-context.md) essa mensagem é enviada a todos os HWNDs na árvore HWDN filho da janela que está passando por uma alteração de DPI. Essa mensagem ocorre depois que a janela de nível superior recebe [**WM \_ DPICHANGED**](wm-dpichanged.md)e atravessa a árvore filho da parte superior para baixo.


```C++
#define WM_DPICHANGED_AFTERPARENT       0x02E3
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse valor não é usada e será zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Esse valor não é usada e será zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse valor não éusado e ignorado pelo sistema.

## <a name="remarks"></a>Comentários

Não há nenhum tratamento padrão dessa mensagem em [DefWindowProc.](/windows/win32/api/winuser/nf-winuser-defwindowproca)

Essa mensagem só é enviada quando a janela de nível superior tem um contexto de reconhecimento de DPI de PMv2.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1703 somente \[ aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2016 somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**WM \_ DPICHANGED**](wm-dpichanged.md)
</dt> <dt>

[**WM \_ DPICHANGED \_ BEFOREPARENT**](wm-dpichanged-beforeparent.md)
</dt> </dl>

 

