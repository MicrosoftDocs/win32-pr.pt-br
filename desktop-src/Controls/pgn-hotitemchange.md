---
title: Mensagem de PGN_HOTITEMCHANGE (commctrl. h)
description: Notifica uma janela pai do controle de pager que o item quente (realçado) foi alterado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 0f59677c-0251-49f4-b909-6fac6d93f354
keywords:
- controles de Windows de mensagem de PGN_HOTITEMCHANGE
topic_type:
- apiref
api_name:
- PGN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6510eeb648ad883d04ccc0baf916223bb5209d110c2237ef3bf618d241c2ede
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830130"
---
# <a name="pgn_hotitemchange-message"></a>\_Mensagem PGN HOTITEMCHANGE

Notifica uma janela pai do controle de pager que o item quente (realçado) foi alterado. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
PGN_HOTITEMCHANGE

    pnmPGHotItem = (LPNMPGHOTITEM) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMPGHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem) que contém informações sobre este código de notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornar zero para realçar o item ou diferente de zero para evitar o realce.

## <a name="remarks"></a>Comentários

> [!Note]  
> Para usar esse código de notificação, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





