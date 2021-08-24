---
title: EN_MSGFILTER de notificação (Richedit.h)
description: Notifica a janela pai de um controle de edição de um evento de teclado ou mouse no controle . Um controle de edição rich envia esse código de notificação na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 96cf0047-baae-46cd-82e8-ab6f3f353260
keywords:
- EN_MSGFILTER código de notificação Windows Controles
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
ms.openlocfilehash: 87d2cbe47af3d74deb4795946d58871b4729118db0e839027e78e05976ebf855
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436706"
---
# <a name="en_msgfilter-notification-code"></a>Código de \_ notificação EN MSGFILTER

Notifica a janela pai de um controle de edição de um evento de teclado ou mouse no controle . Um controle de edição rich envia esse código de notificação na forma de uma [**mensagem WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_MSGFILTER

    pMsgFilter = (MSGFILTER *) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Uma [**estrutura MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) que contém informações sobre o teclado ou a mensagem do mouse. Se a janela pai modificar essa estrutura e retornar um valor diferente de zero, a mensagem modificada será processada em vez da original.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará zero se o controle deve processar o evento do teclado ou do mouse.

Retornará algo além de zero se o controle ignorar o evento do teclado ou do mouse.

## <a name="remarks"></a>Comentários

Para receber códigos de notificação EN MSGFILTER para eventos, especifique um ou mais dos sinalizadores a seguir na máscara enviada com a \_ [**mensagem EM \_ SETEVENTMASK.**](em-seteventmask.md)



| Sinalizador                                                                             | Significado                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------|
| [**ENM \_ KEYEVENTS**](rich-edit-control-event-mask-flags.md)       | Para receber códigos de notificação para eventos de teclado.     |
| [**ENM \_ MOUSEEVENTS**](rich-edit-control-event-mask-flags.md)   | Para receber códigos de notificação para eventos do mouse.        |
| [**ENM \_ SCROLLEVENTS**](rich-edit-control-event-mask-flags.md) | Para receber códigos de notificação para um evento de roda do mouse. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter)
</dt> <dt>

[**WM \_ NOTIFY**](wm-notify.md)
</dt> </dl>

 

 





