---
title: EN_LINK de notificação (Richedit.h)
description: Um controle de edição rich envia códigos de notificação EN LINK quando recebe várias mensagens, por exemplo, quando o usuário clica no mouse ou quando o ponteiro do mouse está sobre o texto que tem o efeito \_ \_ CFE LINK.
ms.assetid: 67f02908-957e-4d91-8a70-70399ce9cf2e
keywords:
- EN_LINK código de notificação Windows Controles
topic_type:
- apiref
api_name:
- EN_LINK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3398f79a94982a8b7c843747f38f16431cad6a061388367037d259cfe862d468
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047656"
---
# <a name="en_link-notification-code"></a>Código de \_ notificação DE LINK EN

Um controle de edição rich envia códigos de notificação EN LINK quando recebe várias mensagens, por exemplo, quando o usuário clica no mouse ou quando o ponteiro do mouse está sobre o texto que tem o efeito \_ **\_ CFE LINK.** Um controle de edição rich edit sem janela envia essa notificação usando o [**método ITextHost::TxNotify.**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) A janela pai do controle recebe esse código de notificação por meio de uma [**mensagem WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_LINK

    penLink = (ENLINK *) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A ID da janela recuperada chamando a [**função GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) com o valor \_ da ID gwL.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura ENLINK.**](/windows/desktop/api/Richedit/ns-richedit-enlink) A estrutura contém uma [**estrutura NMHDR,**](/windows/desktop/api/richedit/ns-richedit-nmhdr) informações sobre o código de notificação e uma estrutura [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) que indica o intervalo de caracteres que têm o efeito **\_ LINK do CFE.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorne zero para permitir que o controle continue com seu tratamento normal da mensagem.

Retornar um valor diferente de zero para impedir que o controle manipula a mensagem.

**Windows 8:** retornar **EN \_ LINK DO DEFAULT \_ \_ para** direcionar o controle de edição rich para executar a ação padrão.

## <a name="remarks"></a>Comentários

Para receber **códigos de \_ notificação de LINK** EN quando o link tiver o foco, especifique o sinalizador [**\_ ENM LINK**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem EM [**\_ SETEVENTMASK.**](em-seteventmask.md)

Se o link não tiver nenhum foco, para receber códigos de notificação **\_ EN LINK,** especifique o sinalizador **SES \_ NOFOCUSLINKNOTIFY** na máscara enviada com a [**mensagem EM \_ SETEDITSTYLE.**](em-seteditstyle.md)

Um controle de edição rich envia códigos de notificação **\_ EN LINK** quando recebe as seguintes mensagens enquanto o ponteiro do mouse está sobre o texto que tem o efeito **\_ CFE LINK:**

-   [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk)
-   [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)
-   [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)
-   [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)
-   [**WM \_ RBUTTONDBLCLK**](/windows/desktop/inputdev/wm-rbuttondblclk)
-   [**WM \_ RBUTTONDOWN**](/windows/desktop/inputdev/wm-rbuttondown)
-   [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)
-   [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor)

O **efeito LINK \_ do CFE** normalmente identifica um intervalo de texto que contém uma URL. Os aplicativos podem manipular o código de notificação en link alterando o ponteiro do mouse quando ele está sobre a URL ou iniciando um navegador para exibir o local \_ identificado pela URL.

Se você enviar a mensagem [**EM \_ AUTOURLDETECT**](em-autourldetect.md) para habilitar a detecção automática de URL, o controle de edição rich define automaticamente o efeito LINK do **CFE \_** para o texto modificado que ele identifica como uma URL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Charrange**](/windows/desktop/api/Richedit/ns-richedit-charrange)
</dt> <dt>

[**EM \_ AUTOURLDETECT**](em-autourldetect.md)
</dt> <dt>

[**ENLINK**](/windows/desktop/api/Richedit/ns-richedit-enlink)
</dt> <dt>

[**ITextRange2::SetURL**](/windows/desktop/api/Tom/nf-tom-itextrange2-seturl)
</dt> <dt>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> </dl>

 

