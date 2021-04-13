---
title: Mensagem de TVM_GETTOOLTIPS (commctrl. h)
description: Recupera o identificador para o controle ToolTip filho usado por um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetToolTips do TreeView.
ms.assetid: 65e8189e-ae3e-4268-b1ed-bb0d88f2cbe3
keywords:
- Controles de TVM_GETTOOLTIPS de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305aaa05df5b72ffde709e4cf3b3e06d47c43448
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454873"
---
# <a name="tvm_gettooltips-message"></a>\_Mensagem TVM GETtooltips

Recupera o identificador para o controle ToolTip filho usado por um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetToolTips do TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettooltips) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador para o controle ToolTip filho ou **NULL** se o controle não estiver usando dicas de ferramenta.

## <a name="remarks"></a>Comentários

Quando criados, os controles de exibição de árvore criam automaticamente um controle de dica de ferramenta filho. Para fazer com que um controle de exibição em árvore não use dicas de ferramenta, crie o controle com o estilo [**\_ notooltips de TVs**](tree-view-control-window-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TVM \_ SETtooltip**](tvm-settooltips.md)
</dt> </dl>

 

 





