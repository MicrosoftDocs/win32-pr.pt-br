---
title: Mensagem de WM_CLIPBOARDUPDATE (WinUser. h)
description: Enviado quando o conteúdo da área de transferência foi alterado.
ms.assetid: 1508aa22-9cf0-40a2-8cb0-ce7c8671df2c
keywords:
- WM_CLIPBOARDUPDATE Exchange de dados da mensagem
topic_type:
- apiref
api_name:
- WM_CLIPBOARDUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0483ba43b6b0c660daee74637fd9f9ac8d377a16097b5cfd60632c1b691ead7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991216"
---
# <a name="wm_clipboardupdate-message"></a>Mensagem do WM \_ CLIPBOARDUPDATE

Enviado quando o conteúdo da área de transferência foi alterado.


```C++
#define WM_CLIPBOARDUPDATE              0x031D
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

Para registrar uma janela para receber essa mensagem, use a função [**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**AddClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener)
</dt> <dt>

[**RemoveClipboardFormatListener**](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener)
</dt> <dt>

[**GetClipboardSequenceNumber**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber)
</dt> </dl>

 

 





