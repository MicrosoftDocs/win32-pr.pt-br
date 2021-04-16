---
title: LVN_BEGINSCROLL código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista quando uma operação de rolagem é iniciada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 67123db1-118c-43d7-8511-12a3c4413958
keywords:
- LVN_BEGINSCROLL de código de notificação controles do Windows
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
ms.openlocfilehash: ae09a05525ac6e9f08d8cc7a0b7de6ef51329baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454695"
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

## <a name="return-value"></a>Retornar valor

Valor de retorno não usado.

## <a name="remarks"></a>Comentários

> [!Note]  
> Para usar esse código de notificação, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





