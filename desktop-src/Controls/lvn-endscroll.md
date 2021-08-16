---
title: LVN_ENDSCROLL mensagem (Commctrl.h)
description: Notifica a janela pai de um controle de exibição de lista quando uma operação de rolagem termina. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 2838dcd0-ac0f-48c7-94ba-dc36febedb94
keywords:
- LVN_ENDSCROLL controles Windows mensagem
topic_type:
- apiref
api_name:
- LVN_ENDSCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 308d0abc3c12170dbc14f5e8a67329ed226610baa7b00fd042a24ed67193e6df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915136"
---
# <a name="lvn_endscroll-message"></a>Mensagem LVN \_ ENDSCROLL

Notifica a janela pai de um controle de exibição de lista quando uma operação de rolagem termina. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_ENDSCROLL

    pnmLVScroll = (LPNMLVSCROLL) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) que contém a posição horizontal ou vertical de onde a operação de rolagem termina.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Valor de retorno não usado.

## <a name="remarks"></a>Comentários

> [!Note]  
> Para usar esse código de notificação, você deve fornecer um manifesto especificando Comclt32.dll versão 6.0. Para obter mais informações sobre manifestos, consulte [Habilitando estilos visuais.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





