---
title: Mensagem de TVM_SETINSERTMARK (commctrl. h)
description: Define a marca de inserção em um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SetInsertMark.
ms.assetid: 35441807-406a-408c-ad89-6dd40c907e3c
keywords:
- Controles de TVM_SETINSERTMARK de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff5a9cc9b05e9cd7dc3281d778734bee1048ffd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824512"
---
# <a name="tvm_setinsertmark-message"></a>\_Mensagem TVM SETINSERTMARK

Define a marca de inserção em um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ SetInsertMark**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmark) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor **bool** que especifica se a marca de inserção é colocada antes ou depois do item especificado. Se esse argumento for diferente de zero, a marca de inserção será colocada após o item. Se esse argumento for zero, a marca de inserção será colocada antes do item.

</dd> <dt>

*lParam* 
</dt> <dd>

**HTREEITEM** que especifica em qual item a marca de inserção será colocada. Se esse argumento for **nulo**, a marca de inserção será removida.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="remarks"></a>Comentários

Em algumas circunstâncias, a marca de inserção pode aparecer em dois locais depois que um nó é expandido. Se você estiver usando marcas de inserção, é recomendável forçar uma atualização do controle depois de expandir um nó.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





