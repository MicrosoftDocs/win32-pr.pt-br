---
title: Mensagem de RBN_AUTOBREAK (commctrl. h)
description: Notifica o pai de um rebar de que uma quebra aparecerá na barra. O pai determina se a interrupção deve ser feita. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: b7a63027-6cfa-4d5a-9ea6-fdd8b4fb6864
keywords:
- Controles de RBN_AUTOBREAK de mensagens do Windows
topic_type:
- apiref
api_name:
- RBN_AUTOBREAK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d614277d89578cb66e528ba16656ed55681ebbcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824791"
---
# <a name="rbn_autobreak-message"></a>\_Mensagem de quebra automática de RBN

Notifica o pai [de um rebar](rebar-controls.md) de que uma quebra aparecerá na barra. O pai determina se a interrupção deve ser feita. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
RBN_AUTOBREAK

    pnmRebarAutoBreak = (LPNMREBARAUTOBREAK) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) que contém informações sobre o código de notificação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno para essa notificação não é usado.

## <a name="remarks"></a>Comentários

O valor no membro **fAutoBreak** da estrutura [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) indica se uma interrupção deve ocorrer no Rebar.

Para usar esse código de notificação, especifique Comctl32.dll versão 6 no manifesto. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





