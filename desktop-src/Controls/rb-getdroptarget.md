---
title: Mensagem de RB_GETDROPTARGET (commctrl. h)
description: Recupera o ponteiro de interface IDropTarget de um controle rebar.
ms.assetid: f429c5d1-406b-47f0-a654-47cabccc1d0e
keywords:
- Controles de RB_GETDROPTARGET de mensagens do Windows
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
ms.openlocfilehash: 55b7960cc13230a2715348bc55e5e65de6f72e5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455531"
---
# <a name="rb_getdroptarget-message"></a>\_Mensagem GETDROPTARGET RB

Recupera o ponteiro de interface [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) de um controle rebar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

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



 

