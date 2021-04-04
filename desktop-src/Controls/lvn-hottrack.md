---
title: LVN_HOTTRACK código de notificação (commctrl. h)
description: Enviado por um controle de exibição de lista quando o usuário move o mouse sobre um item. Este código de notificação é enviado somente por controles de exibição de lista que têm \_ o \_ estilo de exibição de lista estendida LVS ex TRACKSELECT. Ele é enviado na forma de uma mensagem de \_ notificação do WM.
ms.assetid: 6bbfe6b8-9b67-49e4-9481-65abe98608bb
keywords:
- LVN_HOTTRACK de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_HOTTRACK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c677b69fa21cdbe3680442304f6745cfb3a907de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824859"
---
# <a name="lvn_hottrack-notification-code"></a>Código de notificação do LVN \_ HOTTRACK

Enviado por um controle de exibição de lista quando o usuário move o mouse sobre um item. Este código de notificação é enviado somente por controles de exibição de lista que têm o estilo de exibição de lista estendida [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md) . Ele é enviado na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) .


```C++
LVN_HOTTRACK

    lpnmlv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMLISTVEIW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) que contém informações sobre este código de notificação. Os membros **iItem**, **iSubItem** e **ptAction** dessa estrutura contêm informações sobre o item. O aplicativo receptor pode modificar o membro **iItem** para especificar o item que será selecionado. Se **iItem** for definido como-1, nenhum item será selecionado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornar zero para permitir que o modo de exibição de lista execute seu processamento normal de faixa de seleção. Se o aplicativo retornar um zero diferente, o item não será selecionado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





