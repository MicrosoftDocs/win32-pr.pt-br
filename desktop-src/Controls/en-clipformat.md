---
title: EN_CLIPFORMAT código de notificação (RichEdit. h)
description: Notifica uma janela pai do controle de edição rico que ocorreu uma colagem com um formato de área de transferência específico. Um controle de edição rico sem janela envia essa notificação usando o método ITextHost TxNotify.
ms.assetid: 79FE1350-4D45-447B-B705-63E966AC7F0E
keywords:
- EN_CLIPFORMAT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_CLIPFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0430e8a4dba0b1a18f81f4e28ec67f2c93551cd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918275"
---
# <a name="en_clipformat-notification-code"></a>\_Código de notificação en CLIPFORMAT

Notifica uma janela pai do controle de edição rico que ocorreu uma colagem com um formato de área de transferência específico. Um controle de edição rico sem janela envia essa notificação usando o método [**ITextHost:: TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) .


```C++
EN_CLIPFORMAT

      pClipboardFmt = (CLIPBOARDFORMAT *) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A ID da janela recuperada chamando a função [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) com o \_ valor da ID GWL.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat) que contém informações sobre o formato da área de transferência.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é ignorado.

## <a name="remarks"></a>Comentários

Para receber \_ códigos de notificação do en CLIPFORMAT, especifique [**enm \_ CLIPFORMAT**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat)
</dt> </dl>

 

