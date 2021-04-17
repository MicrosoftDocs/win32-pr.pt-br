---
title: TCN_SELCHANGING código de notificação (commctrl. h)
description: Notifica uma janela pai do controle guia que a guia selecionada atualmente está prestes a ser alterada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: ec7b1bd3-8932-4418-9eed-ecb7c748e4dd
keywords:
- TCN_SELCHANGING de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TCN_SELCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6ba7dcf25d243d9b42876425564fba0e01c803f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755420"
---
# <a name="tcn_selchanging-notification-code"></a>Código de notificação de SELCHANGING de TCN \_

Notifica uma janela pai do controle guia que a guia selecionada atualmente está prestes a ser alterada. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TCN_SELCHANGING 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **true** para impedir que a seleção seja alterada ou **false** para permitir que a seleção seja alterada.

## <a name="remarks"></a>Comentários

Para determinar a guia selecionada no momento, use a macro [**\_ getcurseal TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[SELCHANGE de TCN \_](tcn-selchange.md)
</dt> </dl>

 

 





