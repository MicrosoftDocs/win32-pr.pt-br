---
title: WM_POINTERROUTEDTO mensagem
description: Enviado quando entrada de ponteiro contínua, para uma ID de ponteiro existente, faz a transição de um processo para outro em todo o conteúdo configurado para AddContentWithCrossProcessChaining (encadeamento de processo cruzado).
ms.assetid: 163E2C31-4E29-4CBA-B079-1963D4762D7B
keywords:
- Mensagens de entrada e notificações de WM_POINTERROUTEDTO mensagem
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
ms.openlocfilehash: 7658aeef77a0f7e19f2449213e9332b4e60c9450
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369492"
---
# <a name="wm_pointerroutedto-message"></a>WM_POINTERROUTEDTO mensagem

Enviado quando entrada de ponteiro contínua, para uma ID de ponteiro existente, faz a transição de um processo para outro em todo o conteúdo configurado para [**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)(encadeamento de processo cruzado).

Esta mensagem é enviada para o processo que não está recebendo entrada de ponteiro no momento.


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

## <a name="return-value"></a>Retornar valor

NULO

## <a name="remarks"></a>Comentários

Essa mensagem não é enviada quando uma mensagem de [**WM_POINTERDOWN**](wm-pointerdown.md) é postada para uma nova ID de ponteiro em um processo diferente.

Uma mensagem de [**WM_POINTERDOWN**](wm-pointerdown.md) não será enviada se uma mensagem de **WM_POINTERROUTEDTO** for postada primeiro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mensagens](messages.md)
</dt> <dt>

[**WM_POINTERROUTEDAWAY**](wm-pointerroutedaway.md)
</dt> </dl>

 

