---
title: EN_PROTECTED código de notificação (RichEdit. h)
description: Notifica uma janela pai do controle de edição rico que o usuário está realizando uma ação que alteraria um intervalo de texto protegido. Um controle de edição rico envia esse código de notificação na forma de uma \_ mensagem de notificação do WM.
ms.assetid: 29c0cb51-675c-44b1-ad45-5f7140ca5675
keywords:
- EN_PROTECTED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_PROTECTED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1475053366a06f46b0c99514ade961f1a2998b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455233"
---
# <a name="en_protected-notification-code"></a>Código de notificação do EN \_ Protected

Notifica uma janela pai do controle de edição rico que o usuário está realizando uma ação que alteraria um intervalo de texto protegido. Um controle de edição rico envia esse código de notificação na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
EN_PROTECTED

    penProtected = (ENPROTECTED *) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Uma estrutura [**protegida**](/windows/desktop/api/Richedit/ns-richedit-enprotected) que contém informações sobre a mensagem que disparou o código de notificação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornar zero para permitir a operação.

Retornar um valor diferente de zero para impedir a operação.

## <a name="remarks"></a>Comentários

Se zero for retornado e os membros **msg**, **wParam** e **lParam** da estrutura [**protegida**](/windows/desktop/api/Richedit/ns-richedit-enprotected) forem alterados, o controle processará a mensagem revisada em vez da mensagem original.

Para receber códigos de notificação do EN \_ Protected, especifique [**enm \_ Protected**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .

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

[**PROTEGIDO**](/windows/desktop/api/Richedit/ns-richedit-enprotected)
</dt> <dt>

[**notificação do WM \_**](wm-notify.md)
</dt> </dl>

 

 





