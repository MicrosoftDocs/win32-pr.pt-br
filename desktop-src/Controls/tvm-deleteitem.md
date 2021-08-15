---
title: Mensagem de TVM_DELETEITEM (commctrl. h)
description: Remove um item e todos os seus filhos de um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ DeleteItem.
ms.assetid: 225420a5-6ded-4786-a080-2817aa5f66c9
keywords:
- controles de Windows de mensagem de TVM_DELETEITEM
topic_type:
- apiref
api_name:
- TVM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ef0165ffaf1f0f04b32cda43e21c97fed012ad6d61b32f8919612f8924f7c66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018684"
---
# <a name="tvm_deleteitem-message"></a>\_Mensagem TVM DELETEITEM

Remove um item e todos os seus filhos de um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteitem) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

**HTREEITEM** o identificador para o item a ser excluído. Se *lParam* for definido como TVI \_ root ou como **NULL**, todos os itens serão excluídos. Você também pode usar a macro [**TreeView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems) para excluir todos os itens.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Não é seguro excluir itens em resposta a uma notificação como [TVN \_ SELCHANGING](tvn-selchanging.md).

Depois que um item é excluído, seu identificador é inválido e não pode ser usado.

A janela pai recebe um código de notificação [TVN \_ DELETEITEM](tvn-deleteitem.md) quando cada item é removido.

Se o rótulo do item estiver sendo editado, a operação de edição será cancelada e a janela pai receberá o código de notificação [TVN \_ ENDLABELEDIT](tvn-endlabeledit.md) .

Se você excluir todos os itens de um controle de exibição de árvore que tem o estilo [**\_ NoScroll de TVs**](tree-view-control-window-styles.md) , os itens adicionados subsequentemente poderão não ser exibidos corretamente. Para obter mais informações, consulte [**TreeView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





