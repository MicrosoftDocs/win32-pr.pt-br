---
title: Código de notificação de EN_CHANGE (Rich Edit) (WinUser. h)
description: Notifica uma janela de host do controle de edição rico sem janela que ocorreu uma alteração. Um controle de edição rico envia esse código de notificação na forma de uma \_ mensagem de notificação do WM.
ms.assetid: 97C0D9F1-7D4E-409D-A4F6-E645475A8EEF
keywords:
- EN_CHANGE de código de notificação (Rich Edit) controles do Windows
topic_type:
- apiref
api_name:
- EN_CHANGE (rich edit control)
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ea615234aba881b2a8938b8e502b36acfa565fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918278"
---
# <a name="en_change-rich-edit-notification-code"></a>\_Código de notificação de alteração (Rich Edit)

Notifica uma janela de host do controle de edição rico sem janela que ocorreu uma alteração. Um controle de edição rico envia esse código de notificação na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
EN_CHANGE

    penChangeNotify = (CHANGENOTIFY *) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Uma estrutura [**CHANGENOTIFY**](/windows/desktop/api/Textserv/ns-textserv-changenotify) que especifica a alteração feita.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Este código de notificação não retorna um valor.

## <a name="remarks"></a>Comentários

Para receber \_ códigos de notificação de alteração, [**especifique enm \_ alteração**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>WinUser. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify)
</dt> </dl>

 

 





