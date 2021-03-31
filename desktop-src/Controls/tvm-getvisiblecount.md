---
title: Mensagem de TVM_GETVISIBLECOUNT (commctrl. h)
description: Obtém o número de itens que podem ser totalmente visíveis na janela do cliente de um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ GetVisibleCount.
ms.assetid: c3519543-3fb2-4ecf-ac01-905d0946cb1b
keywords:
- Controles de TVM_GETVISIBLECOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETVISIBLECOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1927d21741b109c5f00aa964b058dc0c34732529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918160"
---
# <a name="tvm_getvisiblecount-message"></a>\_Mensagem TVM GETVISIBLECOUNT

Obtém o número de itens que podem ser totalmente visíveis na janela do cliente de um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ GetVisibleCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getvisiblecount) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o número de itens que podem ser totalmente visíveis na janela do cliente do controle de exibição de árvore.

## <a name="remarks"></a>Comentários

O número de itens que podem ser totalmente visíveis pode ser maior que o número de itens no controle. O controle calcula esse valor dividindo a altura da janela do cliente pela altura de um item.

Observe que o valor de retorno é o número de itens que podem estar *totalmente* visíveis. Se você puder ver todos os 20 itens e parte de um item mais, o valor de retorno será 20.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





