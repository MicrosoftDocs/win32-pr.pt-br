---
title: Código de notificação de NM_RDBLCLK (exibição em árvore) (commctrl. h)
description: Notifica o pai de um controle de exibição de árvore que o usuário clicou duas vezes com o botão direito do mouse dentro do controle. Essa notificação é enviada na forma de uma mensagem de \_ notificação do WM.
ms.assetid: eb1ae167-32cb-45d6-92e6-7bf5f7e46c2a
keywords:
- Código de notificação de NM_RDBLCLK (exibição de árvore) controles do Windows
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ef5b4f1dbaf1031c995028028cc0b44e544f5f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086090"
---
# <a name="nm_rdblclk-tree-view-notification-code"></a>\_Código de notificação nm RDBLCLK (exibição em árvore)

Notifica o pai de um controle de exibição de árvore que o usuário clicou duas vezes com o botão direito do mouse dentro do controle. Essa notificação é enviada na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) .


```C++
NM_RDBLCLK

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornar um valor diferente de zero para impedir o processamento padrão ou zero para permitir o processamento padrão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





