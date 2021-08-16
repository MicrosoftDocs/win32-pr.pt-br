---
title: PGN_SCROLL código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de pager que a janela contida está prestes a ser rolada. Essa notificação é enviada na forma de uma mensagem de \_ notificação do WM.
ms.assetid: 3d40e75e-c445-4885-b807-8cfcb92cb2d9
keywords:
- PGN_SCROLL código de notificação Windows controles
topic_type:
- apiref
api_name:
- PGN_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 864903c73eeb611d1c748ec6a4d936192a1a27f22d3f37115af8879916286a8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830140"
---
# <a name="pgn_scroll-notification-code"></a>\_Código de notificação de rolagem PGN

Notifica uma janela pai do controle de pager que a janela contida está prestes a ser rolada. Essa notificação é enviada na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) .


```C++
PGN_SCROLL

    lpnms = (LPNMPGSCROLL) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMPGSCROLL**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll) que contém e recebe informações sobre o código de notificação. O membro **iDir** dessa estrutura indica a direção da rolagem. Os membros **iXpos** e **iYpos** contêm a posição horizontal e vertical da janela contida antes da rolagem. O membro **iScroll** contém o valor delta de rolagem padrão. Você pode modificar esse membro para um valor de rolagem diferente, se desejar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





