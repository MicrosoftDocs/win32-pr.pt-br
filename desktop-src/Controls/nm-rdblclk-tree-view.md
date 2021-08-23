---
title: Código de notificação de NM_RDBLCLK (exibição em árvore) (commctrl. h)
description: Notifica o pai de um controle de exibição de árvore que o usuário clicou duas vezes com o botão direito do mouse dentro do controle. Essa notificação é enviada na forma de uma mensagem de \_ notificação do WM.
ms.assetid: eb1ae167-32cb-45d6-92e6-7bf5f7e46c2a
keywords:
- código de notificação de NM_RDBLCLK (exibição em árvore) Windows controles
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
ms.openlocfilehash: 4da45d7ac3363a5dc362ef6d34255531f71ce780075e8106fb9579126298a1e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826066"
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

## <a name="return-value"></a>Valor retornado

Retornar um valor diferente de zero para impedir o processamento padrão ou zero para permitir o processamento padrão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





