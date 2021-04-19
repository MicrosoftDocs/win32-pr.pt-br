---
title: Estados do item de controle de Tree-View (CommCtrl. h)
description: Esta seção lista os sinalizadores de estado do item usados para indicar o estado de um item em um controle de exibição de árvore.
ms.assetid: 5b11d575-6dfd-47a8-b959-b19aaeeca70e
topic_type:
- apiref
api_name:
- TVIS_BOLD
- TVIS_CUT
- TVIS_DROPHILITED
- TVIS_EXPANDED
- TVIS_EXPANDEDONCE
- TVIS_EXPANDPARTIAL
- TVIS_SELECTED
- TVIS_OVERLAYMASK
- TVIS_STATEIMAGEMASK
- TVIS_USERMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef4a19306855b7f38d03aa00323b26407f108bfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769026"
---
# <a name="tree-view-control-item-states"></a>Tree-View Estados de item de controle

Esta seção lista os sinalizadores de estado do item usados para indicar o estado de um item em um controle de exibição de árvore.



| Constante                                                                                                                                                                        | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVIS_BOLD"></span><span id="tvis_bold"></span><dl> <dt>**TVIS \_ bold**</dt> </dl>                               | O item está em negrito.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_CUT"></span><span id="tvis_cut"></span><dl> <dt>**TVIS \_ recortar**</dt> </dl>                                  | O item é selecionado como parte de uma operação de recortar e colar. <br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TVIS_DROPHILITED"></span><span id="tvis_drophilited"></span><dl> <dt>**TVIS \_ DROPHILITED**</dt> </dl>          | O item é selecionado como um destino de arrastar e soltar.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_EXPANDED"></span><span id="tvis_expanded"></span><dl> <dt>**TVIS \_ expandido**</dt> </dl>                   | A lista de itens filhos do item está expandida no momento; ou seja, os itens filho são visíveis. Esse valor se aplica somente a itens pai.<br/>                                                                                                                                                                                                                                                                                                                  |
| <span id="TVIS_EXPANDEDONCE"></span><span id="tvis_expandedonce"></span><dl> <dt>**TVIS \_ EXPANDEDONCE**</dt> </dl>       | A lista de itens filho do item foi expandida pelo menos uma vez. Os códigos de notificação [TVN \_ doexpanding](tvn-itemexpanding.md) e TVN item- [ \_ Expanded](tvn-itemexpanded.md) não são gerados para itens pai que têm esse estado definido em resposta a uma mensagem de [**\_ expansão TVM**](tvm-expand.md) . Usar TVE \_ Collapse e TVE \_ COLLAPSERESET com **TVM \_ Expand** fará com que esse Estado seja redefinido. Esse valor se aplica somente a itens pai. <br/> |
| <span id="TVIS_EXPANDPARTIAL"></span><span id="tvis_expandpartial"></span><dl> <dt>**TVIS \_ EXPANDPARTIAL**</dt> </dl>    | **Versão 4,70**. Um item de exibição de árvore parcialmente expandido. Nesse estado, alguns, mas não todos, os itens filho são visíveis e o símbolo de adição do item pai é exibido. <br/>                                                                                                                                                                                                                                                                              |
| <span id="TVIS_SELECTED"></span><span id="tvis_selected"></span><dl> <dt>**TVIS \_ selecionado**</dt> </dl>                   | O item está selecionado. Sua aparência depende de se ele tem o foco. O item será desenhado usando as cores do sistema para seleção. <br/>                                                                                                                                                                                                                                                                                                              |
| <span id="TVIS_OVERLAYMASK"></span><span id="tvis_overlaymask"></span><dl> <dt>**TVIS \_ OVERLAYMASK**</dt> </dl>          | Máscara para os bits usados para especificar o índice de imagem de sobreposição do item.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_STATEIMAGEMASK"></span><span id="tvis_stateimagemask"></span><dl> <dt>**TVIS \_ STATEIMAGEMASK**</dt> </dl> | Máscara para os bits usados para especificar o índice de imagem de estado do item.<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_USERMASK"></span><span id="tvis_usermask"></span><dl> <dt>**usermask TVIS \_**</dt> </dl>                   | O mesmo que **TVIS \_ STATEIMAGEMASK**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="remarks"></a>Comentários

Quando você define ou recupera um índice de imagem de sobreposição de um item ou um índice de imagem de estado, você deve especificar as seguintes máscaras no membro **stateMask** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) :

-   **TVIS \_ OVERLAYMASK**
-   **TVIS \_ STATEIMAGEMASK**
-   **usermask TVIS \_**

Esses valores também podem ser usados para mascarar os bits de estado que não são de interesse.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





