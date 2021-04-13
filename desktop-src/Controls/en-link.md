---
title: EN_LINK código de notificação (RichEdit. h)
description: Um controle de edição rico envia \_ códigos de notificação de link quando recebe várias mensagens, por exemplo, quando o usuário clica no mouse ou quando o ponteiro do mouse está sobre o texto que tem o \_ efeito de link CFE.
ms.assetid: 67f02908-957e-4d91-8a70-70399ce9cf2e
keywords:
- EN_LINK de código de notificação controles do Windows
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
ms.openlocfilehash: ec0eeb134804f671502d4cd3abbe2cb6995194af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455759"
---
# <a name="en_link-notification-code"></a>\_Código de notificação do link en

Um controle de edição rico envia \_ códigos de notificação de link quando recebe várias mensagens, por exemplo, quando o usuário clica no mouse ou quando o ponteiro do mouse está sobre o texto que tem o efeito de **\_ link CFE** . Um controle de edição rico sem janela envia essa notificação usando o método [**ITextHost:: TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) . A janela pai do controle recebe esse código de notificação por meio de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
EN_LINK

    penLink = (ENLINK *) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A ID da janela recuperada chamando a função [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) com o \_ valor da ID GWL.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura de [**ENlinks**](/windows/desktop/api/Richedit/ns-richedit-enlink) . A estrutura contém uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , informações sobre o código de notificação e uma estrutura [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) que indica o intervalo de caracteres que têm o efeito de **\_ link CFE** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna zero para permitir que o controle prossiga com seu tratamento normal da mensagem.

Retornar um valor diferente de zero para impedir que o controle trate a mensagem.

**Windows 8**: retornar **link en, por \_ \_ \_ padrão** , para direcionar o controle de edição rico para executar a ação padrão.

## <a name="remarks"></a>Comentários

Para receber códigos de notificação de **\_ link** quando o link tiver foco, especifique o sinalizador de [**\_ link enm**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .

Se o link não tiver foco, para receber os códigos de notificação de **\_ link** , especifique o sinalizador **\_ NOFOCUSLINKNOTIFY do ses** na máscara enviada com a mensagem em [**\_ seteditstyle**](em-seteditstyle.md) .

Um controle rich edit envia códigos de notificação de **\_ link** quando recebe as seguintes mensagens enquanto o ponteiro do mouse está sobre o texto que tem o efeito de **\_ link CFE** :

-   [**LBUTTONDBLCLK do WM \_**](/windows/desktop/inputdev/wm-lbuttondblclk)
-   [**LBUTTONDOWN do WM \_**](/windows/desktop/inputdev/wm-lbuttondown)
-   [**LBUTTONUP do WM \_**](/windows/desktop/inputdev/wm-lbuttonup)
-   [**admousemove do WM \_**](/windows/desktop/inputdev/wm-mousemove)
-   [**RBUTTONDBLCLK do WM \_**](/windows/desktop/inputdev/wm-rbuttondblclk)
-   [**RBUTTONDOWN do WM \_**](/windows/desktop/inputdev/wm-rbuttondown)
-   [**RBUTTONUP do WM \_**](/windows/desktop/inputdev/wm-rbuttonup)
-   [**WM \_ SETcursor**](/windows/desktop/menurc/wm-setcursor)

O efeito de **\_ link do CFE** normalmente identifica um intervalo de texto que contém uma URL. Os aplicativos podem manipular o \_ código de notificação do link en alterando o ponteiro do mouse quando ele está sobre a URL ou iniciando um navegador para exibir o local identificado pela URL.

Se você enviar a mensagem em [**\_ AUTOURLDETECT**](em-autourldetect.md) para habilitar a detecção automática de URL, o controle de edição rico definirá automaticamente o efeito de **\_ link CFE** para o texto modificado que ele identifica como uma URL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange)
</dt> <dt>

[**em \_ AUTOURLDETECT**](em-autourldetect.md)
</dt> <dt>

[**VINCULAR**](/windows/desktop/api/Richedit/ns-richedit-enlink)
</dt> <dt>

[**ITextRange2:: SetURL**](/windows/desktop/api/Tom/nf-tom-itextrange2-seturl)
</dt> <dt>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> </dl>

 

