---
title: CBEN_INSERTITEM de notificação (Commctrl.h)
description: Enviado quando um novo item foi inserido no controle . Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: caf60156-10d2-4cfb-91c4-def6ee99c471
keywords:
- CBEN_INSERTITEM código de notificação Windows Controles
topic_type:
- apiref
api_name:
- CBEN_INSERTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a58c1f8b14f4983e2f7e7444a8110f0407220b0c5bc682cfc73f72bee078ab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413662"
---
# <a name="cben_insertitem-notification-code"></a>Código de notificação CBEN \_ INSERTITEM

Enviado quando um novo item foi inserido no controle . Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
CBEN_INSERTITEM

    pNMInfo = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) que contém informações sobre o código de notificação e o item que foi inserido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O aplicativo que está processando esse código de notificação deve retornar zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





