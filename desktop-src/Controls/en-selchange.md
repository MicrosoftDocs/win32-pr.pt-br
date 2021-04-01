---
title: EN_SELCHANGE código de notificação (RichEdit. h)
description: Notifica uma janela pai do controle de edição rico que a seleção atual foi alterada. Um controle de edição rico envia esse código de notificação na forma de uma \_ mensagem de notificação do WM.
ms.assetid: 53d47b53-a73c-4652-889c-2374f8e99382
keywords:
- EN_SELCHANGE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_SELCHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79dfcf951f88fa1e10f4723bd9843421f0e20ae5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645032"
---
# <a name="en_selchange-notification-code"></a>\_Código de notificação en SELCHANGE

Notifica uma janela pai do controle de edição rico que a seleção atual foi alterada. Um controle de edição rico envia esse código de notificação na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
EN_SELCHANGE

    pSelChange = (SELCHANGE *) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Uma estrutura [**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) que recebe informações sobre a seleção.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Este código de notificação não retorna um valor.

## <a name="remarks"></a>Comentários

Para receber \_ códigos de notificação do en SELCHANGE, especifique [**enm \_ SELCHANGE**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .

Esse código de notificação é enviado quando a posição do cursor é alterada e nenhum texto é selecionado (a seleção está vazia). A posição do cursor pode ser alterada quando o usuário clica no mouse, digita ou pressiona uma tecla de direção.

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

[**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange)
</dt> <dt>

[**notificação do WM \_**](wm-notify.md)
</dt> </dl>

 

 





