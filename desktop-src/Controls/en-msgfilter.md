---
title: EN_MSGFILTER código de notificação (RichEdit. h)
description: Notifica uma janela pai do controle de edição rico de um evento de teclado ou de mouse no controle. Um controle de edição rico envia esse código de notificação na forma de uma \_ mensagem de notificação do WM.
ms.assetid: 96cf0047-baae-46cd-82e8-ab6f3f353260
keywords:
- EN_MSGFILTER de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_MSGFILTER
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40ddb3e9b1d5314e2e981b00f0e0ef8e22974242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085639"
---
# <a name="en_msgfilter-notification-code"></a>\_Código de notificação en MSGFILTER

Notifica uma janela pai do controle de edição rico de um evento de teclado ou de mouse no controle. Um controle de edição rico envia esse código de notificação na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
EN_MSGFILTER

    pMsgFilter = (MSGFILTER *) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Uma estrutura [**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) que contém informações sobre a mensagem do teclado ou do mouse. Se a janela pai modificar essa estrutura e retornar um valor diferente de zero, a mensagem modificada será processada em vez da original.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna zero se o controle deve processar o teclado ou o evento de mouse.

Retorne diferente de zero se o controle precisar ignorar o evento de teclado ou de mouse.

## <a name="remarks"></a>Comentários

Para receber \_ códigos de notificação do en MSGFILTER para eventos, especifique um ou mais dos seguintes sinalizadores na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .



| Sinalizador                                                                             | Significado                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------|
| [**ENM \_**](rich-edit-control-event-mask-flags.md)       | Para receber códigos de notificação para eventos de teclado.     |
| [**ENM \_ MOUSEEVENTS**](rich-edit-control-event-mask-flags.md)   | Para receber códigos de notificação para eventos de mouse.        |
| [**ENM \_ SCROLLEVENTS**](rich-edit-control-event-mask-flags.md) | Para receber códigos de notificação para um evento de roda do mouse. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter)
</dt> <dt>

[**notificação do WM \_**](wm-notify.md)
</dt> </dl>

 

 





