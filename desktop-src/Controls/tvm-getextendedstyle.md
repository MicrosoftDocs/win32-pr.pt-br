---
title: Mensagem de TVM_GETEXTENDEDSTYLE (commctrl. h)
description: Recupera o estilo estendido para um controle de exibição de árvore. Envie essa mensagem explicitamente ou usando a macro TreeView \_ Extended.
ms.assetid: adc74cc5-e741-4966-bf49-a4b0c67e645a
keywords:
- Controles de TVM_GETEXTENDEDSTYLE de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 579a00e125389ff56c7ff93370ab71945598dba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824748"
---
# <a name="tvm_getextendedstyle-message-commctrlh"></a>Mensagem de TVM_GETEXTENDEDSTYLE (commctrl. h)

Recupera o estilo estendido para um controle de exibição de árvore. Envie essa mensagem explicitamente ou usando a macro [**TreeView \_ Extended**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getextendedstyle) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o valor do estilo estendido. Para obter mais informações sobre estilos, consulte [controle de exibição de árvore estilos estendidos](tree-view-control-window-extended-styles.md).

## <a name="remarks"></a>Comentários

Os estilos estendidos para um controle de exibição em árvore não têm nada a ver com os estilos estendidos usados com a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

