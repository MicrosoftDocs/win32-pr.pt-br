---
title: Mensagem de LB_GETCURSEL (WinUser. h)
description: Obtém o índice do item selecionado no momento, se houver, em uma caixa de listagem de seleção única.
ms.assetid: 39ab7f77-6c8e-45a4-aad4-47eba0a11a11
keywords:
- controles de Windows de mensagem de LB_GETCURSEL
topic_type:
- apiref
api_name:
- LB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d67a060669d48a9ab020540c78ece395504c9f0b7e36807e3ac59daf216ea395
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085516"
---
# <a name="lb_getcursel-message"></a>\_Mensagem GETcurseal de lb

Obtém o índice do item selecionado no momento, se houver, em uma caixa de listagem de seleção única.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Em uma caixa de listagem de seleção única, o valor de retorno é o índice de base zero do item selecionado no momento. Se não houver nenhuma seleção, o valor de retorno será um erro de LB \_ .

## <a name="remarks"></a>Comentários

Para recuperar os índices dos itens selecionados em uma caixa de listagem de seleção múltipla, use a [**mensagem \_ GETSELITEMS de lb**](lb-getselitems.md) . Para determinar se o item que tem o retângulo de foco em uma caixa de listagem de seleção múltipla está selecionado, use a mensagem [**\_ GETSEL de lb**](lb-getsel.md) .

Se for enviado para uma caixa de listagem de seleção múltipla, **lb \_ getcurseal** retornará o índice do item que tem o retângulo de foco. Se nenhum item for selecionado, ele retornará zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**\_GETCARETINDEX lb**](lb-getcaretindex.md)
</dt> <dt>

[**\_GETSEL lb**](lb-getsel.md)
</dt> <dt>

[**\_GETSELITEMS lb**](lb-getselitems.md)
</dt> <dt>

[**LB- \_ REcursel**](lb-setcursel.md)
</dt> </dl>

 

 





