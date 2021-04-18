---
title: WM_POINTERROUTEDRELEASED mensagem
description: Enviado a todos os processos (configurados para encadeamento de processo cruzado por meio de AddContentWithCrossProcessChaining e não manipulando a entrada de ponteiro), já associados a uma ID de ponteiro específica, quando uma mensagem de WM_POINTERUP é recebida no processo atual.
ms.assetid: B031ED80-6F1B-42A7-B4E2-55934E2C456C
keywords:
- Mensagens de entrada e notificações de WM_POINTERROUTEDRELEASED mensagem
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
ms.openlocfilehash: 8e24a0df1a2bbdf2b0a9df97057686aa6045eff8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369629"
---
# <a name="wm_pointerroutedreleased-message"></a>WM_POINTERROUTEDRELEASED mensagem

Enviado a todos os processos (configurados para encadeamento de processo cruzado por meio de [**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) e não manipulando a entrada de ponteiro), já associados a uma ID de ponteiro específica, quando uma mensagem de [**WM_POINTERUP**](wm-pointerup.md) é recebida no processo atual.


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

## <a name="return-value"></a>Retornar valor

NULO

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mensagens](messages.md)
</dt> </dl>

 

