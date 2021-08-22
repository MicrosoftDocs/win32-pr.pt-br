---
title: EN_CLIPFORMAT de notificação (Richedit.h)
description: Notifica a janela pai de um controle de edição rica de que ocorreu uma colar com um formato de área de transferência específico. Um controle de edição rich edit sem janela envia essa notificação usando o método TxNotify de ITextHost.
ms.assetid: 79FE1350-4D45-447B-B705-63E966AC7F0E
keywords:
- EN_CLIPFORMAT código de notificação Windows Controles
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
ms.openlocfilehash: 0f4ad87f1c05ac9f5461da8a4ee1d26295be0ae1baafd8991801efc0d90197a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437036"
---
# <a name="en_clipformat-notification-code"></a>Código de \_ notificação EN CLIPFORMAT

Notifica a janela pai de um controle de edição rica de que ocorreu uma colar com um formato de área de transferência específico. Um controle de edição rich edit sem janela envia essa notificação usando o [**método ITextHost::TxNotify.**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify)


```C++
EN_CLIPFORMAT

      pClipboardFmt = (CLIPBOARDFORMAT *) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A ID da janela recuperada chamando a [**função GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) com o valor \_ da ID gwL.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat) que contém informações sobre o formato da área de transferência.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

## <a name="remarks"></a>Comentários

Para receber códigos de notificação EN \_ CLIPFORMAT, especifique [**ENM \_ CLIPFORMAT**](rich-edit-control-event-mask-flags.md) na máscara enviada com a [**mensagem EM \_ SETEVENTMASK.**](em-seteventmask.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat)
</dt> </dl>

 

