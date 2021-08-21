---
title: Mensagem de WM_DRAWCLIPBOARD (WinUser. h)
description: Enviado para a primeira janela na cadeia do Visualizador da área de transferência quando o conteúdo da área de transferência é alterado. Isso permite que uma janela do Visualizador da área de transferência exiba o novo conteúdo da área de transferência. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: ffaadf6f-588b-4a29-b26c-629087e7ce73
keywords:
- WM_DRAWCLIPBOARD Exchange de dados da mensagem
topic_type:
- apiref
api_name:
- WM_DRAWCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3706b0ce96531e4e9ca1354570439d57f06a97ecb78844160b035dcd7d96917e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915016"
---
# <a name="wm_drawclipboard-message"></a>Mensagem do WM \_ DRAWCLIPBOARD

Enviado para a primeira janela na cadeia do Visualizador da área de transferência quando o conteúdo da área de transferência é alterado. Isso permite que uma janela do Visualizador da área de transferência exiba o novo conteúdo da área de transferência.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_DRAWCLIPBOARD                0x0308
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

## <a name="remarks"></a>Comentários

Somente as janelas do Visualizador da área de transferência recebem essa mensagem. Essas são as janelas que foram adicionadas à cadeia do Visualizador da área de transferência usando a função [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) .

Cada janela que recebe a **mensagem \_ DRAWCLIPBOARD do WM** deve chamar a função [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para passar a mensagem para a próxima janela na cadeia do Visualizador da área de transferência. O identificador para a próxima janela na cadeia é retornado por [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)e pode ser alterado em resposta a uma mensagem do [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) .

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

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[**CHANGECBCHAIN do WM \_**](wm-changecbchain.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Área de transferência](clipboard.md)
</dt> </dl>

 

