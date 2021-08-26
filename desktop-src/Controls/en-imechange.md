---
title: EN_IMECHANGE de notificação (Richedit.h)
description: Notifica o pai de um controle de edição rico de que o status de conversão do IME foi alterado.
ms.assetid: 2893e4ef-5904-4a57-95c5-3f6cfbb60d90
keywords:
- EN_IMECHANGE de notificação Windows Controles
topic_type:
- apiref
api_name:
- EN_IMECHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4974c4126606b8ed95ffa645778469b6fc897488533b81498347de1c1995e7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047676"
---
# <a name="en_imechange-notification-code"></a>Código de \_ notificação en IMECHANGE

Notifica o pai de um controle de edição rico de que o status de conversão do IME foi alterado. Esse código de notificação está *disponível apenas para* versões de idioma asiático do sistema operacional. Um controle de edição rich envia esse código de notificação na forma de uma [**mensagem WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
EN_IMECHANGE

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador do controle de edição rich. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.

</dd> <dt>

*lParam* 
</dt> <dd>

Lidar com o controle de edição rich.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse código de notificação retorna zero.

## <a name="remarks"></a>Comentários

Para receber códigos \_ de notificação en IMECHANGE, especifique [**ENM \_ IMECHANGE**](rich-edit-control-event-mask-flags.md) na máscara enviada com a [**mensagem EM \_ SETEVENTMASK.**](em-seteventmask.md)

> [!Note]  
> Esse código de notificação só tem suporte na versão da Ásia do Rich Edit 1.0. Não há suporte para ele em versões posteriores. Para obter informações sobre a compatibilidade de versões de edição rich com as várias versões do sistema, consulte [Sobre controles de edição rich](about-rich-edit-controls.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Outros recursos**
</dt> <dt>

[**Hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**Loword**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

