---
title: RBN_CHEVRONPUSHED código de notificação (commctrl. h)
description: Enviado por um controle rebar quando uma divisa é enviada por push. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 58aa2c9d-8ab6-46ee-b32f-5c04fb7afa84
keywords:
- RBN_CHEVRONPUSHED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- RBN_CHEVRONPUSHED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab28d992b6d4a617b7aa7ee144eb50aef3b0e834
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009348"
---
# <a name="rbn_chevronpushed-notification-code"></a>Código de notificação do RBN \_ CHEVRONPUSHED

Enviado por um controle rebar quando uma divisa é enviada por push. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
RBN_CHEVRONPUSHED

    lpnm = (NMREBARCHEVRON) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para a estrutura [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) da banda.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno para essa notificação não é usado.

## <a name="remarks"></a>Comentários

Quando um aplicativo recebe esse código de notificação, ele é responsável por exibir um menu pop-up com itens para cada ferramenta oculta. Use o membro **RC** da estrutura [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) para localizar a posição correta para o menu pop-up.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





