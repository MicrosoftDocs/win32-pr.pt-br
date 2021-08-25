---
title: EN_REQUESTRESIZE código de notificação (RichEdit. h)
description: Notifica uma janela pai do controle de edição rico que o conteúdo do controle é menor ou maior do que o tamanho da janela do controle. Um controle de edição rico envia esse código de notificação na forma de uma \_ mensagem de notificação do WM.
ms.assetid: 708c23b1-7b81-46f1-9595-46230693855d
keywords:
- EN_REQUESTRESIZE código de notificação Windows controles
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
ms.openlocfilehash: 9b15c21b180c2843eda7947946f6dc98d42caab1bad90383d6afe4a4f8002739
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047576"
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

## <a name="return-value"></a>Valor retornado

Este código de notificação não retorna um valor.

## <a name="remarks"></a>Comentários

Para dar suporte ao comportamento inferior de um controle de edição rico, a janela pai deve redimensionar o controle quando ele recebe esse código de notificação.

Para receber \_ códigos de notificação do en REQUESTRESIZE, especifique [**enm \_ REQUESTRESIZE**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize)
</dt> <dt>

[**notificação do WM \_**](wm-notify.md)
</dt> </dl>

 

 





