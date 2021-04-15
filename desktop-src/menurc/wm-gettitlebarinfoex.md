---
title: Mensagem de WM_GETTITLEBARINFOEX (WinUser. h)
description: Enviado para solicitar informações da barra de título estendida. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: 0760dbf1-5b20-471c-bfd9-b8d28b52074b
keywords:
- WM_GETTITLEBARINFOEX menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_GETTITLEBARINFOEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea31326faf5953df0facf34b58b06d7766c2e7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369356"
---
# <a name="wm_gettitlebarinfoex-message"></a>Mensagem do WM \_ GETTITLEBARINFOEX

Enviado para solicitar informações da barra de título estendida. Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_GETTITLEBARINFOEX            0x033F
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado e deve ser 0.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) . O remetente da mensagem é responsável por alocar memória para esta estrutura. Defina o membro **cbSize** dessa estrutura como `sizeof(TITLEBARINFOEX)` antes de passar essa estrutura com a mensagem.

</dd> </dl>

## <a name="remarks"></a>Comentários

O exemplo a seguir mostra como o receptor de mensagem converte um valor de **lParam** para recuperar a estrutura [**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) .

`TITLEBARINFOEX *ptinfo = (TITLEBARINFOEX *)lParam;`

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral dos menus](menus.md)
</dt> </dl>

 

