---
title: Mensagem de WM_CAPTURECHANGED (WinUser. h)
description: Enviado para a janela que está perdendo a captura do mouse.
ms.assetid: 79c8f65e-31fa-4bdb-9e88-0160a52b5b7d
keywords:
- Entrada de mouse e teclado de mensagem WM_CAPTURECHANGED
topic_type:
- apiref
api_name:
- WM_CAPTURECHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050bc00a7ab19e22e0fe4ea1f35271707180d4d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085426"
---
# <a name="wm_capturechanged-message"></a>Mensagem do WM \_ capturachanged

Enviado para a janela que está perdendo a captura do mouse.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_CAPTURECHANGED               0x0215
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um identificador para a janela que ganha a captura do mouse.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um aplicativo deve retornar zero se ele processar essa mensagem.

## <a name="remarks"></a>Comentários

Uma janela recebe essa mensagem, mesmo que chame o próprio [**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture) . Um aplicativo não deve tentar definir a captura do mouse em resposta a essa mensagem.

Quando ele recebe essa mensagem, uma janela deve ser redesenhada, se necessário, para refletir o novo estado de captura do mouse.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

[**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Entrada do mouse](mouse-input.md)
</dt> </dl>

 

