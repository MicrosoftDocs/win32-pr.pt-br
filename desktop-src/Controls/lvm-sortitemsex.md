---
title: Mensagem de LVM_SORTITEMSEX (commctrl. h)
description: Usa uma função de comparação definida pelo aplicativo para classificar os itens de um controle de exibição de lista. O índice de cada item é alterado para refletir a nova sequência. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SortItemsEx do ListView.
ms.assetid: eab2f6f5-68fd-4cb6-acf4-cb267ee40fdc
keywords:
- Controles de LVM_SORTITEMSEX de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SORTITEMSEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99e524b00cb5ff1260eb68e7d86e185e5ae60c75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008935"
---
# <a name="lvm_sortitemsex-message"></a>\_Mensagem SORTITEMSEX LVM

Usa uma função de comparação definida pelo aplicativo para classificar os itens de um controle de exibição de lista. O índice de cada item é alterado para refletir a nova sequência. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SortItemsEx do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitemsex) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor definido pelo aplicativo que é passado para a função de comparação.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma função de comparação definida pelo aplicativo. Ele é chamado durante a operação de classificação cada vez que a ordem relativa de dois itens de lista precisa ser comparada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

A função de comparação tem o seguinte formato:

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);  
```

Essa mensagem é semelhante ao [**LVM \_ SORTITEMS**](lvm-sortitems.md), exceto pelo tipo de informação passado para a função de comparação. Com o **LVM \_ SORTITEMSEX**, *lParam1* é o índice atual do primeiro item e *lParam2* é o índice atual do segundo item. Você pode enviar uma mensagem [**LVM \_ GETITEMTEXT**](lvm-getitemtext.md) para recuperar mais informações sobre um item, se necessário.

A função de comparação deve retornar um valor negativo se o primeiro item deve preceder o segundo, um valor positivo se o primeiro item deve seguir o segundo ou zero se os dois itens forem equivalentes.

> [!Note]  
> Durante o processo de classificação, o conteúdo da exibição de lista é instável. Se a função de retorno de chamada enviar todas as mensagens para o controle de exibição de lista, além do [**LVM \_ GETITEM**](lvm-getitem.md) ([**ListView \_ GETITEM**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), os resultados serão imprevisíveis.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





