---
title: Mensagem de TVM_SETINSERTMARK (commctrl. h)
description: Define a marca de inserção em um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SetInsertMark.
ms.assetid: 35441807-406a-408c-ad89-6dd40c907e3c
keywords:
- controles de Windows de mensagem de TVM_SETINSERTMARK
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
ms.openlocfilehash: 0c3004395dcc7ea0b83af2fc2b7dae370c303228f79599215d5b6d264379b793
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875626"
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

## <a name="return-value"></a>Valor retornado

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="remarks"></a>Comentários

Em algumas circunstâncias, a marca de inserção pode aparecer em dois locais depois que um nó é expandido. Se você estiver usando marcas de inserção, é recomendável forçar uma atualização do controle depois de expandir um nó.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





