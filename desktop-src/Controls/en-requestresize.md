---
title: EN_REQUESTRESIZE código de notificação (RichEdit. h)
description: Notifica uma janela pai do controle de edição rico que o conteúdo do controle é menor ou maior do que o tamanho da janela do controle. Um controle de edição rico envia esse código de notificação na forma de uma \_ mensagem de notificação do WM.
ms.assetid: 708c23b1-7b81-46f1-9595-46230693855d
keywords:
- EN_REQUESTRESIZE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60214d8902297eb7cd77ded481b0604929e7adb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085828"
---
# <a name="en_requestresize-notification-code"></a>\_Código de notificação en REQUESTRESIZE

Notifica uma janela pai do controle de edição rico que o conteúdo do controle é menor ou maior do que o tamanho da janela do controle. Um controle de edição rico envia esse código de notificação na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
EN_REQUESTRESIZE

    pReqResize = (REQRESIZE *) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Uma estrutura [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) que recebe o tamanho solicitado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Este código de notificação não retorna um valor.

## <a name="remarks"></a>Comentários

Para dar suporte ao comportamento inferior de um controle de edição rico, a janela pai deve redimensionar o controle quando ele recebe esse código de notificação.

Para receber \_ códigos de notificação do en REQUESTRESIZE, especifique [**enm \_ REQUESTRESIZE**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .

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

[**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize)
</dt> <dt>

[**notificação do WM \_**](wm-notify.md)
</dt> </dl>

 

 





