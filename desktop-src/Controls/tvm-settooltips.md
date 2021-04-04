---
title: Mensagem de TVM_SETTOOLTIPS (commctrl. h)
description: Define um controle de dica de ferramenta filho do controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetToolTips de TreeView.
ms.assetid: beb9a739-868e-46a8-95d9-9dc032c79dd4
keywords:
- Controles de TVM_SETTOOLTIPS de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efd9d5957a38d873993405a5283545472433e958
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085535"
---
# <a name="tvm_settooltips-message"></a>\_Mensagem TVM SETtooltips

Define um controle de dica de ferramenta filho do controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetToolTips de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settooltips) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador para um controle de dica de ferramenta.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador para o controle de dica de ferramenta definido anteriormente para o controle de exibição em árvore ou **NULL** se as dicas de ferramentas não foram usadas anteriormente.

## <a name="remarks"></a>Comentários

Quando criados, os controles de exibição de árvore criam automaticamente um controle de dica de ferramenta filho. Para impedir que um controle de exibição de árvore use dicas de ferramenta, crie o controle com o estilo [**\_ notooltips de TVs**](tree-view-control-window-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_GETtooltips TVM**](tvm-gettooltips.md)
</dt> </dl>

 

 





