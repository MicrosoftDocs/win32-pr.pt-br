---
title: WM_POINTERROUTEDAWAY mensagem
description: Ocorre no processo que recebe a entrada quando a entrada do ponteiro é roteada para outro processo. AddContentWithCrossProcessChaining).
ms.assetid: 06F8152C-0DA0-4820-835E-07AD35B24310
keywords:
- Mensagens de entrada e notificações de WM_POINTERROUTEDAWAY mensagem
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDAWAY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: d6df21a5464aa44621c2eca760690806237f9e75a79c5f695d3df5b7604a6878
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964216"
---
# <a name="wm_pointerroutedaway-message"></a>WM_POINTERROUTEDAWAY mensagem

Ocorre no processo que recebe a entrada quando a entrada do ponteiro é roteada para outro processo.

Enviado quando a entrada do ponteiro faz a transição de um processo para outro no conteúdo configurado para encadeamento de processo cruzado ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).

Esta mensagem é enviada para o processo que recebe entrada de ponteiro no momento.


```C++
#define WM_POINTERROUTEDAWAY       0x0252
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

Essa mensagem não é enviada com uma mensagem [**WM_POINTERUP**](wm-pointerup.md) ou uma mensagem de [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2016 \[ somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mensagens](messages.md)
</dt> <dt>

[**WM_POINTERROUTEDTO**](wm-pointerroutedto.md)
</dt> </dl>

 

