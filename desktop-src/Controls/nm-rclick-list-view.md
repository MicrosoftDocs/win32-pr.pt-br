---
title: Código de notificação de NM_RCLICK (exibição de lista) (commctrl. h)
description: Enviado por um controle de exibição de lista quando o usuário clica em um item com o botão direito do mouse. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: dc7f97b3-4aec-4a8f-a87c-62cef5ba4c40
keywords:
- NM_RCLICK de código de notificação (exibição de lista) Windows controles
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f58ab6b2496c35bb4b95a3808afb7e58b961584b8b72d086933ad2c3281e6f29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018804"
---
# <a name="nm_rclick-list-view-notification-code"></a>\_Código de notificação nm RCLICK (exibição de lista)

Enviado por um controle de exibição de lista quando o usuário clica em um item com o botão direito do mouse. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
NM_RCLICK

    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

[Versão 4,71](common-control-versions.md). Ponteiro para uma estrutura [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) que contém informações adicionais sobre esta notificação. Os membros **iItem**, **iSubItem** e **ptAction** dessa estrutura contêm informações sobre o item.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornar zero para não permitir o processamento padrão ou zero para permitir o processamento padrão.

## <a name="remarks"></a>Comentários

O membro **iItem** de *lParam* só será válido se o ícone ou rótulo de primeira coluna tiver sido clicado. Para determinar qual item é selecionado quando um clique ocorre em outro lugar em uma linha, envie uma mensagem [**LVM \_ SUBITEMHITTEST**](lvm-subitemhittest.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





