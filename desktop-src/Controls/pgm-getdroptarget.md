---
title: Mensagem de PGM_GETDROPTARGET (commctrl. h)
description: Recupera o ponteiro de interface IDropTarget de um controle de pager. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetDropTarget do pager.
ms.assetid: 6b548c30-2d32-4372-90e4-346a27dda218
keywords:
- Controles de PGM_GETDROPTARGET de mensagens do Windows
topic_type:
- apiref
api_name:
- PGM_GETDROPTARGET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b90f7f9667dd30a79b9345eec211a6ebfcd7a12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455540"
---
# <a name="pgm_getdroptarget-message"></a>\_Mensagem GETDROPTARGET do PGM

Recupera o ponteiro de interface [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) de um controle de pager. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetDropTarget do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para um ponteiro [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) que recebe o ponteiro de interface. É responsabilidade do chamador chamar [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) neste ponteiro quando ele não for mais necessário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor retornado para esta mensagem não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

