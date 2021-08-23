---
title: TVM_GETEXTENDEDSTYLE mensagem (Commctrl.h)
description: Recupera o estilo estendido para um controle de exibição de árvore. Envie essa mensagem explicitamente ou usando a \_ macro TreeView GetExtendedStyle.
ms.assetid: adc74cc5-e741-4966-bf49-a4b0c67e645a
keywords:
- TVM_GETEXTENDEDSTYLE controles Windows mensagem
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
ms.openlocfilehash: a93eb22b3dfdbe05365d28a7c93bfa9df3619796f9b4ae9ec603c74da252c5a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834196"
---
# <a name="tvm_getextendedstyle-message-commctrlh"></a>TVM_GETEXTENDEDSTYLE mensagem (Commctrl.h)

Recupera o estilo estendido para um controle de exibição de árvore. Envie essa mensagem explicitamente ou usando a macro [**\_ TreeView GetExtendedStyle.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getextendedstyle)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o valor do estilo estendido. Para obter mais informações sobre estilos, consulte Estilos estendidos do [controle de exibição de árvore.](tree-view-control-window-extended-styles.md)

## <a name="remarks"></a>Comentários

Os estilos estendidos para um controle de exibição de árvore não têm nada a ver com os estilos estendidos usados com a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou a [**função SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

