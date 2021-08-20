---
title: RB_GETDROPTARGET mensagem (Commctrl.h)
description: Recupera o ponteiro de interface IDropTarget de um controle de barra de rebar.
ms.assetid: f429c5d1-406b-47f0-a654-47cabccc1d0e
keywords:
- RB_GETDROPTARGET controles de Windows mensagem
topic_type:
- apiref
api_name:
- RB_GETDROPTARGET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5793d2192ef65f193ff27d40cc14660c90d067034d8c1304e1bde1a354a4f493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169606"
---
# <a name="rb_getdroptarget-message"></a>Mensagem \_ GETDROPTARGET do RB

Recupera o ponteiro de interface [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) de um controle de barra de rebar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para um [**ponteiro IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) que recebe o ponteiro da interface. É responsabilidade do chamador chamar [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) neste ponteiro quando ele não for mais necessário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno para essa mensagem não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

