---
title: LVN_BEGINSCROLL código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista quando uma operação de rolagem é iniciada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 67123db1-118c-43d7-8511-12a3c4413958
keywords:
- LVN_BEGINSCROLL código de notificação Windows controles
topic_type:
- apiref
api_name:
- LVN_BEGINSCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e416aee093ed6526d85d81361e2774b963572de73ce84c21105f19d1675968f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915216"
---
# <a name="lvn_beginscroll-notification-code"></a>Código de notificação do LVN \_ BEGINSCROLL

Notifica uma janela pai do controle de exibição de lista quando uma operação de rolagem é iniciada. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
LVN_BEGINSCROLL

    pnmLVScroll = (LPNMLVSCROLL) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) que contém a posição horizontal ou vertical de onde a operação de rolagem é iniciada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Valor de retorno não usado.

## <a name="remarks"></a>Comentários

> [!Note]  
> Para usar esse código de notificação, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





