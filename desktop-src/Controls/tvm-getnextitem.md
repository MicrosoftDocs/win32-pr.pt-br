---
title: Mensagem de TVM_GETNEXTITEM (commctrl. h)
description: Recupera o item de exibição de árvore que possui a relação especificada para um item especificado. Você pode enviar essa mensagem explicitamente usando a \_ macro TreeView GetNextItem.
ms.assetid: 505c713c-7728-4119-bc0e-482fe7e73193
keywords:
- Controles de TVM_GETNEXTITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETNEXTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3099af5e9abcd3e9c144cfc615a12dd2acb0332b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085329"
---
# <a name="tvm_getnextitem-message"></a>\_Mensagem TVM GETNEXTITEM

Recupera o item de exibição de árvore que possui a relação especificada para um item especificado. Você pode enviar essa mensagem explicitamente usando a macro [**TreeView \_ GetNextItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextitem) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Sinalizador que especifica o item a ser recuperado. Esse parâmetro pode ser um dos seguintes valores:



| Valor                                                                                                                                                                              | Significado                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVGN_CARET"></span><span id="tvgn_caret"></span><dl> <dt>**TVGN \_ circunflexo**</dt> </dl>                               | Recupera o item selecionado no momento. Você pode usar a [**macro \_ getSelect da TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselection) para enviar esta mensagem.<br/>                                                                                                                                                                          |
| <span id="TVGN_CHILD"></span><span id="tvgn_child"></span><dl> <dt>**TVGN \_ filho**</dt> </dl>                               | Recupera o primeiro item filho do item especificado pelo parâmetro *hItem* . Você pode usar a [**macro \_ GetChild do TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getchild) para enviar esta mensagem.<br/>                                                                                                                                          |
| <span id="TVGN_DROPHILITE"></span><span id="tvgn_drophilite"></span><dl> <dt>**TVGN \_ DROPHILITE**</dt> </dl>                | Recupera o item que é o destino de uma operação de arrastar e soltar. Você pode usar a macro [**TreeView \_ GetDropHilight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getdrophilight) para enviar esta mensagem.<br/>                                                                                                                                         |
| <span id="TVGN_FIRSTVISIBLE"></span><span id="tvgn_firstvisible"></span><dl> <dt>**TVGN \_ FIRSTVISIBLE**</dt> </dl>          | Recupera o primeiro item que está visível na janela de exibição em árvore. Você pode usar a macro [**TreeView \_ GetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getfirstvisible) para enviar esta mensagem.<br/>                                                                                                                                         |
| <span id="TVGN_LASTVISIBLE"></span><span id="tvgn_lastvisible"></span><dl> <dt>**TVGN \_ LASTVISIBLE**</dt> </dl>             | [Versão 4,71](common-control-versions.md). Recupera o último item expandido na árvore. Isso não recupera o último item visível na janela de exibição em árvore. Você pode usar a macro [**TreeView \_ GetLastVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlastvisible) para enviar esta mensagem.<br/>                                            |
| <span id="TVGN_NEXT"></span><span id="tvgn_next"></span><dl> <dt>**TVGN \_ próximo**</dt> </dl>                                  | Recupera o próximo item irmão. Você pode usar a macro [**TreeView \_ GetNextSibling**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextsibling) para enviar esta mensagem.<br/>                                                                                                                                                                            |
| <span id="TVGN_NEXTSELECTED"></span><span id="tvgn_nextselected"></span><dl> <dt>**TVGN \_ NEXTSELECTED**</dt> </dl>          | **Windows Vista e posterior.** Recupera o próximo item selecionado. Você pode usar a macro [**TreeView \_ GetNextSelected**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextselected) para enviar esta mensagem.<br/>                                                                                                                                            |
| <span id="TVGN_NEXTVISIBLE"></span><span id="tvgn_nextvisible"></span><dl> <dt>**TVGN \_ NEXTVISIBLE**</dt> </dl>             | Recupera o próximo item visível que segue o item especificado. O item especificado deve estar visível. Use a mensagem [**TVM \_ GETITEMRECT**](tvm-getitemrect.md) para determinar se um item está visível. Você pode usar a macro [**TreeView \_ GetNextVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextvisible) para enviar esta mensagem.<br/>   |
| <span id="TVGN_PARENT"></span><span id="tvgn_parent"></span><dl> <dt>**TVGN \_ pai**</dt> </dl>                            | Recupera o pai do item especificado. Você pode usar a macro do [**TreeView \_ GetParent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getparent) para enviar esta mensagem.<br/>                                                                                                                                                                           |
| <span id="TVGN_PREVIOUS"></span><span id="tvgn_previous"></span><dl> <dt>**TVGN \_ anterior**</dt> </dl>                      | Recupera o item irmão anterior. Você pode usar a macro [**TreeView \_ GetPrevSibling**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevsibling) para enviar esta mensagem.<br/>                                                                                                                                                                        |
| <span id="TVGN_PREVIOUSVISIBLE"></span><span id="tvgn_previousvisible"></span><dl> <dt>**TVGN \_ PREVIOUSVISIBLE**</dt> </dl> | Recupera o primeiro item visível que precede o item especificado. O item especificado deve estar visível. Use a mensagem [**TVM \_ GETITEMRECT**](tvm-getitemrect.md) para determinar se um item está visível. Você pode usar a macro [**TreeView \_ GetPrevVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevvisible) para enviar esta mensagem.<br/> |
| <span id="TVGN_ROOT"></span><span id="tvgn_root"></span><dl> <dt>**\_raiz TVGN**</dt> </dl>                                  | Recupera o primeiro item do controle de exibição de árvore. Você pode usar a [**macro \_ GetRoot do TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getroot) para enviar esta mensagem. <br/>                                                                                                                                                       |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador para um item.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador para o item, se for bem-sucedido. Na maioria dos casos, a mensagem retorna um valor **nulo** para indicar um erro. Consulte a seção comentários para obter detalhes.

## <a name="remarks"></a>Comentários

Essa mensagem retornará **NULL** se o item que está sendo recuperado for o nó raiz da árvore. Por exemplo, se você usar essa mensagem com o \_ sinalizador pai TVGN em um filho de primeiro nível do nó raiz da exibição de árvore, a mensagem retornará **NULL**.

Você também pode usar uma destas macros relacionadas:



|                                                               |
|---------------------------------------------------------------|
| [**TreeView \_ GetChild**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getchild)               |
| [**\_GetDropHilight TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getdrophilight)   |
| [**\_GetFirstVisible TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getfirstvisible) |
| [**\_GetLastVisible TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlastvisible)   |
| [**\_GetNextSibling TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextsibling)   |
| [**\_GetNextVisible TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextvisible)   |
| [**TreeView \_ GetParent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getparent)             |
| [**\_GetPrevSibling TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevsibling)   |
| [**\_GetPrevVisible TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevvisible)   |
| [**TreeView \_ GetRoot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getroot)                 |
| [**Getseleções de TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselection)       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





