---
title: Mensagem de TVM_SORTCHILDREN (commctrl. h)
description: Classifica os itens filho do item pai especificado em um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SortChildren.
ms.assetid: c18bcd5f-c083-46ee-873b-d3100b0d7b04
keywords:
- controles de Windows de mensagem de TVM_SORTCHILDREN
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
ms.openlocfilehash: f975814fadc5271c562e4e8e420c35dbb3450142bed797af83af73fdf81a55d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913796"
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

## <a name="return-value"></a>Valor retornado

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Esta mensagem alphabetizes os itens de árvore usando [**lstrcmpi**](/windows/desktop/api/winbase/nf-winbase-lstrcmpia) no nome do item. Você pode usar a mensagem [**TVM \_ SORTCHILDRENCB**](tvm-sortchildrencb.md) para personalizar o comportamento de ordenação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

