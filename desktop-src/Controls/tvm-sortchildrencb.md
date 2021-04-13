---
title: Mensagem de TVM_SORTCHILDRENCB (commctrl. h)
description: Classifica os itens de exibição em árvore usando uma função de retorno de chamada definida pelo aplicativo que compara os itens. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SortChildrenCB.
ms.assetid: 1669e576-5e57-49f6-8097-7d6547306014
keywords:
- Controles de TVM_SORTCHILDRENCB de mensagens do Windows
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
ms.openlocfilehash: 4b1dab4abbbc019a81d7a066c81dbb3537a0d80d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455889"
---
# <a name="tvm_sortchildrencb-message"></a>\_Mensagem TVM SORTCHILDRENCB

Classifica os itens de exibição em árvore usando uma função de retorno de chamada definida pelo aplicativo que compara os itens. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ SortChildrenCB**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Reservado. Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**TVSORTCB**](/windows/win32/api/commctrl/ns-commctrl-tvsortcb) . O membro **lpfnCompare** é o endereço da função de retorno de chamada definida pelo aplicativo, que é chamada durante a operação de classificação cada vez que a ordem relativa de dois itens de lista precisa ser comparada. Para obter mais informações sobre a função de retorno de chamada, consulte a descrição de **TVSORTCB**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





