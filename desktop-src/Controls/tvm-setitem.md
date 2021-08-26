---
title: TVM_SETITEM mensagem (Commctrl.h)
description: A mensagem TVM SETITEM define alguns ou todos os atributos de um item de \_ exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SetItem.
ms.assetid: 28d288bf-a557-4fce-870c-ffa368ece5a9
keywords:
- TVM_SETITEM controles Windows mensagem
topic_type:
- apiref
api_name:
- TVM_SETITEM
- TVM_SETITEMA
- TVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9521bc67766dbb503fc205e966d6ce72e674a4050b6c0d237c885dcb4a8f4b68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913936"
---
# <a name="tvm_setitem-message"></a>Mensagem TVM \_ SETITEM

A **mensagem TVM \_ SETITEM** define alguns ou todos os atributos de um item de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ SetItem.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contém os novos atributos de item. Com [a versão 4.71](common-control-versions.md) e posterior, você pode usar uma [**estrutura TVITEMEX.**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="remarks"></a>Comentários

O **membro hItem** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) ou [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) identifica o item e o membro **de** máscara especifica quais atributos definir.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVM \_ SETITEMW** (Unicode) e **TVM \_ SETITEMA** (ANSI)<br/>                   |



 

 





