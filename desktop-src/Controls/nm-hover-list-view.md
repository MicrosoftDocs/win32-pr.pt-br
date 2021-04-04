---
title: Código de notificação de NM_HOVER (exibição de lista) (commctrl. h)
description: Enviado por um controle de exibição de lista quando o mouse passa sobre um item. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 0d4a2eee-9c98-43d1-bc05-226d91c0480a
keywords:
- NM_HOVER de código de notificação (exibição de lista) controles do Windows
topic_type:
- apiref
api_name:
- NM_HOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e60606dfac73e13b0439ce861f37cb4ec941fda3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824160"
---
# <a name="nm_hover-list-view-notification-code"></a>\_Código de notificação de foco de nm (exibição de lista)

Enviado por um controle de exibição de lista quando o mouse passa sobre um item. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
NM_HOVER

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornar zero para permitir que o modo de exibição de lista processe o foco normalmente ou diferente de zero para impedir que o foco seja processado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





