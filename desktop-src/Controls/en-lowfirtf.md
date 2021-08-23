---
title: EN_LOWFIRTF de notificação (Richedit.h)
description: Notifica a janela pai de um controle Microsoft Rich Edit de que uma palavra-chave RTF (Rich Text Format) sem suporte foi recebida. Um controle Rich Edit envia esse código de notificação na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 3b18320b-ebc3-44f2-a93c-e967a028c522
keywords:
- EN_LOWFIRTF de notificação Windows Controles
topic_type:
- apiref
api_name:
- EN_LOWFIRTF
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffafccf7fc52506ce72c6591ae9d4b5e3f5ee8855788267fbfae98497165e4ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576316"
---
# <a name="en_lowfirtf-notification-code"></a>Código \_ de notificação EN LOWFIRTF

Notifica a janela pai de um controle Microsoft Rich Edit de que uma palavra-chave RTF (Rich Text Format) sem suporte foi recebida. Um controle Rich Edit envia esse código de notificação na forma de uma [**mensagem WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_LOWFIRTF

    penLowfiRTF = (ENLOWFIRTF *) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

A [**estrutura ENLOWFIRTF.**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse código de notificação não retorna um valor.

## <a name="remarks"></a>Comentários

Para receber uma notificação EN LOWFIRTF, especifique o sinalizador ENM LOWFIRTF na máscara enviada com a \_ mensagem EM \_ [**\_ SETEVENTMASK.**](em-seteventmask.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho SP1\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**ENLOWFIRTF**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf)
</dt> <dt>

[**WM \_ NOTIFY**](wm-notify.md)
</dt> </dl>

 

 





