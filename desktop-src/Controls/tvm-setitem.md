---
title: Mensagem de TVM_SETITEM (commctrl. h)
description: A \_ mensagem TVM SETITEM define alguns ou todos os atributos de um item de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SetItem.
ms.assetid: 28d288bf-a557-4fce-870c-ffa368ece5a9
keywords:
- Controles de TVM_SETITEM de mensagens do Windows
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
ms.openlocfilehash: 95750af3aa43a25f0ff4eae5533df5d9aef23537
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455224"
---
# <a name="tvm_setitem-message"></a>\_Mensagem TVM SETITEM

A mensagem **TVM \_ SETITEM** define alguns ou todos os atributos de um item de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contém os novos atributos de item. Com a [versão 4,71](common-control-versions.md) e posterior, você pode usar uma estrutura [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) em vez disso.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

O membro **hItem** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) ou [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) identifica o item, e o membro **Mask** especifica quais atributos definir.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVM \_ SETITEMW** (Unicode) e **TVM \_ setitema** (ANSI)<br/>                   |



 

 





