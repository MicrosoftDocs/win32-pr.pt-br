---
title: PGN_SCROLL código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de pager que a janela contida está prestes a ser rolada. Essa notificação é enviada na forma de uma mensagem de \_ notificação do WM.
ms.assetid: 3d40e75e-c445-4885-b807-8cfcb92cb2d9
keywords:
- PGN_SCROLL de código de notificação controles do Windows
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
ms.openlocfilehash: 62bc964b1a820fb0d5cd341e8909f36d5f6312ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085459"
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

## <a name="return-value"></a>Retornar valor

O valor de retorno é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





