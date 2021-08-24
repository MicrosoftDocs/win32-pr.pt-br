---
title: Mensagem de LVM_SORTITEMS (commctrl. h)
description: Usa uma função de comparação definida pelo aplicativo para classificar os itens de um controle de exibição de lista. O índice de cada item é alterado para refletir a nova sequência. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SortItems do ListView.
ms.assetid: ed3d5cec-69af-49a1-9cb7-eb5da1163071
keywords:
- controles de Windows de mensagem de LVM_SORTITEMS
topic_type:
- apiref
api_name:
- LVM_SORTITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a245e8236995d0d595c339b322140ee53ab5f84e83f1ecbd6b8ed47293e7dc7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119816386"
---
# <a name="lvm_sortitems-message"></a>\_Mensagem SORTITEMS LVM

Usa uma função de comparação definida pelo aplicativo para classificar os itens de um controle de exibição de lista. O índice de cada item é alterado para refletir a nova sequência. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SortItems do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor definido pelo aplicativo que é passado para a função de comparação.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para a função de comparação definida pelo aplicativo. A função de comparação é chamada durante a operação de classificação cada vez que a ordem relativa de dois itens de lista precisa ser comparada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

A função de comparação tem o seguinte formato:

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);
```

O parâmetro *lParam1* é o valor associado ao primeiro item que está sendo comparado e o parâmetro *lParam2* é o valor associado ao segundo item. Esses são os valores que foram especificados no membro **lParam** da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) dos itens quando eles foram inseridos na lista. O parâmetro *wParam* do [**ListView \_ SortItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems)é passado para a função de retorno de chamada como seu terceiro parâmetro.

A função de comparação deve retornar um valor negativo se o primeiro item deve preceder o segundo, um valor positivo se o primeiro item deve seguir o segundo ou zero se os dois itens forem equivalentes.

> [!Note]  
> Durante o processo de classificação, o conteúdo da exibição de lista é instável. Se a função de retorno de chamada enviar todas as mensagens para o controle de exibição de lista, além do [**LVM \_ GETITEM**](lvm-getitem.md) ([**ListView \_ GETITEM**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), os resultados serão imprevisíveis.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





