---
title: WM_POINTERROUTEDTO mensagem
description: Enviado quando a entrada de ponteiro em andamento, para uma ID de ponteiro existente, faz a transição de um processo para outro em todo o conteúdo configurado para encadeamento entre processos (AddContentWithCrossProcessChaining).
ms.assetid: 163E2C31-4E29-4CBA-B079-1963D4762D7B
keywords:
- WM_POINTERROUTEDTO mensagens de entrada e notificações
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDTO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 9b7de7dd1affb9100a29613e3b4186d3d5bdaa32d853e683579fdcc62e7f981f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117695617"
---
# <a name="wm_pointerroutedto-message"></a>WM_POINTERROUTEDTO mensagem

Enviado quando a entrada de ponteiro em andamento, para uma ID de ponteiro existente, faz a transição de um processo para outro em todo o conteúdo configurado para encadeamento entre processos ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).

Essa mensagem é enviada para o processo que não está recebendo entrada de ponteiro no momento.


```C++
#define WM_POINTERROUTEDTO       0x0251
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

## <a name="remarks"></a>Comentários

Essa mensagem não é enviada quando uma [**WM_POINTERDOWN**](wm-pointerdown.md) é postada para uma nova ID de ponteiro em um processo diferente.

Uma [**WM_POINTERDOWN**](wm-pointerdown.md) mensagem não será enviada se uma **WM_POINTERROUTEDTO** for postada primeiro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2016 somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mensagens](messages.md)
</dt> <dt>

[**WM_POINTERROUTEDAWAY**](wm-pointerroutedaway.md)
</dt> </dl>

 

