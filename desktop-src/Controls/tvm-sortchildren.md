---
title: Mensagem de TVM_SORTCHILDREN (commctrl. h)
description: Classifica os itens filho do item pai especificado em um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SortChildren.
ms.assetid: c18bcd5f-c083-46ee-873b-d3100b0d7b04
keywords:
- Controles de TVM_SORTCHILDREN de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SORTCHILDREN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 341591c31accb4aab0b49f611359a93ec99c0cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009701"
---
# <a name="tvm_sortchildren-message"></a>\_Mensagem TVM SORTCHILDREN

Classifica os itens filho do item pai especificado em um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ SortChildren**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildren) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica se a classificação é recursiva. Defina *wParam* como **true** para classificar todos os níveis de itens filho abaixo do item pai. Caso contrário, somente os filhos imediatos do pai serão classificados.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador para o item pai cujos itens filho devem ser classificados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Esta mensagem alphabetizes os itens de árvore usando [**lstrcmpi**](/windows/desktop/api/winbase/nf-winbase-lstrcmpia) no nome do item. Você pode usar a mensagem [**TVM \_ SORTCHILDRENCB**](tvm-sortchildrencb.md) para personalizar o comportamento de ordenação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

