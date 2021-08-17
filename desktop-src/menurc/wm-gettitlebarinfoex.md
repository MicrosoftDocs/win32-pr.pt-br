---
title: WM_GETTITLEBARINFOEX mensagem (Winuser.h)
description: Enviado para solicitar informações estendidas da barra de título. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: 0760dbf1-5b20-471c-bfd9-b8d28b52074b
keywords:
- WM_GETTITLEBARINFOEX menus de mensagem e outros recursos
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
ms.openlocfilehash: 1acbe85afa1871caf796c70a9535f5646d2511317a0e9ee0564db55101a16449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869662"
---
# <a name="wm_gettitlebarinfoex-message"></a>Mensagem WM \_ GETTITLEBARINFOEX

Enviado para solicitar informações estendidas da barra de título. Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

Um ponteiro para uma [**estrutura TITLEBARINFOEX.**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) O remetente da mensagem é responsável por alocar memória para essa estrutura. De definir **o membro cbSize** dessa estrutura como `sizeof(TITLEBARINFOEX)` antes de passar essa estrutura com a mensagem .

</dd> </dl>

## <a name="remarks"></a>Comentários

O exemplo a seguir mostra como o receptor da mensagem lança um **valor LPARAM** para recuperar a [**estrutura TITLEBARINFOEX.**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex)

`TITLEBARINFOEX *ptinfo = (TITLEBARINFOEX *)lParam;`

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral de menus](menus.md)
</dt> </dl>

 

