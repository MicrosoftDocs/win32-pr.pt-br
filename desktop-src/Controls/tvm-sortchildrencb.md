---
title: TVM_SORTCHILDRENCB mensagem (Commctrl.h)
description: Classifica itens de exibição de árvore usando uma função de retorno de chamada definida pelo aplicativo que compara os itens. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SortChildrenCB.
ms.assetid: 1669e576-5e57-49f6-8097-7d6547306014
keywords:
- TVM_SORTCHILDRENCB controles de Windows mensagem
topic_type:
- apiref
api_name:
- TVM_SORTCHILDRENCB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45f0ec311cc5ce0f972f3363ea97cd42874ca85807bf852296de0283fccc95c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669472"
---
# <a name="tvm_sortchildrencb-message"></a>Mensagem TVM \_ SORTCHILDRENCB

Classifica itens de exibição de árvore usando uma função de retorno de chamada definida pelo aplicativo que compara os itens. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ SortChildrenCB.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Reservado. Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura TVSORTCB.**](/windows/win32/api/commctrl/ns-commctrl-tvsortcb) O **membro lpfnCompare** é o endereço da função de retorno de chamada definida pelo aplicativo, que é chamada durante a operação de classificação sempre que a ordem relativa de dois itens de lista precisa ser comparada. Para obter mais informações sobre a função de retorno de chamada, consulte a descrição de **TVSORTCB.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





