---
title: EN_STOPNOUNDO de notificação (Richedit.h)
description: Notifica a janela pai de um controle de edição rich que ocorreu uma ação para a qual o controle não pode alocar memória suficiente para manter o estado de desfazer. Um controle de edição rich envia esse código de notificação na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 5608f6dd-83dc-4712-b485-dd9bc17dea24
keywords:
- EN_STOPNOUNDO código de notificação Windows Controles
topic_type:
- apiref
api_name:
- EN_STOPNOUNDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e2bd22161f215e9544db08f845eb144fe94ec083b8a887a3db6fc46220d822d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047386"
---
# <a name="en_stopnoundo-notification-code"></a>Código de \_ notificação EN STOPNOUNDO

Notifica a janela pai de um controle de edição rich que ocorreu uma ação para a qual o controle não pode alocar memória suficiente para manter o estado de desfazer. Um controle de edição rich envia esse código de notificação na forma de uma [**mensagem WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_STOPNOUNDO

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Uma [**estrutura NMHDR.**](/windows/desktop/api/richedit/ns-richedit-nmhdr)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorne zero para continuar a **operação Desfazer.**

Retornar um valor não zero para interromper a **operação Desfazer.**

## <a name="remarks"></a>Comentários

A janela pai sempre receberá uma mensagem [**WM \_ NOTIFY**](wm-notify.md) para esse evento, não requer uma máscara de notificação enviada com [**EM \_ SETEVENTMASK**](em-seteventmask.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> <dt>

[**WM \_ NOTIFY**](wm-notify.md)
</dt> </dl>

 

 





