---
title: WM_POINTERROUTEDRELEASED mensagem
description: Enviado para todos os processos (configurados para encadeamento entre processos por meio de AddContentWithCrossProcessChaining e não está tratando atualmente a entrada de ponteiro) associados a uma ID de ponteiro específica, quando uma mensagem WM_POINTERUP é recebida no processo atual.
ms.assetid: B031ED80-6F1B-42A7-B4E2-55934E2C456C
keywords:
- WM_POINTERROUTEDRELEASED mensagens de entrada e notificações
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDRELEASED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 318134779d94824daef0b05903f45121665892fbcafbeb48589ef150f324d2b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611286"
---
# <a name="wm_pointerroutedreleased-message"></a>WM_POINTERROUTEDRELEASED mensagem

Enviado para todos os processos (configurados para encadeamento entre processos por meio de [**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) e não está tratando atualmente a entrada de ponteiro) associados a uma ID de ponteiro específica, quando uma [**mensagem WM_POINTERUP**](wm-pointerup.md) é recebida no processo atual.


```C++
#define WM_POINTERROUTEDRELEASED       0x0253
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não utilizado.

</dd> <dt>

*lParam* 
</dt> <dd>

Não utilizado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

NULO

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2016 somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mensagens](messages.md)
</dt> </dl>

 

